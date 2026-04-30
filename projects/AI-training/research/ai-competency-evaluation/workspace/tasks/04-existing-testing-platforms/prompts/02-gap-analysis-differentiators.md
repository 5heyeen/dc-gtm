# Prompt 02: gap-analysis-differentiators

> **Prompt:** Competitive analysis and differentiator spec for the new web-based AI competency test

---

## Overview

The landscape of AI competency testing in 2026 is fragmented across three distinct clusters: hiring-screening tools (HackerRank, Turing), learning-path-integrated assessments (Pluralsight, Coursera, Microsoft AI Skills Navigator), and lightweight literacy checks (TestDome, iMocha, AI Act Blog). None of these was designed to solve the same problem: establishing a vendor-neutral, multi-role, organisation-level AI competency baseline with actionable team-level gap reporting. That structural absence is the market opportunity the new test is designed to fill.

---

## (a) Comparison Table: New Test vs. Top 4 Existing Platforms

| Criterion | **New Test** | **HackerRank** | **Pluralsight Skill IQ** | **Microsoft AI Skills Navigator** | **iMocha AI Literacy** |
|---|---|---|---|---|---|
| **Audience** | All professional roles — technical and non-technical; org-level cohorts | Software developers, ML engineers; individual hiring candidates | Technical practitioners (developers, data scientists); individual learners | Microsoft ecosystem users (IT, knowledge workers); individual learners | Enterprise hiring teams screening candidates |
| **Scope** | 6 competency dimensions: Conceptual Understanding, Prompt Literacy, Critical Evaluation, Ethics & Responsibility, Workflow Integration, Agentic AI & Orchestration; 4 levels | Classical ML, prompt engineering (Jan 2025), RAG (Apr 2025); developer-centric; limited ethics/governance coverage | Classical ML/AI; cloud-based AI services; limited GenAI/prompt engineering; minimal governance | Microsoft Copilot, Azure AI, M365 AI; ecosystem-locked; limited vendor-neutral coverage | AI concepts, generative AI basics, prompt design, ethics, governance; broad but shallow |
| **Format** | 24-item two-stage adaptive MCQ; scenario-based stems; Bloom's-stratified (6 Beginner / 12 Intermediate / 6 Advanced); 20–25 min | MCQ + coding challenges + prompt engineering tasks + RAG tasks; AI-collaborative coding; variable length | 20+ adaptive MCQ; timed; Bayesian scoring; no coding or scenario-based tasks | Self-reported intake survey; links to learning modules; no objective diagnostic item | MCQ with scenario questions; short test; no adaptive routing |
| **Scoring** | IRT 3PL theta (or Bloom's-weighted classical proxy pre-pilot); 4-level placement: Beginner / Intermediate / Advanced / Expert; dimensional profile per competency domain | Band scoring for RAG (Excellent/Good/Satisfactory/Needs Improvement); partial credit on prompt engineering; conversation log capture | Continuous 0–300 Skill IQ score; percentile-based 5-level bands (Novice to Expert); no domain sub-scores | Personalised learning plan output; no objective competency score; scoring tied to Microsoft Certification exams only | Pass/fail or band result; no detailed diagnostic sub-scores documented publicly |
| **Reporting** | Individual level diagnosis + dimensional radar/bar profile; org-level cohort gap report; timestamped baseline for pre/post training comparison | Individual candidate report with full AI interaction log; hiring-manager view; not designed for org-level aggregation | Individual Skill IQ score + recommended learning path; no team-level gap dashboard | Individual learning path recommendation; no org-level analytics dashboard documented | Individual test result; enterprise platform may support aggregation but not with validated diagnostic depth |
| **Cost / Access** | Designed as standalone web tool; intended to be accessible without platform subscription or ecosystem lock-in | Paid enterprise platform; hiring-pipeline context; not available as org baseline diagnostic off-the-shelf | Subscription-based (per seat or team plan); requires Pluralsight platform access | Requires Microsoft licensing; free entry point for individuals but org analytics tied to Microsoft 365/Azure subscriptions | Enterprise pricing; closed pipeline for hiring use; not a free-standing diagnostic |

---

## (b) 5 Specific Differentiators

**1. Multi-role design across the full professional spectrum.**
Every competing platform either targets technical practitioners (HackerRank, Pluralsight, Turing) or creates a generic literacy baseline that lacks depth for technical roles (iMocha, AI Act Blog). The new test's 6-dimension framework — which spans Conceptual Understanding through Agentic AI & Orchestration — is explicitly calibrated to discriminate skill at all levels, from a HR manager who needs prompt literacy and critical evaluation to a software engineer who needs workflow integration and agentic AI knowledge. No existing instrument attempts this full-spectrum design within a single coherent scoring model. (Cited Findings: Task 04 Prompt 01 — gap finding; Task 01 — 6-dimension taxonomy.)

**2. Org-level cohort gap reporting as a first-class output.**
Existing platforms produce individual scores for individual decisions (hire / don't hire; which course to enrol in). None was designed to answer the question an L&D director or CTO actually needs answered: "Where are the skill gaps across my team of 60 people, broken down by role and competency domain?" The new test generates team-level aggregate reports from the same dimensional profile data used for individual placement. This transforms the assessment from a point-in-time credential into a strategic workforce planning instrument. (Cited Findings: Task 04 Prompt 01 — Inferred Finding 1; Task 03 Prompt 03 — reporting logic with timestamped baseline.)

**3. Timestamped baseline enabling pre/post training measurement on the same scale.**
Because the new test uses IRT-calibrated scoring (or Bloom's-weighted proxy pre-pilot) that places all test-takers on the same theta scale regardless of which specific items they answered, a re-test after training produces a directly comparable score. This creates a closed-loop measurement system: organisations can demonstrate ROI from AI training investments in a quantified, auditable way. No platform surveyed offers this capability for general AI competency at the organisational level. Microsoft's Navigator does not produce a comparable objective score. Pluralsight's Skill IQ is percentile-relative (population shifts change scores). (Cited Findings: Task 03 Prompt 01 — IRT vertical scaling; Task 03 Prompt 03 — progress baseline design.)

**4. Vendor-neutral, tool-agnostic scope.**
Microsoft AI Skills Navigator is structurally locked to the Azure/Copilot/M365 ecosystem. Pluralsight's AI role IQs are anchored to AWS or specific cloud platforms. Even HackerRank's prompt engineering tasks are evaluated using a specific AI assistant. The new test is designed around transferable judgment competencies — how to evaluate AI output quality, when to suspend AI use, how to design a human+AI workflow — that apply regardless of which tools an employee uses. This is critical for organisations with heterogeneous AI tooling or vendor relationships they do not want to pre-determine through their skills assessment. (Cited Findings: Task 01 — 6 dimensions including Critical Evaluation and Ethics & Responsibility; Task 04 Prompt 01 — Microsoft gap analysis.)

**5. Two-stage adaptive routing without requiring a CAT engine.**
Pluralsight uses Bayesian adaptive MCQ but requires full platform infrastructure. Full computerised adaptive testing (CAT) requires 80–120 calibrated items and IRT parameters unavailable at launch. The new test's two-stage routing design (12 Intermediate items first, then routing to Beginner or Advanced based on Stage 1 score) achieves adaptive precision with standard branching logic in any web platform. This design reduces floor/ceiling waste, shortens the effective test for participants at clear extremes, and is implementable immediately. It is a structural advance over the flat-form MCQ used by iMocha and the non-adaptive quizzes used by Coursera. (Cited Findings: Task 03 Prompt 03 — two-stage routing design; Task 03 Prompt 01 — IRT TIF and item placement rationale.)

---

## (c) 3 Features to Avoid Building

**1. A coding challenge or hands-on technical execution environment.**
HackerRank already does this better than any new entrant could match quickly: it supports prompt engineering tasks, RAG evaluation tasks, AI-collaborative coding, and full conversation-log capture — with years of validated item banks and employer adoption behind it. Building a code execution environment is expensive, technically complex, and irrelevant for the non-technical half of the new test's target audience. The new test should stay within scenario-based MCQ and reserve hands-on task formats for a future advanced module only after the core instrument is validated.

**2. A certification or badge credential tied to the test.**
LinkedIn, Microsoft (AI-900, AI-102), Google (GCPE, MLE), AWS, and Coursera already occupy the credentialing space. A new badge from an unknown issuer competes for employer recognition against these established brands and loses. More importantly, it creates the wrong incentive: learners chase the credential rather than using the test as a diagnostic tool. The new test's value proposition is gap identification and workforce planning, not credentialing. Positioning it as a diagnostic instrument — not a pass/fail gate — avoids this trap and differentiates cleanly from the certification-heavy competitive field.

**3. A full learning management system (LMS) or course recommendation engine.**
Pluralsight, Coursera, and Microsoft Skills Navigator all include course recommendation engines as their primary output. Building this feature replicates existing infrastructure and creates direct vendor competition the new test cannot win on content breadth. Instead, the test output should generate a structured gap profile that links to curated external resources (agnostically) or integrates via API into whichever LMS the organisation already uses. The core product is measurement, not content delivery.

---

## (d) Recommended Positioning

**What it is:** A 24-item, 20-minute, web-based AI competency diagnostic that places individuals at one of four levels (Beginner / Intermediate / Advanced / Expert) across six vendor-neutral skill dimensions, and aggregates results into team-level gap reports.

**For whom:** L&D managers, HR directors, and team leads at organisations deploying AI tools who need to baseline workforce AI readiness, prioritise training investment, and measure training impact — and who need a tool that works across both technical and non-technical roles from a single instrument.

**What problem it solves that nothing else does:** The combination of (a) multi-role coverage across the full spectrum from AI literacy to agentic AI engineering, (b) org-level cohort reporting rather than individual scores only, (c) timestamped pre/post comparability on the same measurement scale, and (d) complete vendor neutrality — in a single lightweight web tool requiring no platform subscription or ecosystem commitment. Today, an organisation trying to answer "where is our AI capability gap, across all roles, and how do we measure progress?" has no single instrument available. They must stitch together Pluralsight for developers, iMocha for general staff, and manual surveys for everyone else — with no common scale, no cohort aggregation, and no pre/post comparability. The new test solves exactly that problem.

---

## Inferred Findings

**IF-1: Organisations with heterogeneous AI tooling have no vendor-neutral baseline diagnostic option available today.**
- Based on: Task 04 Prompt 01 finding that Microsoft AI Skills Navigator is ecosystem-locked; Pluralsight Skill IQ is cloud-platform-anchored; HackerRank assesses tool-specific tasks (prompt engineering using a specific AI assistant).
- Reasoning: If all three technically advanced platforms are vendor- or ecosystem-locked, and the lightweight tools (iMocha, TestDome) lack depth for technical roles, then the market gap for a vendor-neutral multi-role instrument is real and unserved, not just claimed. An organisation using a mix of OpenAI, Anthropic, and open-source models cannot use any existing platform without accepting ecosystem bias in their baseline data.

**IF-2: Org-level cohort gap reporting is the highest-value unbuilt feature in the AI competency testing market.**
- Based on: Task 04 Prompt 01 — Inferred Finding 1 (no platform provides org-level AI competency baseline); Task 03 Prompt 03 — reporting logic explicitly designed for team-level output; Task 02 research showing EU AI Act Article 4 creates a compliance obligation for organisations to demonstrate employee AI literacy.
- Reasoning: The EU AI Act's mandatory AI literacy obligation (Task 02 context) creates a regulatory pull for organisations to document workforce AI competency. Hiring-focused platforms (HackerRank, Turing) produce candidate-level data that cannot be aggregated for workforce compliance purposes. A tool that produces an org-level gap report with a timestamped audit trail directly addresses a compliance need that none of the surveyed platforms serves.

**IF-3: The intermediate Bloom's band (Apply/Analyze) is the key differentiating zone where the new test must outperform competitors.**
- Based on: Task 03 Prompt 02 — Apply/Analyze is where self-reported literacy diverges most sharply from demonstrated skill; Task 04 Prompt 01 — Pluralsight focuses on knowledge of technical concepts rather than applied problem-solving, lacks scenario-based tasks.
- Reasoning: If competitors cluster at recall-and-understand question formats (definitional MCQ), and the Apply/Analyze band is where real skill discrimination occurs, then a test that concentrates 50% of its items (12 of 24) at this level will generate more accurate placement and more actionable gap profiles than any competitor — even with a smaller total item bank.

---

## Unverified Observations

- Workera (formerly part of deeplearning.ai's ecosystem) reportedly offers adaptive AI competency assessments for enterprise workforce planning with role-based benchmarking. If this is confirmed, it would represent the closest existing competitor to the new test's positioning. This could not be verified from available research.
- The OECD MAIL (Media and AI Literacy) test, planned for 2029 field trials with results expected by end of 2031, may eventually set an internationally validated benchmark that the new test should align with. Alignment now would position the new test favourably when that standard emerges.
- Enterprise adoption data for iMocha's AI Literacy test (number of organisations using it for workforce baselining vs. purely for hiring screening) is not publicly available and may materially affect the competitive assessment above.

---

## Sources

- https://www.hackerrank.com/writing/demystifying-generative-ai-hiring-evaluating-rag-llm-skills-hackerrank-april-2025-assessments
- https://www.hackerrank.com/writing/prompt-engineering-questions-hackerrank-coding-interview-tests-2025-practice-guide
- https://www.hackerrank.com/writing/designing-2025-ai-skills-assessment-hackerrank-prompt-engineering-rag-ai-interviewer
- https://help.pluralsight.com/hc/en-us/articles/24394106940180-Introduction-to-Skill-IQ
- https://www.pluralsight.com/product/skills-assessment
- https://aiskillsnavigator.microsoft.com/
- https://techcommunity.microsoft.com/blog/skills-hub-blog/certifications-refresh-ai-focused-and-fundamentals-updates/4446638
- https://www.imocha.io/tests/ai-literacy-test
- https://www.testdome.com/tests/ai-literacy-test/262
- https://www.linkedin.com/help/linkedin/answer/a507663/linkedin-skill-assessments?lang=en
- https://www.turing.com/resources/ai-driven-talent-assessment
- https://ailiteracy.institute/ai-literacy-tests/
- https://www.aiactblog.nl/en
- https://www.sciencedirect.com/science/article/pii/S294988212500060X
- https://courses.cfte.education/aiq-ai-skills-assessment/
- https://joint-research-centre.ec.europa.eu/projects-and-activities/education-and-training/digital-transformation-education/digital-competence-framework-digcomp/digcomp-30_en
- https://en.wikipedia.org/wiki/Item_response_theory
- https://www.publichealth.columbia.edu/research/population-health-methods/item-response-theory
- https://www.washington.edu/assessment/scanning-scoring/scoring/reports/item-analysis/
- https://link.springer.com/article/10.1007/s40593-025-00471-z
- https://arxiv.org/html/2412.00970v1
- https://www.sciencedirect.com/science/article/pii/S2666920X24000857

---
*Executed: 2026-04-30 | Mode: sequential*
