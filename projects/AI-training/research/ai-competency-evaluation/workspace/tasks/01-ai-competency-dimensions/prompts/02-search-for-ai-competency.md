# Prompt 02: search-for-ai-competency

> **Prompt:** What skill dimensions do Microsoft, Google, Anthropic, OpenAI frameworks identify for AI competency?

---

## Microsoft: AI Skills Initiative & Certifications

Microsoft's framework is the most explicitly tiered of the four. As of February 2026 it released four new certifications spanning entry-level to expert, framing AI competency across at least three axes: **role/persona** (business professional vs. IT admin vs. architect), **technical depth** (usage vs. configuration vs. design), and **organisational scope** (individual productivity vs. enterprise transformation).

Cert-level descriptors from the certification refresh:

- **AB-900** — "entry-level IT admins" responsible for Copilot and Agent Administration Fundamentals — establishes an administrative/governance skill dimension.
- **AB-730** — validates "the ability to use generative AI and Copilot to streamline workflows" — a *task-automation / productivity* dimension aimed at business professionals.
- **AB-731** — verifies "ability to define AI's business value and drive company-wide AI adoption" — a *strategic/leadership* dimension.
- **AB-100** — expert-level "designing multi-agent AI systems" — an *agentic system design* dimension for architects.

"[Microsoft Learn officially announced the general availability of 4 new AI Certifications and 6 new Microsoft Applied Skills credentials on February 25, 2026.](https://www.sci-tech-today.com/news/microsoft-ai-certifications-applied-skills-2026/)" — [Microsoft AI Certifications 2026 Overview](https://www.sci-tech-today.com/news/microsoft-ai-certifications-applied-skills-2026/)

Microsoft also runs an AI Skills Navigator and a **People Skills** platform that uses "AI-powered skill inferencing" to map employee competencies — reflecting a *skill self-awareness / meta-competency* dimension built into the tooling itself. "Since launching in June 2025, People Skills has become foundational within Microsoft 365 — powering Copilot and a new generation of Copilot agents." — [Microsoft Community Hub](https://techcommunity.microsoft.com/blog/microsoft365copilotblog/people-skills-expanding-skills-intelligence-to-more-users-and-surfaces-across-mi/4497646)

**Proficiency levels:** Yes — four cert tiers (Fundamentals → Associate/Professional → Expert) map to distinct proficiency bands.

---

## Google: AI Essentials & AI Professional Certificate

Google's framework, anchored in the AI Professional Certificate launched February 2026, organises AI competency around **use-case domains** rather than technical depth levels. The six core competency areas are: **communication, research, data analysis, content generation, planning,** and **"vibe coding"** (building custom applications without writing code). These map directly to the seven courses in the certificate:

- AI Fundamentals
- AI for Brainstorming and Planning
- AI for Research and Insights
- AI for Writing and Communicating
- AI for Content Creation
- AI for Data Analysis

"The program focuses on six core competencies: communication, research, data analysis, content generation, planning, and what Google calls 'vibe coding' — building custom applications without writing actual code." — [ALM Corp Guide to Google AI Professional Certificate](https://almcorp.com/blog/google-ai-professional-certificate-complete-guide/)

Google's framing is explicitly **task-oriented and worker-facing**: "Learners gain in-demand AI skills to help speed up daily tasks, make more informed decisions, develop new ideas and content, with hands-on experience in AI tools that can be immediately integrated into daily workflow." — [Google AI Essentials / Coursera](https://www.coursera.org/specializations/ai-essentials-google)

**Proficiency levels:** Not explicitly tiered within the certificate itself — it is a single-level credential, though it builds on the prior AI Essentials course (which functions as a lower rung).

---

## Anthropic: Claude Usage & Prompt Engineering Documentation

Anthropic's public documentation does not use the language of a "competency framework" explicitly, but the Prompting Best Practices guide implicitly structures skill across five technique-clusters:

1. **Clarity and instruction precision** — writing unambiguous, well-scoped prompts.
2. **Structural formatting** — use of XML tags, markdown, and output templates.
3. **Role prompting and context-setting** — assigning personas and defining task boundaries.
4. **Reasoning elicitation** — requesting chain-of-thought, step-by-step decomposition, and evidence-first responses.
5. **Agentic and tool-use orchestration** — managing multi-step pipelines, tool-call triggering, subagent spawning, and effort/budget parameters.

"All prompting techniques — from clarity and examples to XML structuring, role prompting, thinking, and prompt chaining — are covered in Prompting best practices. That's the living reference; start there." — [Anthropic Prompt Engineering Overview](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/overview)

The best-practices page further distinguishes skill by **model-generation awareness** (prompts must be tuned per model version) and **effort calibration** ("Start with the new `xhigh` effort level for coding and agentic use cases, and use a minimum of `high` effort for most intelligence-sensitive use cases"), implicitly adding a *parameter governance* dimension unique to Anthropic's framing. — [Claude Prompting Best Practices](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/claude-prompting-best-practices)

**Proficiency levels:** Implicit rather than explicit — the framework progresses from basic prompt clarity → structural techniques → agentic orchestration, but no formal levels are named.

---

## OpenAI: Skills Guides & Academy

OpenAI's competency framing in 2025-2026 centres on **reusable workflow construction** rather than individual user skill. The Codex Skills framework (launched December 2025) defines a skill as a package of "instructions, resources, and optional scripts so agents can follow workflows reliably." — [OpenAI Codex Skills](https://developers.openai.com/codex/skills)

OpenAI Academy covers "using ChatGPT skills to build reusable workflows, automate recurring tasks, and ensure consistent, high-quality outputs." — [OpenAI Academy: Using Skills](https://openai.com/academy/skills/)

The broader OpenAI developer-facing literature identifies an implicit dimension set: **AI engineering, software architecture, security, cost optimisation, and business alignment** — though these are described as enterprise requirements rather than a formal competency ladder.

**Proficiency levels:** No formal tiered proficiency framework published. OpenAI's approach is tool-capability-centric rather than learner-level-centric.

---

## Cross-Cutting Comparison: Industry vs. Academic/Standards-Body Definitions

Industry frameworks (Microsoft, Google, Anthropic, OpenAI) converge on **functional, task-oriented skill clusters** — what a user *does with* AI — rather than on cognitive or epistemic competencies. Academic and standards-body frameworks (e.g., DigComp 2.2, UNESCO's AI competency framework for teachers) tend to foreground **critical evaluation, ethical reasoning, and AI literacy** as distinct dimensions, and explicitly model progression from awareness → understanding → application → creation.

Key contrasts:

| Dimension | Industry Frameworks | Academic/Standards Frameworks |
|---|---|---|
| Primary organising principle | Task domain / tool capability | Cognitive level / epistemic stance |
| Ethics & critical AI literacy | Rarely a named skill dimension | Core required dimension |
| Proficiency levels | Present in Microsoft; absent/implicit in others | Systematically defined (e.g., 3–5 levels) |
| Societal/contextual awareness | Absent or marginal | Central (DigComp, UNESCO) |
| Target learner | Worker / developer | General citizen or educator |

---

## Inferred Findings

1. **Google's "vibe coding" signals a collapsing boundary between user and developer skill.** Based on: (a) the inclusion of "building custom applications without writing actual code" as a core competency — [ALM Corp](https://almcorp.com/blog/google-ai-professional-certificate-complete-guide/); (b) OpenAI's parallel shift toward skill-as-workflow rather than skill-as-knowledge — [OpenAI Codex Skills](https://developers.openai.com/codex/skills). Inference: industry frameworks are converging toward a single "orchestration" skill tier that blurs the developer/end-user distinction.

2. **Anthropic's effort-calibration dimension is unique and technically demanding.** Based on: (a) the effort parameter taxonomy (`low` → `medium` → `high` → `xhigh` → `max`) described in prompting best practices — [Claude Prompting Best Practices](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/claude-prompting-best-practices); (b) the absence of equivalent constructs in Google or OpenAI's public skill guides. Inference: Anthropic implicitly requires a *model-parameter literacy* skill dimension that the other vendors do not surface at the user level.

---

## Unverified Observations

- OpenAI Academy may have a more structured competency framework behind its login wall that was not accessible for this research (the `/academy/skills/` page returned a 403 error).
- Microsoft's Applied Skills credentials (6 new ones announced February 2026) may contain more granular skill dimension descriptions than the certification summaries captured here; full rubrics were not publicly accessible.
- Google AI Essentials and the AI Professional Certificate may differ in their internal skill taxonomies in ways not captured by publicly available course descriptions.

---

## Sources

- https://www.sci-tech-today.com/news/microsoft-ai-certifications-applied-skills-2026/
- https://techcommunity.microsoft.com/blog/microsoft365copilotblog/people-skills-expanding-skills-intelligence-to-more-users-and-surfaces-across-mi/4497646
- https://aiskillsnavigator.microsoft.com/
- https://techcommunity.microsoft.com/blog/skills-hub-blog/certifications-refresh-ai-focused-and-fundamentals-updates/4446638
- https://almcorp.com/blog/google-ai-professional-certificate-complete-guide/
- https://www.coursera.org/specializations/ai-essentials-google
- https://grow.google/ai
- https://ai.google/learn-ai-skills/
- https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/overview
- https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/claude-prompting-best-practices
- https://github.com/anthropics/prompt-eng-interactive-tutorial
- https://openai.com/academy/skills/
- https://developers.openai.com/codex/skills
- https://github.com/openai/skills

---
*Executed: 2026-04-30 | Mode: independent*
