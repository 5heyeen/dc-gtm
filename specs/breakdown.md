# Spec: Breakdown

## Overview
- **Type:** Skill
- **Trigger / Invocation:** `/breakdown [free-text | file-path | notion-url]`
- **Date:** 2026-03-29
- **Status:** Draft

## 1. Functional Spec (What)

### Purpose
`/breakdown` is a personal skill that takes a large, potentially vague task and transforms it into a structured checklist of smaller, self-contained subtasks. It can be invoked at planning time before any work begins, or mid-task when scope has grown. It conducts a short interactive interview to clarify scope, constraints, and priorities before producing a numbered checklist saved as both a markdown file and a Notion page.

### Use Cases
- Starting a large feature and needing to scope it before writing any code
- Realizing mid-implementation that a task is too big and needs splitting
- Turning a Notion brief or a file-based task description into an actionable checklist
- Capturing a task discussed in conversation and breaking it into steps

### Inputs & Arguments
| Input | Type | Required | Description |
|-------|------|----------|-------------|
| Free-text description | String (inline argument) | No | Task description passed directly, e.g. `/breakdown "migrate auth to OAuth"` |
| File path | File path (argument) | No | Path to a markdown/text file containing the task, e.g. `/breakdown ./tasks/big-feature.md` |
| Notion URL | URL (argument) | No | A Notion page URL whose content describes the task |
| No argument | — | No | Infers the task from the current conversation context |

At least one input source must be resolvable. If no argument is provided and no clear task exists in conversation context, `/breakdown` warns the user and asks for clarification before proceeding.

### Expected Output
1. **Markdown file** saved to a user-specified project directory (asked interactively). Contains the task title, a brief context summary, and a numbered checklist of subtasks with one-line descriptions.
2. **Notion page** created under a user-specified parent page (asked interactively). Mirrors the markdown structure.

### Edge Cases & Error Handling
- **Too vague input:** If the task description cannot be broken down meaningfully, warn and ask for more context before producing any output. Never generate a low-quality breakdown.
- **No input + no conversation context:** Warn the user and prompt them to describe the task.
- **Invalid file path:** If the file does not exist, report the error and ask the user to correct it.
- **Invalid/unfetchable Notion URL:** Report the error and ask the user to describe the task manually.
- **Notion MCP unavailable:** Save the markdown file successfully and inform the user the Notion page could not be created.

### Acceptance Criteria
- **Given** a vague free-text task, **When** I run `/breakdown "something vague"`, **Then** the skill asks clarifying questions and only produces a breakdown once it has sufficient detail.
- **Given** a Notion page URL with a task brief, **When** I run `/breakdown https://notion.so/...`, **Then** the skill fetches the page, conducts a targeted interview for missing context, and produces a breakdown.
- **Given** a file path, **When** I run `/breakdown ./tasks/big-feature.md`, **Then** the skill reads the file and adapts its interview based on what's already written.
- **Given** no argument mid-conversation, **When** I run `/breakdown`, **Then** the skill infers the task from conversation context and proceeds to the interview.
- **Given** a vague one-word input, **When** the skill cannot determine what needs to be broken down, **Then** it warns and asks for more detail before outputting anything.

## 2. Technical Plan (How)

### Architecture & Approach
1. **Parse the argument**: Detect whether the argument is a Notion URL (starts with `https://notion.so` or `https://www.notion.so`), a file path (starts with `./`, `/`, or `~`), free text, or absent.
2. **Resolve the task description**:
   - File path → Read tool
   - Notion URL → `notion-fetch` MCP tool
   - Free text → use as-is
   - No argument → summarize from recent conversation context
3. **Vagueness check**: If the resolved description is fewer than ~20 words or lacks a clear goal, warn and ask the user to elaborate before continuing.
4. **Interview loop** (one question at a time via `AskUserQuestion`):
   - What are the constraints or deadlines?
   - What does "done" look like — is there a clear end state?
   - Are there known dependencies or blockers between parts?
   - What are the riskiest or least-understood areas?
5. **Generate breakdown**: Produce 4–10 self-contained subtasks, each with a short title and one-line description. Order them by dependency.
6. **Ask for save locations**: Ask for the local project directory and the Notion parent page URL.
7. **Write markdown file**: Save to `<project-dir>/<kebab-case-task-name>.md`.
8. **Create Notion page**: Use `notion-create-pages` under the user-provided parent.
9. **Optionally mirror to TodoWrite**: Create in-conversation tasks for visibility.

### Tools & MCPs Required
- **AskUserQuestion**: Interactive interview to gather clarifying info and save locations
- **Read / Glob / Grep**: Read task descriptions from local files
- **notion-fetch (Notion MCP)**: Fetch task content from a Notion page URL
- **Write**: Save the markdown breakdown file to disk
- **TodoWrite**: Mirror subtasks as in-conversation task items (optional)
- **notion-create-pages (Notion MCP)**: Create the output Notion page

### Files to Create or Modify
| File | Action | Purpose |
|------|--------|---------|
| `~/.claude/commands/breakdown.md` | Create | Skill definition and behavior prompt |

### Patterns & Reuse
- Interview-driven flow similar to `/spec-out` but lighter-weight (fewer, more focused questions)
- Output format borrows the task-breakdown checklist structure from SDD specs
- Argument-parsing logic (URL vs. path vs. text vs. none) is a reusable pattern

### Constraints & Non-Goals
- ✅ In scope: interactive clarification interview, breakdown generation, markdown file output, Notion page output, optional TodoWrite mirroring
- ❌ Out of scope: writing any implementation code
- ❌ Out of scope: creating GitHub issues or pull requests
- ❌ Out of scope: time estimates or task assignment/ownership
- ❌ Out of scope: running as a background agent (always interactive foreground)

## 3. Task Breakdown

Each task is self-contained and completable in a single agent session.

- [ ] **Task 1:** Write the skill prompt file at `~/.claude/commands/breakdown.md` with full behavior instructions covering argument parsing, interview flow, vagueness check, output formatting, and save-location prompts — *Verify:* File exists and `/breakdown --help` (or a dry-run invocation) shows expected behavior.
- [ ] **Task 2:** Test the free-text invocation path end-to-end: run `/breakdown "migrate the database layer to use Prisma"`, confirm interview fires, markdown file is saved to specified dir, and Notion page is created — *Verify:* Both outputs exist with correct structure and content.
- [ ] **Task 3:** Test the file-path invocation: run `/breakdown ./some-task.md`, confirm the file is read and interview adapts (skips questions already answered by the file) — *Verify:* Breakdown reflects file content, interview is appropriately shorter.
- [ ] **Task 4:** Test the Notion URL path: run `/breakdown https://notion.so/...`, confirm the page content is fetched and seeds the interview — *Verify:* Breakdown reflects the Notion page content.
- [ ] **Task 5:** Test the no-argument path mid-conversation, confirm the skill infers the task from context — *Verify:* Skill does not ask "what is the task?" when context is clear.
- [ ] **Task 6:** Test the vague-input edge case with a minimal description — *Verify:* Skill warns and asks for clarification before producing any output.

## 4. Examples

### Example Invocation
```
/breakdown "migrate the database layer to use Prisma"
```

### Example Output
```
> What are the constraints on this migration — keeping the existing schema or redesigning it?
  → "Keeping the schema, just swapping the ORM"

> What does done look like — full cutover, or incremental dual-write?
  → "Full cutover, we'll do it in a feature branch"

> Any known risky or poorly-understood areas?
  → "The raw SQL queries in the reporting module"

Where should I save the markdown file? (project directory path)
  → ~/projects/my-app/tasks/

Which Notion parent page should I create the breakdown under? (paste URL)
  → https://www.notion.so/My-Project-Tasks-abc123

---

Saved: ~/projects/my-app/tasks/migrate-database-layer-to-prisma.md
Notion page created: [Migrate Database Layer to Prisma] under My Project Tasks

Breakdown: Migrate Database Layer to Prisma
1. Audit all existing ORM queries and identify raw SQL usage in reporting module
2. Install Prisma and initialize schema from current database
3. Generate Prisma client and validate against existing schema
4. Migrate model layer to Prisma (one model at a time)
5. Migrate service layer to use generated Prisma client
6. Rewrite raw SQL in reporting module using Prisma query builder
7. Update test suite to use Prisma test client
8. Remove old ORM dependency and clean up configuration
9. Smoke-test all DB interactions in staging before merging
```

### Other Invocation Forms
```
/breakdown ./docs/big-feature.md
/breakdown https://www.notion.so/My-Task-Brief-abc123
/breakdown
```
