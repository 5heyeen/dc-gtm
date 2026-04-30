# Task Breakdown: AI Competency Evaluation Research

**Scope:** Research the full spectrum of methods for evaluating AI competency — from prompt writing through agentic AI — to inform a multiple-choice web test that diagnoses starting level and tracks progress over time. Primary audience is professionals new to AI; full technical spectrum (through coding, RAG, fine-tuning, agentic systems) is in scope.
**Date:** 2026-04-30

---

### Task 01: AI Competency Dimensions & Taxonomy
Research how AI competency is structured as a multi-dimensional skill space. Find existing taxonomies, skill maps, and level models that describe what someone needs to know and be able to do with AI — from basic literacy and prompt writing through critical evaluation, workflow integration, API use, and system design. Look for sources from academia (AI literacy research), industry (Microsoft, Google, Anthropic skill guides), and standards bodies (UNESCO, OECD). Completion: a documented map of skill dimensions and a defensible level model (beginner → intermediate → advanced → expert) with published citations.

### Task 02: Existing AI Competency Frameworks & Certifications
Survey the landscape of published AI competency frameworks and formal certifications. Targets include: EU DigComp / DigComp2.2, UNESCO AI Competency Frameworks for Citizens and Teachers, OECD AI skills taxonomy, Microsoft AI Skills Initiative / Copilot certifications, Google Cloud AI certifications, AWS AI Practitioner, Coursera/DeepLearning.AI certificates, and any emerging national AI literacy standards (e.g. UK, Norway, US). For each: what skill levels do they define, what is the assessment format, and how do they distinguish levels? Completion: a structured comparison table of frameworks with their level definitions, skill domains, and assessment approach.

### Task 03: Assessment Design Principles for AI Skills Tests
Research evidence-based principles for designing multiple-choice competency assessments that reliably discriminate between skill levels. Covers: Bloom's taxonomy applied to AI skills testing, item difficulty and discrimination indices, question formats that test understanding vs. recall, scenario-based MCQ design, psychometric best practices for diagnostic tests, and how to construct a scoring model that produces a "start here" recommendation and a trackable progress score. Look for sources in instructional design, psychometrics, and published AI/digital skills test design guides. Completion: a set of actionable design principles with examples and sources.

### Task 04: Existing AI Skills Testing Platforms & Tools
Survey platforms that currently offer AI competency assessments or skill tests. Targets: LinkedIn Learning skill assessments, Pluralsight AI skill IQ, HackerRank AI/ML assessments, Coursera quizzes, Turing AI tests, dedicated upskilling platforms (Learnit, AI Academy, DataCamp), and any platforms specifically built for AI literacy testing. For each: what skill areas do they cover, what question formats do they use, how do they score and report results, and what are gaps or weaknesses in their approach? Completion: a comparative overview of existing platforms with gap analysis.

### Task 05: Advanced Technical Tier Assessment (RAG, Agents, Fine-tuning)
Research how to assess advanced AI skills that go beyond tool usage: prompt engineering at an expert level, API integration, retrieval-augmented generation (RAG), multi-step agent orchestration, fine-tuning and model adaptation, AI system evaluation and evals design. Look for benchmark datasets, challenge problems, or published assessment rubrics that distinguish intermediate from advanced practitioners. Sources: research papers, GitHub repositories for AI evals (e.g. HELM, MMLU, AgentBench), developer certification programmes, and practitioner community assessments. Completion: a documented set of distinguishing questions/tasks for the advanced and expert tiers, with sources.

### Task 06: Test Architecture & Scoring Model Design
*[Sequential — depends on Tasks 01–05]* Synthesise findings from all prior tasks into a concrete test architecture. Define: the number of competency levels and their descriptions, the skill dimensions to test at each level, the recommended number of questions per dimension/level, the question format (scenario-based MCQ), the scoring logic that produces a level diagnosis and progress-tracking baseline, and any adaptive testing considerations (e.g. skip easy questions if early answers are strong). This is a synthesis task — no web research. Completion: a structured test specification document ready to hand to a developer building the web test.

---

## Dependency Map

| Task | Type | Depends On |
|------|------|------------|
| 01 | [independent] | — |
| 02 | [independent] | — |
| 03 | [independent] | — |
| 04 | [independent] | — |
| 05 | [independent] | — |
| 06 | [sequential] | 01, 02, 03, 04, 05 |

## Execution Waves

- **Wave 1:** Tasks 01, 02, 03, 04, 05 (all independent — run sequentially one at a time)
- **Wave 2:** Task 06 (sequential synthesis — runs after Wave 1 completes)
