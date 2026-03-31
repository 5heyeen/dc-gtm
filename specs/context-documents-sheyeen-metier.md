# Spec: Context Documents — Sheyeen & Metier

## Overview
- **Type:** Memory
- **Trigger / Invocation:** Auto-loaded at conversation start (slim files); on-demand via Read tool (deep reference docs)
- **Date:** 2026-03-29
- **Status:** Implemented

## 1. Functional Spec (What)

### Purpose
Two-tier context system for Sheyeen Liew and her employer Metier AS. A slim memory file per subject is auto-loaded every conversation (minimal token cost), containing essential facts plus pointers to deep reference documents that Claude fetches only when additional detail is needed for a specific task.

### Use Cases
- Claude understands who Sheyeen is and how to collaborate with her without being told each session
- Claude understands what Metier does and can frame advice in the right industry/company context
- Claude can fetch deeper career, goals, or company detail on demand without bloating every conversation

### Inputs & Arguments
| Input | Type | Required | Description |
|-------|------|----------|-------------|
| Personal profile data | Interview + Notion CV | Yes | Name, role, domain, tech level, working style |
| Company context data | Notion page | Yes | Metier overview, services, methodologies |
| Current goals | Notion database | Yes | In-progress goals across career, health, finances |

### Expected Output
Four files:
1. `memory/user_sheyeen_profile.md` — slim, auto-loaded personal memory
2. `memory/reference_metier.md` — slim, auto-loaded company reference
3. `memory/MEMORY.md` — index file pointing to both
4. `docs/sheyeen_deep_profile.md` — full career background + current goals
5. `docs/metier_deep_context.md` — full company context, service hierarchy, methodologies

### Edge Cases & Error Handling
- If memory dir does not exist, create it before writing
- If MEMORY.md already exists, append new entries rather than overwrite

### Acceptance Criteria
- **Given** a new conversation, **When** Claude loads context, **Then** it knows Sheyeen's name, role, domain, tech level, and communication preferences without being told
- **Given** a task requiring company context, **When** Claude reads the slim Metier memory, **Then** it understands Metier's positioning and Sheyeen's department
- **Given** a task requiring deeper career detail, **When** Claude reads the pointer in the slim file, **Then** it can fetch the deep profile and apply relevant background

## 2. Technical Plan (How)

### Architecture & Approach
Tiered memory system:
- **Tier 1 (always loaded):** Slim `.md` files in `~/.claude/projects/c--Users-shelie--claude/memory/` — essential facts only, ~10–20 lines each
- **Tier 2 (on demand):** Full reference docs in `~/.claude/docs/` — comprehensive detail Claude reads only when the task warrants it
- Each Tier 1 file ends with explicit pointers to both the local Tier 2 file and the source Notion page

### Tools & MCPs Required
- Write: create all files
- mcp__claude_ai_Notion__notion-create-pages: publish spec to Notion

### Files to Create or Modify
| File | Action | Purpose |
|------|--------|---------|
| `~/.claude/projects/c--Users-shelie--claude/memory/user_sheyeen_profile.md` | Create | Slim personal memory |
| `~/.claude/projects/c--Users-shelie--claude/memory/reference_metier.md` | Create | Slim company memory |
| `~/.claude/projects/c--Users-shelie--claude/memory/MEMORY.md` | Create | Memory index |
| `~/.claude/docs/sheyeen_deep_profile.md` | Create | Deep personal reference doc |
| `~/.claude/docs/metier_deep_context.md` | Create | Deep company reference doc |

### Constraints & Non-Goals
- ✅ In scope: personal profile, company context, current goals
- ✅ In scope: tiered slim/deep architecture
- ❌ Out of scope: family details (user opted out)
- ❌ Out of scope: project-specific memories (handled separately per project)

## 3. Task Breakdown

- [x] **Task 1:** Create memory directory and docs directory — *Verify:* directories exist
- [x] **Task 2:** Write slim personal memory file `user_sheyeen_profile.md` — *Verify:* file contains name, role, domain, tech level, working style, pointer to deep doc
- [x] **Task 3:** Write slim company memory file `reference_metier.md` — *Verify:* file contains company name, purpose, service pillars, Sheyeen's dept, pointer to deep doc
- [x] **Task 4:** Write MEMORY.md index with pointers to both slim files — *Verify:* both entries present
- [x] **Task 5:** Write deep personal reference doc with full CV summary and current goals — *Verify:* all career history and in-progress goals included
- [x] **Task 6:** Write deep Metier reference doc with full company context — *Verify:* service hierarchy, methodologies, customer cases included
- [x] **Task 7:** Create Notion spec page — *Verify:* page exists under Specifications workspace

## 4. Examples

### Example — slim memory loaded
Claude reads `user_sheyeen_profile.md` at conversation start and automatically:
- Addresses Sheyeen by name
- Frames answers with bullet-point leads + why/what/how/when elaboration
- Offers 2–3 options rather than a single recommendation
- Applies business-first framing to technical decisions

### Example — deep profile fetched on demand
User: "Help me write a bio for a pitch deck"
Claude reads pointer → fetches `docs/sheyeen_deep_profile.md` → draws on specific project experience (Frier Vest, Bulk Data Centers, Elkem CAPEX) to write a targeted bio
