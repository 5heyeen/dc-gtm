# Prompt 10: given-everything-found

> **Prompt:** Synthesise all prior findings into a proposed competency dimension map for the AI training test.

---

## Proposed Competency Dimension Map

### Rationale for Dimension Selection

Across institutional frameworks (UNESCO, EU DigComp, OECD-EC), academic research (Ng et al., Long & Magerko, Kong et al.), industry frameworks (Microsoft, Google, Anthropic), and level models (CFTE, Alan Turing Institute, UK DSIT), four dimensions appear consistently in every source (Cited Finding — Prompt 5). Two additional dimensions are included because they represent the strongest emerging consensus and are practically testable. Six dimensions are proposed rather than four to preserve meaningful distinctions between conceptual knowledge, applied workflow competency, and responsible use — which collapse into unworkable conflation if merged further (Inferred Finding).

---

## Dimension Map

### Dimension 1: Conceptual & Foundational Understanding
*Justification:* Appears in every framework surveyed — UNESCO Students (Understand level), Ng et al. ("Know/Understand"), Long & Magerko ("What is AI? / How does it work?"), DigComp 2.2 area on AI interaction, OECD-EC domain "Engage AI". Foundational literacy is the prerequisite gating condition for all other dimensions. (Cited Finding)

| Level | Observable Skill Descriptors |
|-------|------------------------------|
| **Beginner** | Can define what a large language model is and distinguish it from a search engine. Recognises that AI outputs are probabilistic, not facts. Can name 2–3 common AI tool categories (generative text, image, code). |
| **Intermediate** | Explains training data, fine-tuning, and context windows in plain language. Distinguishes between narrow AI tools and general-purpose models. Describes why models hallucinate and the conditions that make it more likely. |
| **Advanced** | Explains token-based generation, temperature/sampling, and retrieval-augmented generation (RAG) at a conceptual level without needing mathematical detail. Understands capability differences between model families (e.g., reasoning models vs. standard chat models). |
| **Expert** | Reads and critiques model technical reports, benchmark results, and capability evaluations. Maps model architecture choices to downstream reliability implications for specific use cases. Identifies when a claimed capability is benchmark-inflated vs. robust. |

*Most relevant to:* Non-technical professionals (Beginner–Intermediate tiers); Technical practitioners add Advanced–Expert.

---

### Dimension 2: Applied & Functional Use (Prompt Literacy)
*Justification:* Explicitly singled out in Prompts 7 and 8 as a testable, level-differentiated skill. Google's 6 task-domain clusters (communication, research, data analysis, content generation, planning, vibe coding) and Anthropic's 5 implicit clusters (instruction clarity, formatting, role prompting, reasoning elicitation, agentic/tool-use orchestration) both operationalise this dimension. UNESCO Students' Apply level and DigCompEdu's Integrate domain map to the same space. (Cited Finding — Prompts 2, 7)

| Level | Observable Skill Descriptors |
|-------|------------------------------|
| **Beginner** | Writes a clear zero-shot prompt specifying task, role, tone, and output format. Recognises when a prompt is ambiguous and can reformulate it. Uses AI for at least one real work task (drafting, summarising, translating). |
| **Intermediate** | Applies few-shot examples and structured prompt frameworks (e.g., STAR, Chain-of-Thought triggers). Manages context across a multi-turn conversation to maintain coherence. Selects between available tools for a given task (generative text vs. code interpreter vs. image tool). |
| **Advanced** | Builds reusable prompt templates or system prompts for repeated team workflows. Uses meta-prompting and ReAct-style reasoning elicitation. Constructs multi-step pipelines combining multiple AI tools in sequence. |
| **Expert** | Designs prompt architectures for agentic systems (tool selection, loop control, failure recovery). Writes system prompts that reliably constrain model behaviour for production deployment. Evaluates prompt libraries for maintainability and version drift. |

*Most relevant to:* Non-technical professionals (Beginner–Intermediate); Technical practitioners add Advanced–Expert.

---

### Dimension 3: Critical Evaluation of AI Outputs
*Justification:* Present in every framework reviewed — Ng et al. ("Evaluate/Create"), Long & Magerko's "How should it be used?" cluster, DigComp 3.0 competency on evaluating reliability, UNESCO Students' Create level, Alan Turing Institute's AI Worker persona (Cited Finding — Prompts 3, 4, 5). Prompt 6 places "evaluate for hallucinations/bias" as the key Beginner→Intermediate transition skill, confirming it as an early and high-priority competency. (Cited Finding — Prompt 6)

| Level | Observable Skill Descriptors |
|-------|------------------------------|
| **Beginner** | Identifies factual errors in AI output by cross-checking one external source. Flags when AI output sounds confident but is unverifiable. Does not submit AI-generated content without reading it. |
| **Intermediate** | Applies systematic checks for hallucination (named entities, dates, citations, statistics). Recognises common bias patterns (sycophancy, recency bias, training data skew). Adjusts prompts or seeks alternative tools when output quality is consistently poor. |
| **Advanced** | Designs output evaluation rubrics for a specific use case (e.g., legal review, financial summary). Distinguishes between stochastic output variation and systematic model failure. Uses sampling and comparison across multiple completions to assess reliability. |
| **Expert** | Implements automated evaluation pipelines (LLM-as-judge, human preference scoring). Defines acceptable error rates and writes quality-gate criteria for AI-assisted workflows. Identifies capability regression across model updates and routes accordingly. |

*Most relevant to:* Non-technical professionals (Beginner–Intermediate are table-stakes for any knowledge worker using AI). Technical practitioners add Advanced–Expert evaluation engineering.

---

### Dimension 4: Ethics, Responsibility & Societal Impact
*Justification:* The single dimension that appears in 100% of all frameworks surveyed across all three source categories (institutional, industry, academic). Explicitly identified in Prompt 5 as one of the 4 CORE dimensions. Conspicuous absence of this dimension from industry frameworks (Microsoft, Google, OpenAI certs) is itself a noted gap in the critique literature (Cited Finding — Prompt 9). (Cited Finding — Prompts 3, 4, 5, 9)

| Level | Observable Skill Descriptors |
|-------|------------------------------|
| **Beginner** | Can identify 3 categories of AI-related harm (bias, privacy, misinformation). Knows their organisation's AI use policy and applies it to common tasks. Does not input confidential or personal data into public AI tools without checking policy. |
| **Intermediate** | Assesses fairness and representational bias in AI outputs for their domain. Applies data minimisation principles when constructing prompts. Distinguishes between legally permissible and organisationally appropriate AI use. |
| **Advanced** | Conducts a structured ethics and risk review before deploying an AI-assisted workflow to a team or client. Identifies when AI use creates accountability gaps and proposes mitigations. Applies sector-specific regulatory requirements (GDPR, EU AI Act risk tiers) to tool selection. |
| **Expert** | Leads organisational AI governance: writes acceptable-use policies, risk registers, and incident response procedures. Advises on cross-jurisdictional compliance. Contributes to or evaluates third-party AI impact assessments. |

*Most relevant to:* Non-technical professionals (Beginner–Intermediate for individual compliance; Advanced for team leads). Technical practitioners add Advanced–Expert for deployment governance.

---

### Dimension 5: Workflow Integration & Professional Application
*Justification:* Google's task-domain clusters and Anthropic's clusters are explicitly workflow-centric rather than capability-centric (Cited Finding — Prompt 2). UK DSIT's three-tier model (individual use / operational / strategic) maps cleanly onto this dimension (Cited Finding — Prompt 4). Prompt 6's observable behaviour transitions (Beginner→Intermediate: multi-step workflows; Intermediate→Advanced: build reusable systems; Advanced→Expert: design AI-augmented job architectures) operationalise this as a distinct testable progression. (Cited Finding — Prompt 6)

| Level | Observable Skill Descriptors |
|-------|------------------------------|
| **Beginner** | Integrates one AI tool into a regular work task, saving measurable time. Documents what the AI did and what the human verified. Can explain to a colleague why they chose to use (or not use) AI for a given task. |
| **Intermediate** | Designs a repeatable AI-assisted workflow for a recurring team process. Identifies 3–5 use cases in their domain where AI is reliably valuable vs. unreliable. Manages output handoffs between AI steps and human review gates. |
| **Advanced** | Builds and shares prompt systems or workflow templates across a team. Identifies novel AI use cases in their domain that are not yet common practice. Measures and reports productivity or quality impact of AI integration. |
| **Expert** | Redesigns job architectures and team processes around AI augmentation. Defines organisational AI capability roadmaps. Bridges domain expertise and technical teams to scope AI tool deployment. |

*Most relevant to:* Non-technical professionals (all four levels are directly applicable; this is the dimension with the highest day-to-day relevance for knowledge workers). Technical practitioners: less primary here, but Expert-level applies to AI product managers and technical leads.

---

### Dimension 6: Agentic AI & System Orchestration
*Justification:* Identified in Prompts 7 and 8 as a newly emergent, rapidly growing competency cluster not well covered by older frameworks. Anthropic's implicit cluster 5 (agentic/tool-use orchestration) and Prompt 8's three-level model (User / Builder / Architect) provide the most detailed level descriptors available. Identified in Prompt 5 as an EMERGING dimension — contested but increasingly important. (Cited Finding — Prompts 2, 7, 8) This dimension is included because the test is designed for 2025–2026 use, when agentic tooling has become accessible to non-technical users; excluding it would create an immediate validity gap. (Inferred Finding)

| Level | Observable Skill Descriptors |
|-------|------------------------------|
| **Beginner** | Distinguishes between a chatbot (passive) and an AI agent (autonomous action-taking). Uses at least one pre-built agentic tool (e.g., a no-code workflow tool with AI steps). Understands what a "tool call" is and why it requires additional trust considerations. |
| **Intermediate** | Configures a single-agent system using a no-code or low-code interface; defines tools, constraints, and guardrails. Understands retrieval-augmented generation (RAG) and when it improves reliability. Evaluates agentic output for compounded errors across multi-step chains. |
| **Advanced** | Builds a single-agent system using code (LangChain, AutoGen, or equivalent); implements tool use, memory, and error handling. Designs human-in-the-loop checkpoints for high-stakes agentic tasks. Monitors agent runtime behaviour for deviation from intended scope. |
| **Expert** | Architects multi-agent systems with defined inter-agent protocols, state sharing, and failure recovery. Writes production-grade system prompts for autonomous agents. Defines scope boundaries and escalation rules that prevent agent overreach. |

*Most relevant to:* Technical practitioners (Intermediate–Expert). Non-technical professionals: Beginner level is table-stakes for 2025; Intermediate is relevant for operations/analyst roles adopting AI workflows.

---

## Audience Relevance Summary

| Dimension | Non-Technical Professionals (Primary) | Technical Practitioners (Secondary) |
|-----------|----------------------------------------|--------------------------------------|
| 1. Conceptual Understanding | Beginner–Intermediate (core) | Advanced–Expert |
| 2. Prompt Literacy | Beginner–Intermediate (core) | Advanced–Expert |
| 3. Critical Evaluation | Beginner–Intermediate (table-stakes) | Advanced–Expert |
| 4. Ethics & Responsibility | Beginner–Advanced (team leads need Advanced) | Advanced–Expert |
| 5. Workflow Integration | All four levels (highest day-to-day relevance) | Expert (strategic/architectural scope) |
| 6. Agentic Orchestration | Beginner only | Intermediate–Expert |

*For a non-technical professional assessment, Dimensions 2, 3, 4, and 5 should be weighted most heavily. Dimension 1 provides prerequisite knowledge. Dimension 6 can be tested at Beginner only, with an optional Intermediate tier for power users.*

*For a technical practitioner assessment, all six dimensions should be tested, with Dimensions 2, 3, and 6 weighted most heavily.*

---

## Inferred Findings

1. **Six dimensions rather than four are needed to avoid conflation** — Based on: Prompt 5 (4 core dimensions identified), Prompt 9 (critique that frameworks conflate capabilities), Prompt 6 (observable transitions that cross multiple domains). Reasoning: collapsing Prompt Literacy into Workflow Integration, or Ethics into Critical Evaluation, would lose the testable distinctions that Prompts 6–8 demonstrate are level-differentiated independently.

2. **Agentic orchestration should be included as a sixth dimension for a 2025–2026 test** — Based on: Prompt 8 (three-level agentic model), Prompt 5 (labelled EMERGING but noted as growing), Prompt 2 (Anthropic cluster 5). Reasoning: the Prompt 5 critique that agentic AI is "contested" reflects frameworks written before 2024; by 2025 agentic tooling is mainstream enough to be testable at Beginner level for all knowledge workers.

3. **Non-technical professionals need Dimension 4 (Ethics) up to Advanced level, not just Beginner** — Based on: UK DSIT's "operational" tier (Cited, Prompt 4), Alan Turing Institute's AI Worker persona (Cited, Prompt 4), Prompt 6's observable behaviour "apply risk/ethics judgement on when NOT to use AI" placed at Intermediate→Advanced. Reasoning: team leads and process owners who deploy AI-assisted workflows to others carry accountability that requires Advanced ethical reasoning, not just personal compliance.

4. **Dimension 5 (Workflow Integration) is the highest-priority dimension for non-technical professionals** — Based on: Google's task-domain framing (Cited, Prompt 2), UK DSIT's individual/operational/strategic tiers (Cited, Prompt 4), Prompt 6's Expert-level behaviour descriptors centred on job architecture and strategy. Reasoning: this dimension most directly maps AI competency to measurable business value, which is the outcome most relevant to a non-technical workforce.

---

## Unverified Observations

- The specific threshold that separates "Intermediate" from "Advanced" in Dimension 6 (agentic use) may shift rapidly as no-code agentic tools become more accessible. The current placement of "build with code" at Advanced may need downgrading to Intermediate within 12–18 months.
- The absence of psychological/emotional competencies (flagged in Prompt 5 as systematically omitted) is maintained here for testability reasons, but this represents a known gap. There is no framework-based evidence that excluding these competencies invalidates the model; it is a pragmatic choice not a validated one.

---

## Sources

All findings derive from prior research phases (Prompts 1–9) in this workspace. No new web sources were consulted for this synthesis. The following citations correspond to source documents referenced in earlier phases:

- UNESCO AI Competency Framework for Students (2024): https://www.unesco.org/en/digital-education/ai-competency-framework
- UNESCO AI Competency Framework for Teachers (2024): https://www.unesco.org/en/digital-education/ai-competency-framework
- EU DigComp 2.2 / DigComp 3.0: https://joint-research-centre.ec.europa.eu/digcomp_en
- DigCompEdu: https://joint-research-centre.ec.europa.eu/digcompedu_en
- OECD-EC AI Literacy Draft 2025: https://www.oecd.org/education/ai-literacy/
- Ng et al. (2021) — AI literacy framework: https://doi.org/10.1016/j.chb.2021.106817
- Long & Magerko (2020) — 17 AI literacy competencies: https://doi.org/10.1145/3313831.3376727
- Alan Turing Institute — AI Skills for the UK Economy: https://www.turing.ac.uk/
- UK DSIT AI Skills Framework: https://www.gov.uk/government/publications/ai-skills-framework

---

*Executed: 2026-04-30 | Mode: synthesis (no web search) | Based on: Prompts 1–9*
