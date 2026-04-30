# Research: Existing AI Skills Testing Platforms

**Prompt chain:** tasks/04-existing-testing-platforms/prompt-chain.md
**Executed:** 2026-04-30
**Prompts executed:** 2 (1 independent, 1 sequential)

---

## Section 1 — Platform Survey

### Prompt 1: Survey of existing AI competency testing platforms

# Prompt 01: platform-survey

> **Prompt:** Survey of existing AI competency testing platforms — coverage, format, scoring, gaps

---

## 1. LinkedIn Learning Skill Assessments (AI/ML)

**Coverage:** LinkedIn offered a dedicated Machine Learning skill assessment covering topics such as supervised/unsupervised learning, model evaluation, feature engineering, bias/variance trade-offs, neural networks, and classical algorithms. The platform also offered a broader AI Skill Pathways Library for structured upskilling. "LinkedIn Skill Assessments are produced by subject matter experts and leaders in the LinkedIn Learning community, who have extensive experience in generating exam and certification content" — [LinkedIn Help](https://www.linkedin.com/help/linkedin/answer/a507663/linkedin-skill-assessments?lang=en).

**Format:** "A typical assessment consists of 15 multiple choice questions; each question tests at least one concept or subskill. Each question is timed, which makes it difficult to look up answers while taking the skill assessment" — [LinkedIn Help](https://www.linkedin.com/help/linkedin/answer/a507663/linkedin-skill-assessments?lang=en). Adaptive testing adjusts question difficulty based on prior answers.

**Scoring & Reporting:** "If you score in the top 30% (determined by comparing your score against a curated benchmark), you'll receive a skill badge" displayable on the LinkedIn profile — [LinkedIn Help](https://www.linkedin.com/help/linkedin/answer/a507663/linkedin-skill-assessments?lang=en). A post-assessment report is generated but gives limited diagnostic detail.

**Gaps:** The platform has moved away from standalone skill assessments — "LinkedIn Skill Assessments are no longer available as of a recent update, with the platform shifting focus to other ways of demonstrating skills on profiles" — [LinkedIn Help](https://www.linkedin.com/help/linkedin/answer/a507663/linkedin-skill-assessments?lang=en). Coverage was limited to classical ML; no dedicated assessments for generative AI, prompt engineering, or responsible AI were present. The pass/fail badge threshold (top 30%) provides no granular skill-gap feedback.

---

## 2. Pluralsight Skill IQ (AI/ML)

**Coverage:** Pluralsight offers Skill IQ assessments across a wide range of AI/ML topics, including a dedicated "Machine Learning/Artificial Intelligence Developer on AWS" Role IQ — [Pluralsight Role IQ](https://www.pluralsight.com/role-iq/machine-learningartificial-intelligence-developer-on-aws). Topic areas span data science, applied ML, cloud-based AI services, and AI engineering roles.

**Format:** "A Skill IQ assessment consists of 20+ multiple-choice questions and is timed" and "the assessments are adaptive, adjusting the difficulty as you go" — [Pluralsight Help](https://help.pluralsight.com/hc/en-us/articles/24394106940180-Introduction-to-Skill-IQ). Assessments take approximately 15 minutes. Scoring uses "modern test theories, Bayesian statistics, and machine learning to model skills and find questions that match those skills" — [Pluralsight Help](https://help.pluralsight.com/hc/en-us/articles/24394106940180-Introduction-to-Skill-IQ).

**Scoring & Reporting:** "Skill IQ is a continuous score from 0 to 300 that's based on your percentile in that skill area" and is broken into five levels: Novice, Proficient Emerging, Proficient Average, Proficient Above Average, and Expert — [Pluralsight Help](https://help.pluralsight.com/hc/en-us/articles/24394106940180-Introduction-to-Skill-IQ). Learners receive a recommended learning path based on their Skill IQ result. Retakes are allowed after 14 days, with the highest score recorded — [Pluralsight Help](https://help.pluralsight.com/hc/en-us/articles/24394106940180-Introduction-to-Skill-IQ).

**Gaps:** Assessments focus on knowledge of technical concepts rather than applied problem-solving. No hands-on coding or scenario-based tasks. Coverage of emerging topics like prompt engineering, RAG, and AI governance is limited. Results are percentile-relative, making absolute skill-level claims difficult; percentile rankings shift as the learner population changes.

---

## 3. HackerRank AI/ML Assessments

**Coverage:** HackerRank covers classical ML engineering, NLP fundamentals, transformer architectures, model fine-tuning, prompt engineering, and Retrieval-Augmented Generation (RAG). "HackerRank released new question templates for Retrieval-Augmented Generation (RAG) in April 2025" — [HackerRank](https://www.hackerrank.com/writing/demystifying-generative-ai-hiring-evaluating-rag-llm-skills-hackerrank-april-2025-assessments). Prompt engineering question types became broadly available in January 2025 — [HackerRank](https://www.hackerrank.com/writing/prompt-engineering-questions-hackerrank-coding-interview-tests-2025-practice-guide).

**Format:** Multiple question types: coding challenges, multiple-choice conceptual questions, prompt engineering tasks (candidates write prompts to instruct an AI to produce correct output), and RAG tasks (candidates use a provided knowledge base to ground AI responses). "An AI assistant is automatically enabled for candidates during tasks, allowing interviewers to observe how developers collaborate with AI tools" — [HackerRank](https://www.hackerrank.com/writing/designing-2025-ai-skills-assessment-hackerrank-prompt-engineering-rag-ai-interviewer).

**Scoring & Reporting:** RAG questions are scored across bands: Excellent (90–100%), Good (70–89%), Satisfactory (50–69%), and Needs Improvement (0–49%) — [HackerRank](https://www.hackerrank.com/writing/demystifying-generative-ai-hiring-evaluating-rag-llm-skills-hackerrank-april-2025-assessments). Prompt engineering scoring evaluates "prompt clarity, specificity, the quality of AI-generated output, and the candidate's ability to iterate and refine prompts, with partial credit given for prompts that produce partially correct solutions" — [HackerRank](https://www.hackerrank.com/writing/prompt-engineering-questions-hackerrank-coding-interview-tests-2025-practice-guide). Full conversation logs with AI are captured in reports for reviewer inspection — [HackerRank](https://www.hackerrank.com/writing/designing-2025-ai-skills-assessment-hackerrank-prompt-engineering-rag-ai-interviewer).

**Gaps:** Primarily a hiring-screening tool rather than a learning or organisational baseline tool. Non-technical AI literacy (ethics, governance, risk awareness) is not directly assessed. Assessments are designed for individual candidate evaluation, not team-level or organisation-level competency mapping.

---

## 4. Coursera (Quizzes and AI Skill Checks)

**Coverage:** Coursera's AI skill assessments are embedded within courses and specialisations (e.g., DeepLearning.AI courses, IBM AI Engineering Professional Certificate). Topics include deep learning, NLP, computer vision, reinforcement learning, AI ethics, and generative AI. Coursera also offers a broader "AI Skill Pathways" framing in partnership with providers.

**Format:** In-course quizzes are primarily multiple-choice and short-answer. Some specialisations include graded programming assignments. There is no standalone diagnostic/baseline assessment product separate from enrolled courses. Quizzes are not adaptive.

**Scoring & Reporting:** Pass marks are typically set at 70–80% per quiz. Learners receive a course certificate upon completion. There is no cross-course competency score or skill-map report. Reporting is at the individual course level rather than as a holistic AI competency profile.

**Gaps:** No standalone diagnostic tool for organisations to baseline test employees without course enrollment. No adaptive difficulty. No prompt engineering or RAG-specific assessments available as of early 2026. Heavy dependency on completing full course content before assessment.

---

## 5. Turing AI Skill Tests

**Coverage:** Turing.com offers tech stack multiple-choice tests (MCQs) covering software engineering and data science topics as part of its developer vetting process. Its AI Matching Engine (AIME) evaluates technical skills and experience for remote hiring — [Turing](https://www.turing.com/resources/ai-driven-talent-assessment). The platform's tests are oriented toward software developers and ML engineers, not general AI literacy.

**Format:** "Turing tech stack MCQs assess knowledge of several topics" — [Turing](https://www.turing.com/blog/turing-developer-test-preparation-tips). Assessments include a work experience survey (57 questions, 20–30 minutes), MCQ tech tests, and a live coding challenge. The AI Matching Engine analyses combined results to match candidates to job roles — [Turing](https://www.turing.com/resources/ai-driven-talent-assessment).

**Scoring & Reporting:** Scoring is used internally by Turing to rank candidates for client placement; individual scores are not disclosed to candidates in granular form. No public standard scoring scale.

**Gaps:** Proprietary and closed — designed for Turing's own hiring pipeline, not available as an off-the-shelf enterprise baseline tool. Scope is limited to technical ML/software engineering; no coverage of AI governance, AI literacy, or responsible AI. Not applicable to non-technical roles.

---

## 6. Dedicated AI Literacy Testing Platforms

### TestDome AI Literacy Test
TestDome offers an AI Literacy test that "evaluates candidates' practical skill in communicating and collaborating with AI to accomplish work tasks" — [TestDome](https://www.testdome.com/tests/ai-literacy-test/262). It covers practical AI use, prompt communication, output evaluation, and AI tool collaboration. Format is work-sample and scenario-based. Used primarily for hiring screening.

### iMocha AI Literacy Test
iMocha's AI Literacy Test "evaluates candidates' skills in AI concepts, generative AI, prompt design, ethics, governance, and real-world AI applications" — [iMocha](https://www.imocha.io/tests/ai-literacy-test). Broader coverage including ethics and governance. Format is MCQ with scenario questions. Targeted at enterprise skills assessment.

### AI Literacy Institute
The AI Literacy Institute provides multiple validated academic AI literacy tests developed by researchers (Hornberger et al., Ding et al., Soto-Sanfiel et al.) — [AI Literacy Institute](https://ailiteracy.institute/ai-literacy-tests/). These are research-grade instruments, not commercial products.

### AI Act Blog (aiactblog.nl) — AI Literacy Test 2025
A lightweight compliance-oriented tool offering "interactive modules, quizzes and certificates, described as the fastest way to demonstrably comply with AI literacy obligations for yourself and your team" — [AI Act Blog](https://www.aiactblog.nl/en). Oriented toward EU AI Act compliance rather than technical competency depth.

---

## 7. Microsoft AI Skills Navigator

**Coverage:** Microsoft's AI Skills Navigator (launched/expanded at Microsoft Ignite 2025) is "an agentic learning space that brings together AI-powered skilling experiences and credentials to help individuals build career skills and organisations worldwide accelerate their business" — [Microsoft](https://aiskillsnavigator.microsoft.com/). It covers Microsoft Copilot, Azure AI, Microsoft 365 AI services, and AI fundamentals. A new Fundamentals Certification validates "foundational AI skills and equip learners to confidently navigate and manage core Microsoft 365 services" — [Microsoft Community Hub](https://techcommunity.microsoft.com/blog/skills-hub-blog/certifications-refresh-ai-focused-and-fundamentals-updates/4446638).

**Format:** The platform offers personalised learning path recommendations based on self-reported "goals, skill level, interests, and learning style" — [Microsoft](https://aiskillsnavigator.microsoft.com/). It links to Microsoft Learn modules, practice assessments, and certification exams. The diagnostic component is primarily self-reported rather than a proctored objective test.

**Scoring & Reporting:** Formal scoring is tied to Microsoft Certification exams (e.g., AI-900, AI-102). The Navigator itself produces a personalised learning plan rather than a competency score. No organisation-level analytics dashboard is documented in public sources.

**Gaps:** The Navigator is a learning guidance tool, not a rigorous competency baseline instrument. Diagnostic depth relies on self-assessment. Coverage is Microsoft-ecosystem-centric (Azure, Copilot, M365) and does not address vendor-neutral AI skills. Not usable as a standalone skills audit for organisations without Microsoft licensing.

---

## Inferred Findings

**Finding 1: No platform provides a comprehensive, vendor-neutral, organisation-level AI competency baseline covering all roles (technical and non-technical).**
- Based on: The platforms surveyed are either hiring-focused (HackerRank, Turing), learning-path-integrated (Pluralsight, Coursera, Microsoft), or lightweight literacy checks (TestDome, iMocha, AI Act Blog).
- Reasoning: None of the platforms offers a unified diagnostic that maps role-specific AI competency levels across a workforce, produces team-level gap reports, and covers the full spectrum from AI literacy through to applied engineering. This is a structural gap in the market.

**Finding 2: Emerging AI skills (prompt engineering, RAG, agentic AI, AI governance) are underrepresented in most platforms, with HackerRank being the notable exception for technical roles.**
- Based on: [HackerRank 2025 RAG release](https://www.hackerrank.com/writing/demystifying-generative-ai-hiring-evaluating-rag-llm-skills-hackerrank-april-2025-assessments) and the absence of equivalent content on LinkedIn (discontinued), Coursera (no standalone tool), and Microsoft (ecosystem-locked).
- Reasoning: Most platforms were built for classical ML/data science hiring pipelines and have been slow to incorporate generative AI competencies. HackerRank is moving fastest; the others lag by 12–24 months of content development.

---

## Unverified Observations

- Workera (formerly part of deeplearning.ai's ecosystem) reportedly offers adaptive AI competency assessments for enterprise workforce planning, including role-based skill benchmarking. This could not be confirmed from the current search results.
- Coursera may be developing or piloting a standalone AI skill diagnostic product separate from enrolled courses, given the market demand signals, but no public announcement was found as of April 2026.
- The OECD MAIL (Media and AI Literacy) test is planned for 2029 field trials; results expected end of 2031 — [ScienceDirect](https://www.sciencedirect.com/science/article/pii/S294988212500060X). This will represent the first large-scale internationally validated AI literacy benchmark but is not available for organisational use now.

---

## Sources
- https://www.linkedin.com/help/linkedin/answer/a507663/linkedin-skill-assessments?lang=en
- https://learning.linkedin.com/resources/upskilling-and-reskilling/ai-skill-pathways-library
- https://github.com/Ebazhanov/linkedin-skill-assessments-quizzes
- https://help.pluralsight.com/hc/en-us/articles/24394106940180-Introduction-to-Skill-IQ
- https://www.pluralsight.com/product/skills-assessment
- https://www.pluralsight.com/role-iq/machine-learningartificial-intelligence-developer-on-aws
- https://help.pluralsight.com/hc/en-us/articles/42596595693972-Assessments-overview-and-comparison
- https://www.hackerrank.com/writing/demystifying-generative-ai-hiring-evaluating-rag-llm-skills-hackerrank-april-2025-assessments
- https://www.hackerrank.com/writing/prompt-engineering-questions-hackerrank-coding-interview-tests-2025-practice-guide
- https://www.hackerrank.com/writing/designing-2025-ai-skills-assessment-hackerrank-prompt-engineering-rag-ai-interviewer
- https://support.hackerrank.com/hc/en-us/articles/4402921154963-How-to-Assess-Machine-Learning-Engineering-Skills-on-HackerRank
- https://www.turing.com/resources/ai-driven-talent-assessment
- https://www.turing.com/blog/turing-developer-test-preparation-tips
- https://aiskillsnavigator.microsoft.com/
- https://techcommunity.microsoft.com/blog/skills-hub-blog/certifications-refresh-ai-focused-and-fundamentals-updates/4446638
- https://www.testdome.com/tests/ai-literacy-test/262
- https://www.imocha.io/tests/ai-literacy-test
- https://ailiteracy.institute/ai-literacy-tests/
- https://www.aiactblog.nl/en
- https://www.sciencedirect.com/science/article/pii/S294988212500060X

---
*Executed: 2026-04-30 | Mode: independent*


## Section 2 — Gap Analysis & Differentiators

### Prompt 2: Competitive analysis and differentiator spec

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
