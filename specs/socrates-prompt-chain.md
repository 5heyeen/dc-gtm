# Spec: Socrates Prompt Chain Skill

## Overview
- **Type:** Skill
- **Trigger / Invocation:** `/socrates-prompt-chain`
- **Date:** 2026-03-29
- **Status:** Draft

## 1. Functional Spec (What)

### Purpose
The `/socratic-research` skill generates an exhaustive Socratic prompt chain for a given topic or task. It uses the Socratic prompting method (principles → framework → expert simulation → failure analysis → objection pre-empt → application) to produce a ready-to-use prompt chain the user can paste into any AI tool to drive deep, structured research. **The skill does NOT conduct research itself** — it only produces the prompts. Output is saved locally as a markdown file and to a user-specified Notion page.

### Use Cases
- User has a research topic or question and wants a structured prompt chain to guide AI-driven research
- User has a task from the `/breakdown` skill (in Notion or a local `.md` file) and wants Socratic prompts tailored to that task
- User wants exhaustive prompt coverage of a domain before conducting research in a separate session

### Inputs & Arguments
| Input | Type | Required | Description |
|-------|------|----------|-------------|
| `<topic>` | free-text | No (skill will ask) | The research topic, question, or problem statement |
| `<breakdown-task>` | Notion URL or local `.md` file path | No | A task reference from the `/breakdown` skill |
| `<domain>` | string keyword | No | Broad category — skill will clarify interactively |

If input is missing or too vague, the skill asks clarifying questions before generating.

### Expected Output
A structured Socratic prompt chain in markdown, organized into labeled sections:
- **Principles** — What makes this type of thing work well?
- **Framework** — What factors matter? What would an expert consider?
- **Expert Simulation** — What would a domain expert ask first?
- **Failure Analysis** — What commonly goes wrong?
- **Objection Pre-Empt** — What would a skeptic challenge?
- **Application** — Apply all of the above to my specific case: [user's context]

Saved to:
1. `~/.claude/research/<topic-slug>.md` (local markdown)
2. A Notion page — the skill asks the user for the parent page URL each time

### Edge Cases & Error Handling
- If input is vague or missing: ask clarifying questions (goal, context, constraints) before generating
- If Notion save fails: save locally, report the error, and provide the Notion page content inline
- If breakdown task source (Notion page or local `.md`) is unreachable: fall back to treating the input as free-text and note the fallback
- If the user cancels mid-clarification: do not generate partial prompts

### Acceptance Criteria
- **Given** I run `/socratic-research go-to-market strategy for B2B SaaS`, **When** the skill finishes, **Then** I receive an exhaustive Socratic prompt chain saved to `~/.claude/research/go-to-market-strategy-for-b2b-saas.md` and a Notion page I specify
- **Given** I run `/socratic-research` with no arguments, **When** the skill runs, **Then** it asks me clarifying questions before generating any prompts
- **Given** I pass a `/breakdown` task reference (Notion URL or `.md` path), **When** the skill runs, **Then** it reads the task context and generates prompts tailored to that specific task
- **Given** I provide a vague input like just "marketing", **When** the skill runs, **Then** it asks clarifying questions to sharpen the topic before generating

---

## 2. Technical Plan (How)

### Architecture & Approach
1. **Parse input**: detect if it's a free-text topic, a domain keyword, a Notion URL (breakdown task), or a local `.md` file path
2. **If breakdown task**: read task content via `mcp__claude_ai_Notion__notion-fetch` or `Read` tool
3. **If input is vague or missing**: use `AskUserQuestion` to clarify the research goal, target audience, context, and key constraints
4. **Generate prompt chain**: produce an exhaustive Socratic chain covering all applicable angles — do not limit to 3 steps; cover as many angles as needed for the topic complexity
5. **Ask for Notion destination**: use `AskUserQuestion` to get the parent Notion page URL
6. **Save locally**: write to `~/.claude/research/<topic-slug>.md` using `Write` tool
7. **Save to Notion**: create a page via `mcp__claude_ai_Notion__notion-create-pages`
8. **Report**: confirm both save locations with clickable paths/URLs

### Tools & MCPs Required
- `AskUserQuestion` — clarifying questions and prompting for Notion save location
- `mcp__claude_ai_Notion__notion-fetch` — read breakdown tasks from Notion
- `mcp__claude_ai_Notion__notion-create-pages` — save prompt chain to Notion
- `Read` / `Glob` / `Grep` — read local `.md` breakdown task files
- `Write` — save prompt chain as local markdown file

### Files to Create or Modify
| File | Action | Purpose |
|------|--------|---------|
| `~/.claude/commands/socratic-research.md` | Create | Skill definition file |
| `~/.claude/research/<topic-slug>.md` | Create (runtime) | Output Socratic prompt chain |

### Patterns & Reuse
- Follows the save-to-Notion + local file pattern established by `/spec-out`
- Integrates with `/breakdown` skill output (Notion pages or local `.md` task lists)
- Uses `AskUserQuestion` interactively in the same style as `/spec-out`

### Constraints & Non-Goals
- ✅ In scope: generating Socratic prompt chains, reading breakdown tasks, saving output locally and to Notion, asking clarifying questions
- ❌ Out of scope: conducting actual research, generating summaries or research reports, performing web searches to inform prompt generation, modifying or updating existing prompt chain files

---

## 3. Task Breakdown

- [ ] **Task 1:** Write the `/socratic-research` skill file at `~/.claude/commands/socratic-research.md` with the full behavior spec, Socratic chain generation instructions, and save logic — *Verify:* File exists and the skill can be invoked with `/socratic-research`
- [ ] **Task 2:** Test with a free-text topic (e.g., "go-to-market strategy for B2B SaaS") — *Verify:* Skill asks clarifying questions, generates an exhaustive prompt chain, saves to `~/.claude/research/`, and saves to Notion
- [ ] **Task 3:** Test with a `/breakdown` task reference (Notion URL) — *Verify:* Skill reads the task, tailors prompts to task context, and saves correctly
- [ ] **Task 4:** Test with a vague/ambiguous input (e.g., "marketing") — *Verify:* Skill asks clarifying questions before generating any prompts, not after

---

## 4. Examples

### Example 1: Free-text Strategy Topic
```
/socratic-research go-to-market strategy for B2B SaaS
```

**Output saved to `~/.claude/research/go-to-market-strategy-for-b2b-saas.md`:**

```markdown
# Socratic Research Prompts: Go-to-Market Strategy for B2B SaaS

## Principles
- What makes a go-to-market strategy actually work for early-stage B2B SaaS?
- What separates a successful GTM from one that burns runway?
- What do companies that nail early distribution have in common?
- What does "product-market fit" really mean in terms of GTM readiness?

## Framework
- What are the core components of a B2B SaaS GTM strategy?
- What channels tend to work best when you have a limited budget?
- How do you decide between product-led, sales-led, and marketing-led growth?
- What metrics define GTM success in the first 90 days vs. 12 months?
- What's the right sequencing of GTM motions at different revenue stages?

## Expert Simulation
- What would a top B2B growth advisor ask before recommending a GTM approach?
- What data would they need? What assumptions would they validate first?
- What would they look at that most founders overlook?
- How would they stress-test the ICP definition?

## Failure Analysis
- What are the most common reasons B2B SaaS GTM strategies fail?
- What do founders typically underestimate about enterprise sales cycles?
- What does premature scaling look like and how do you avoid it?
- What channel bets fail most often and why?

## Objection Pre-Empt
- What would a skeptical enterprise buyer challenge about your GTM assumptions?
- What competitive dynamics would a critic point to?
- What would an investor push back on in your GTM thesis?

## Application
Now apply all of the above to my specific case:
- My product is: [DESCRIBE YOUR PRODUCT]
- My target customer is: [ICP — role, company size, industry]
- My current stage is: [STAGE / FUNDING / TEAM SIZE]
- My constraints are: [BUDGET / TIME / TEAM LIMITATIONS]
- The outcome I want in 90 days is: [SPECIFIC GOAL]
```

---

### Example 2: Breakdown Task Reference
```
/socratic-research https://notion.so/my-workspace/Task-Research-Async-Hiring-abc123
```

Skill reads the task (e.g., "Research best practices for async hiring processes"), generates a tailored Socratic prompt chain for that specific task context, and saves it to `~/.claude/research/async-hiring-best-practices.md` and the specified Notion page.

---

### Example 3: Vague Input → Clarifying Questions
```
/socratic-research hiring
```

Skill responds with clarifying questions:
- "What aspect of hiring are you researching? (e.g., async processes, interviewing, onboarding, sourcing)"
- "What's the context — a specific role type, company stage, or problem you're trying to solve?"
- "What outcome do you want from the research?"

After answers, generates a targeted Socratic prompt chain.
