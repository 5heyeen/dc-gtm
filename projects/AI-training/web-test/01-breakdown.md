# ACA Web Test — Implementation Breakdown

**Project:** AI Competency Assessment (ACA) — web application
**Stack:** Next.js (TypeScript) · Tailwind CSS · Vercel + Vercel Postgres
**Scope:** Participant test + L&D manager dashboard + CSV export
**Auth:** Public test URL · Password-protected `/admin`
**Research source:** `projects/AI-training/research/ai-competency-evaluation/workspace/synthesis.md`
**Date:** 2026-04-30

---

## Decisions

| Decision | Choice |
|----------|--------|
| Tech stack | Next.js 14+ (App Router), TypeScript, Tailwind CSS |
| Database | Vercel Postgres (Neon), EU region (Frankfurt) |
| Deployment | Vercel |
| Auth | Public participant URL · shared-password `/admin` (HTTP-only JWT cookie) |
| Scope | Participant test + results + PDF · L&D dashboard + cohort gap report + CSV export |
| Notion sync | None |

---

## Task List

### Task 01: Initialise project scaffold
Set up the Next.js 14+ (App Router) project with TypeScript, Tailwind CSS, ESLint, and Prettier. Configure Vercel Postgres (or Neon) as the database provider. Create the top-level folder structure: `app/`, `components/`, `lib/`, `db/`, `public/`. Add `.env.local` with database connection string. Completion: `npm run dev` serves a blank home page; `db` connection resolves without error.

### Task 02: Design and migrate database schema
Define and run the initial database migrations. Tables: `question_bank` (item_id, dimension, level, bloom_verb, stem, options JSON, correct_key, distractor_rationale), `test_sessions` (session_id, started_at, stage1_score, route, completed_at, level_assigned), `item_responses` (response_id, session_id, item_id, selected_key, is_correct, time_on_item_ms), `admin_sessions` (token, created_at, expires_at). Completion: all tables exist in the database; `db/schema.ts` exports typed table definitions.

### Task 03: Seed the 24-item question bank
Create a seed script that populates `question_bank` with all 24 assessment items: 6 Beginner, 12 Intermediate, 6 Advanced, spanning all 6 competency dimensions (Conceptual Understanding, Prompt Literacy, Critical Evaluation, Ethics & Responsibility, Workflow Integration, Agentic AI & Orchestration). Each item includes dimension, level, Bloom's verb, stem (≥40 words), four options, correct key, and distractor rationale. Seed from `db/seeds/question-bank.json`. Completion: `npm run db:seed` inserts 24 rows with no constraint violations.

### Task 04: Build test session API routes
Implement the core session API: `POST /api/sessions` (create session, return session_id), `GET /api/sessions/[id]/items` (return the 12 Stage 1 items in randomised order), `POST /api/sessions/[id]/responses` (record a response, return next item or routing decision), `GET /api/sessions/[id]/result` (return scored results after completion). Completion: all routes return correct status codes and typed JSON; tested with Postman or `curl`.

### Task 05: Build participant landing page
Create the `/` route: brief explanation of the test (purpose, format, time estimate: 25 minutes total), a GDPR-compliant consent checkbox ("I agree that my anonymised responses may be stored for research and compliance purposes"), and a "Start Assessment" button that calls `POST /api/sessions` and redirects to `/test/[session_id]`. Completion: landing page renders; consent must be checked before the button is enabled; session is created on click.

### Task 06: Build the Stage 1 test interface
Create the `/test/[session_id]` route. Render one item at a time: scenario stem, four radio-button options (A–D), a "Next" button (disabled until an option is selected). Show a progress indicator ("Question 3 of 12") and the Stage 1 countdown timer (20 minutes). On each submission, call `POST /api/sessions/[id]/responses` and render the next item. Completion: participant can complete all 12 Stage 1 items; timer counts down; responses are persisted.

### Task 07: Implement two-stage routing logic
After the 12th Stage 1 response, the API computes Stage 1 raw score (0–18, Bloom's-weighted: Intermediate items ×2). If score ≥ 9 → assign route `"advanced"` and queue 6 Advanced items; if score < 9 → assign route `"foundational"` and queue 6 Beginner items. Update `test_sessions.route` and `test_sessions.stage1_score`. Return the routing decision and first Stage 2 item to the client. Completion: routing decision is correct for scores above and below the cut; both branches are reachable in testing.

### Task 08: Build the Stage 2 test interface
Extend `/test/[session_id]` to render Stage 2 items after routing. Show a brief transition message ("You're now in the Advanced section — 6 more questions, 5 minutes"). Render the same item component as Stage 1. Replace the 20-minute timer with a 5-minute Stage 2 timer. On completion of the 6th item, call the scoring endpoint and redirect to `/results/[session_id]`. Completion: Stage 2 renders correctly for both routes; auto-submits on timer expiry.

### Task 09: Build the scoring engine
Implement `lib/scoring.ts`. Inputs: array of 24 item_responses with is_correct flags and item metadata. Outputs: (1) per-dimension sub-scores (0–100 scale, Bloom's-weighted within each dimension); (2) overall weighted score; (3) level assignment (Beginner / Intermediate / Advanced) using provisional cut scores; (4) weakest dimensions (bottom 2 by sub-score). Unit-test with mock response sets covering all level assignments. Completion: `scoreSession()` returns correct output for all test cases; `npm test` passes.

### Task 10: Build the radar chart component
Create `components/RadarChart.tsx` using Recharts (or Chart.js via react-chartjs-2). Render a 6-axis radar chart with axes: Conceptual Understanding, Prompt Literacy, Critical Evaluation, Ethics & Responsibility, Workflow Integration, Agentic AI & Orchestration. Each axis scaled 0–100. Accept a `scores` prop (`Record<dimension, number>`). Add axis labels and a subtle fill. Completion: component renders correctly in a test page with mock scores; no external font or image dependencies.

### Task 11: Build the participant results page
Create `/results/[session_id]`. Fetch results from `GET /api/sessions/[id]/result`. Display: (1) level badge (Beginner / Intermediate / Advanced) with a one-sentence interpretation; (2) the radar chart (Task 10); (3) a per-dimension score table with a short description of each dimension; (4) a "Your two weakest areas" call-out with one-line next-step suggestions. Completion: results page renders correctly for both routing paths; all 6 dimension scores displayed.

### Task 12: Implement participant PDF export
Add a "Download your results (PDF)" button on the results page. Implement `GET /api/sessions/[id]/pdf` using `@react-pdf/renderer` or Puppeteer. The PDF includes: participant's level, radar chart (as embedded SVG or canvas snapshot), per-dimension scores, and a footer noting "AI Competency Assessment — [date] — for EU AI Act Article 4 compliance reference." Completion: clicking the button downloads a valid, readable PDF; chart renders in the PDF.

### Task 13: Build admin authentication
Create `/admin/login` route with a single password field. On submit, compare against `ADMIN_PASSWORD` env var (hashed with bcrypt). On success, set an HTTP-only `admin_session` cookie (JWT, 8-hour expiry) and redirect to `/admin`. Add middleware to protect all `/admin/*` routes. Completion: unauthenticated `/admin` access redirects to login; correct password grants access; incorrect password shows error.

### Task 14: Build admin dashboard index
Create `/admin` (the cohort overview page). Display a paginated table of all test sessions: session ID (truncated), date, route taken, level assigned, overall score, and a "View detail" link. Add a search/filter bar (filter by level, date range, route). Completion: all sessions display correctly; pagination works; filters narrow results.

### Task 15: Build the cohort gap report
Create `/admin/gap-report`. Display: (1) average per-dimension score across all sessions (bar chart, 6 bars); (2) a "gap heatmap" table — dimensions × levels, showing % of participants below threshold in each cell; (3) a top-3 "organisational weaknesses" call-out (lowest average dimension scores). Completion: report renders correctly with ≥10 seeded test sessions; charts update when new sessions complete.

### Task 16: Implement CSV export
Add a "Export all data (CSV)" button on the admin dashboard. Implement `GET /api/admin/export/csv`. The CSV includes one row per session: session_id, started_at, completed_at, route, level_assigned, overall_score, and one column per dimension sub-score. Completion: downloaded CSV opens correctly in Excel/Numbers; all columns present; no PII in the export.

### Task 17: Add GDPR compliance layer
Add: (1) a `/privacy` page explaining what data is collected, how long it is retained, and how to request deletion; (2) a `DELETE /api/sessions/[id]` endpoint (token-protected, for data deletion requests); (3) a data retention note in the admin dashboard ("Sessions older than 24 months are auto-deleted"); (4) `robots.txt` blocking `/admin/*` and `/results/*`. Completion: privacy page is linked from the landing page and results page; delete endpoint works; robots.txt is correct.

### Task 18: Add test timers and auto-submit
Implement countdown timers in the test interface using `useInterval` or a custom hook. Stage 1: 20-minute countdown visible in the header. Stage 2: 5-minute countdown. On timer expiry: submit any unanswered items as blank (scored incorrect), call the session completion endpoint, and redirect to results. Show a 60-second warning banner. Completion: timer counts down correctly; auto-submit fires on expiry; no double-submission possible.

### Task 19: Write tests
Write: (1) unit tests for `lib/scoring.ts` covering all level-assignment edge cases (scores at cut boundaries, all-correct, all-incorrect, partial completion); (2) integration tests for the session API routes using a test database; (3) one end-to-end test using Playwright covering the full participant flow (landing → Stage 1 → routing → Stage 2 → results → PDF download). Completion: `npm test` passes; `npx playwright test` passes against localhost.

### Task 20: Configure deployment and monitoring
Configure Vercel project: set production environment variables (`DATABASE_URL`, `ADMIN_PASSWORD`, `JWT_SECRET`), set Vercel Postgres region to EU (Frankfurt) for GDPR compliance. Add Sentry (or Vercel Analytics) for error tracking. Add `next-sitemap` for `/` and `/privacy` only. Write a `README.md` covering local setup, seeding, and deployment. Completion: `vercel deploy` succeeds; production URL is live; admin dashboard is accessible; Sentry receives a test error event.

---

## Dependency Map

```
01 → 02 → 03
          ↓
          04 → 06 → 07 → 08 → 09 → 10 → 11 → 12
          ↓                        ↑
          05 ──────────────────────┘
          
09 → 15
13 → 14 → 15 → 16

17 (parallel after 05)
18 (parallel after 06, 08)
19 (after 09, 04)
20 (after all)
```

**Wave 1 (foundation):** Tasks 01, 02, 03
**Wave 2 (core flow):** Tasks 04, 05, 06, 07, 08
**Wave 3 (scoring + output):** Tasks 09, 10, 11, 12, 18
**Wave 4 (admin):** Tasks 13, 14, 15, 16
**Wave 5 (compliance + QA + deploy):** Tasks 17, 19, 20
