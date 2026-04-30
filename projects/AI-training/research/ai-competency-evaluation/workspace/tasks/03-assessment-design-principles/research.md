# Research: Assessment Design Principles for AI Skills Tests

**Prompt chain:** tasks/03-assessment-design-principles/prompt-chain.md
**Executed:** 2026-04-30
**Prompts executed:** 3 (2 independent, 1 sequential)

---

## Section 1 — Psychometric Foundations

### Prompt 1: MCQ design principles and diagnostic scoring
# Prompt 01: mcq-design-principles

> **Prompt:** Evidence-based principles for designing MCQ competency assessments that discriminate between AI skill levels

---

## 1. Bloom's Taxonomy Applied to AI Skills Testing

Bloom's Taxonomy provides a six-level cognitive hierarchy — remember, understand, apply, analyze, evaluate, create — that directly maps to the skill levels a competency test must discriminate between. "When properly developed, MCQs can access all the levels of Bloom's taxonomy except for create." — [Teaching & Learning, University of Saskatchewan](https://teaching.usask.ca/articles/2025-02-28-multichoice-questions-higher-order-thinking.php)

For AI skills testing this means:

- **Recall (Level 1–2):** Stem asks to define or recognize a term. Example: "Which of the following best describes a large language model?" These items are necessary as floor anchors but insufficient for discrimination.
- **Application (Level 3):** The test-taker must use a concept in a new context. "MCQs can assess a test-taker's ability to apply the knowledge acquired in the course to new situations." — [Teaching & Learning, University of Saskatchewan](https://teaching.usask.ca/articles/2025-02-28-multichoice-questions-higher-order-thinking.php)
- **Analysis / Evaluation (Levels 4–5):** Stems present a scenario and ask the test-taker to diagnose, compare trade-offs, or evaluate a course of action. "MCQs can tap into the cognitive process of evaluation by asking students to make judgments based on a set of guidelines." — [Teaching & Learning, University of Saskatchewan](https://teaching.usask.ca/articles/2025-02-28-multichoice-questions-higher-order-thinking.php) These are the items that reliably separate intermediate from advanced learners.

The key design shift from recall to analysis is the stem: recall stems are definitional ("What is X?"), while analysis stems are situational ("A product manager receives an AI-generated market report containing conflicting figures. Which action best addresses the risk?").

---

## 2. Item Difficulty and Discrimination Indices

Two classical statistics govern whether an item is doing useful measurement work.

**Difficulty index (p-value):** The proportion of test-takers who answered correctly. "The item difficulty index ranges from 0 to 100; the higher the value, the easier the question." — [University of Washington Assessment](https://www.washington.edu/assessment/scanning-scoring/scoring/reports/item-analysis/)

For a discriminating test (not a mastery gate), the optimal range is p = 0.30–0.70. "To maximize item discrimination, desirable difficulty levels are slightly higher than midway between chance and perfect scores for the item." — [University of Washington Assessment](https://www.washington.edu/assessment/scanning-scoring/scoring/reports/item-analysis/) For a 4-option item, chance is 0.25, so the target p is roughly 0.50–0.62.

**Discrimination index (D):** Compares correct-answer rates between the top and bottom 27% of scorers. "As a rule of thumb, .40 and greater are very good items, .30 to .39 are reasonably good but possibly subject to improvement, .20 to .29 are marginal items and need some revision, below .19 are considered poor items and need major revision or should be eliminated." — [University of Washington Assessment](https://www.washington.edu/assessment/scanning-scoring/scoring/reports/item-analysis/)

**Distractor quality** directly drives both statistics. "Whereas the discrimination value of the correct answer should be positive, the discrimination values for the distractors should be lower and, preferably, negative." — [PMC / Item analysis: distractor efficiency](https://pmc.ncbi.nlm.nih.gov/articles/PMC11040895/) Plausible distractors that attract lower-ability test-takers (common misconceptions about AI outputs, overgeneralization of model capabilities) are what give an item its discriminating power.

**Composite review:** "All the indicators — Item Discrimination Index, Item Difficulty Index, Point-Biserial Correlation, Distractor Analysis, and Kuder-Richardson 20 (KR-20) — should be examined together to gain a comprehensive understanding of how well a test functions." — [University of Washington Assessment](https://www.washington.edu/assessment/scanning-scoring/scoring/reports/item-analysis/)

---

## 3. Scenario-Based MCQ Design for AI Judgment

Scenario-based MCQs (SBMCQs) are the primary mechanism for testing judgment rather than memorization. "Scenario-based multiple-choice questions are highly compatible with competence-based assessments as they effectively target essential elements of higher-order thinking." — [Springer / International Journal of AI in Education](https://link.springer.com/article/10.1007/s40593-025-00471-z)

Design principles for AI-use scenarios:

1. **Anchor in a realistic work context.** A scenario should describe a plausible professional situation (e.g., drafting a policy with AI assistance, reviewing AI-generated code for a production system, choosing a prompt strategy for a constrained task). "Provide a detailed prompt or scenario and then ask a number of questions about it. This will allow students to apply their understanding to a specific situation." — [Teaching & Learning, University of Saskatchewan](https://teaching.usask.ca/articles/2025-02-28-multichoice-questions-higher-order-thinking.php)

2. **Embed a decision point, not a fact lookup.** The question should ask what the person *should do* or *which outcome to expect*, not what a term means.

3. **Make wrong answers diagnostic.** Each distractor should represent a specific, recognizable misconception (e.g., treating AI output as ground truth, ignoring context window limits, conflating fine-tuning with RAG). This turns incorrect responses into evidence of which specific skill gap exists.

4. **Include reasoning in answer options.** "Provide response options that represent the correct answer as well as why the answer is correct so that students must engage in a reasoning process, rather than just recall a fact." — [Teaching & Learning, University of Saskatchewan](https://teaching.usask.ca/articles/2025-02-28-multichoice-questions-higher-order-thinking.php)

5. **AIQ (AI Skills Assessment by CFTE)** provides a published model: "a mix of scenario-based questions, practical decision-making, real-world AI situations, and knowledge checks — not just multiple choice, but tests of how people think about using AI in real work and life contexts." — [CFTE AIQ](https://courses.cfte.education/aiq-ai-skills-assessment/)

---

## 4. Psychometric Best Practices for Diagnostic (Placement) Tests

A diagnostic test differs from a pass/fail test: its purpose is to locate an examinee on a skill continuum, not to clear a threshold. This requires specific design choices.

**Item Response Theory (IRT)** is the preferred framework. "IRT is a paradigm for the design, analysis, and scoring of tests measuring abilities — it is based on the relationship between individuals' performances on a test item and the test takers' levels of performance on an overall measure of the ability that item was designed to measure." — [Wikipedia: Item Response Theory](https://en.wikipedia.org/wiki/Item_response_theory)

Under the 3-parameter logistic (3PL) model, each item is characterized by:
- **a (discrimination):** How sharply the item separates ability levels; typically 0–2, higher is better.
- **b (difficulty):** The ability level at which a test-taker has a 50% chance of answering correctly; ranges −3 to +3 on the theta scale.
- **c (pseudo-guessing):** The probability a very low-ability examinee gets the item right by chance.

"The IRT models put people and items onto a latent scale called θ (theta), which represents whatever is being measured." — [IRT Intro, bookdown](https://bookdown.org/bean_jerry/using_r_for_educational_research/item-response-theory.html)

For a placement test, **items should be spread across the b-parameter range** to cover all target levels. A test with items clustered at b = 0 measures average learners well but gives imprecise scores at the extremes — exactly where level placement decisions matter most.

**Test Information Function (TIF):** The TIF aggregates item-level information across theta values. A well-designed placement battery shows high information (low measurement error) at each level boundary where a placement decision must be made, not just at the overall mean.

---

## 5. Scoring Model for Level Recommendation and Progress Baseline

**Level recommendation:** The most defensible approach combines a theta estimate (from IRT or a classical proxy) with empirically derived cut scores at each level boundary. "The boundary locations where one level becomes more likely than another are where the curves cross." — [theta-minus-b IRT textbook](https://www.thetaminusb.com/intro-measurement-r-sp/irt.html) In practice: administer a 20–30 item bank stratified by level and Bloom's level, compute theta (or a weighted sum as a classical proxy), and map theta to levels using pre-set cut points validated against learner performance data.

**Scoring methods:** Three IRT-based scoring approaches are available: Maximum Likelihood (ML), Maximum A Posteriori (MAP), and Expected A Posteriori (EAP). EAP is generally preferred for placement because it performs well with short tests and shrinks extreme estimates toward the prior distribution. — [Columbia University / IRT](https://www.publichealth.columbia.edu/research/population-health-methods/item-response-theory)

**Progress baseline:** Because IRT places both items and persons on the same theta scale, a re-test after training can be compared directly to the baseline theta, regardless of which specific items were used — provided items are calibrated on the same scale. "IRT can connect multiple levels of content, such as math curriculum from grades 3 to 12, known as vertical scaling within the progress monitoring framework." — [IRT intro, assess.com](https://assess.com/what-is-item-response-theory/)

For a practical implementation without full IRT infrastructure: assign each item a level weight (1 = recall, 2 = application, 3 = analysis), compute a weighted score by Bloom's level, and generate a profile showing strength/gap per cognitive level. Map profile patterns to starting-level recommendations using a decision rule (e.g., "if weighted application score < 50% and analysis score < 30%, recommend Level 1"). This classical approach is less precise than IRT but interpretable and auditable.

**Reliability check:** Use Kuder-Richardson 20 (KR-20) for internally consistent scoring. A KR-20 ≥ 0.70 is considered acceptable for a placement decision; ≥ 0.80 is preferred. — [University of Washington Assessment](https://www.washington.edu/assessment/scanning-scoring/scoring/reports/item-analysis/)

---

## Inferred Findings

1. **AI-specific distractor design requires domain knowledge of common AI misconceptions.** Based on: the general principle that "discrimination values for distractors should be negative" — [PMC / distractor efficiency](https://pmc.ncbi.nlm.nih.gov/articles/PMC11040895/) — and the CFTE AIQ model testing "how people think about using AI in real work contexts" — [CFTE AIQ](https://courses.cfte.education/aiq-ai-skills-assessment/). Reasoning: distractors for AI-skills items (e.g., "AI output is always factually accurate," "more tokens always improve output") must be grounded in documented user misconceptions, not generic wrong answers, to achieve negative discrimination values and genuine diagnostic power.

2. **A 30-item diagnostic battery spanning 3 Bloom's levels and 3 content domains is likely the minimum viable instrument for reliable level placement.** Based on: IRT guidance that short tests require EAP scoring to control variance — [Columbia University / IRT](https://www.publichealth.columbia.edu/research/population-health-methods/item-response-theory) — and classical test theory guidance that KR-20 ≥ 0.70 requires sufficient item count. Reasoning: with 3 levels × 3 domains × ~3 items each = 27–30 items, the test can generate both a level score and a domain-specific gap profile.

---

## Unverified Observations

- The CFTE AIQ assessment claims to test "how people think about using AI in real work and life contexts" but its specific item formats, psychometric validation data, and reliability coefficients are not publicly documented. The claim should be treated as illustrative rather than a validated benchmark.
- Some sources assert that scenario-based MCQs are superior to recall MCQs for learning outcomes as well as measurement. This learning-benefit claim has stronger support in medical education than in AI/digital skills contexts, where direct empirical studies are sparse as of April 2026.

---

## Sources

- https://teaching.usask.ca/articles/2025-02-28-multichoice-questions-higher-order-thinking.php
- https://pmc.ncbi.nlm.nih.gov/articles/PMC4511057/
- https://pmc.ncbi.nlm.nih.gov/articles/PMC11040895/
- https://www.washington.edu/assessment/scanning-scoring/scoring/reports/item-analysis/
- https://www.tmcc.edu/sites/default/files/documents/asmt-tutorial-difficulty-indices.pdf
- https://ericae.net/ft/tamu/Espy.htm
- https://en.wikipedia.org/wiki/Item_response_theory
- https://assess.com/what-is-item-response-theory/
- https://www.publichealth.columbia.edu/research/population-health-methods/item-response-theory
- https://bookdown.org/bean_jerry/using_r_for_educational_research/item-response-theory.html
- https://www.thetaminusb.com/intro-measurement-r-sp/irt.html
- https://link.springer.com/article/10.1007/s40593-025-00471-z
- https://courses.cfte.education/aiq-ai-skills-assessment/
- https://pmc.ncbi.nlm.nih.gov/articles/PMC6096460/

---
*Executed: 2026-04-30 | Mode: independent*


## Section 2 — AI-Specific Question Writing

### Prompt 2: Writing questions that distinguish AI competency levels

# Prompt 02: ai-question-writing

> **Prompt:** How to write MCQ questions that distinguish AI competency levels — with examples

---

## What Makes a Good AI Competency Question

The core challenge in writing AI skill assessments is the gap between **knowing about AI** and **knowing how to use AI well**. Most published AI literacy instruments expose this gap directly: "Many existing AI literacy scales rely on self-reporting, capturing only individuals' subjective perceptions of their AI knowledge and skills. Self-perception often deviates from real ability." — [Developing and validating measures for AI literacy tests, ScienceDirect](https://www.sciencedirect.com/science/article/pii/S2666920X24000857)

A good AI competency question therefore:
1. Tests a **decision or judgment**, not a definition
2. Places the respondent **inside a realistic scenario** rather than asking about abstract concepts
3. Has **distractors that a knowledgeable-but-unskilled person would choose** (plausible wrong answers based on partial understanding)
4. Maps to a specific **Bloom's taxonomy level**, with higher levels (Apply, Analyze, Evaluate, Create) separating intermediate/advanced users from beginners

---

## The Bloom's Taxonomy Ladder for AI Questions

Research on AI literacy assessment consistently applies Bloom's six cognitive levels to stratify question difficulty. "With generative AI now capable of handling lower-level cognitive tasks such as remembering and understanding, assessments need to challenge students to engage in higher-order thinking. Analyzing data, evaluating scenarios, and creating new solutions are tasks which AI cannot easily replicate." — [Balancing Bloom, Assessment, and AI, eSchool News](https://www.eschoolnews.com/digital-learning/2024/05/27/balancing-bloom-assessment-and-ai/)

| Bloom Level | AI Competency Target | Question Verb |
|---|---|---|
| Remember | Recall what AI tools exist, basic definitions | Identify, list, name |
| Understand | Explain what a model does, describe limitations | Explain, describe, summarize |
| Apply | Use AI correctly for a given task | Use, demonstrate, execute |
| Analyze | Spot errors, biases, or hallucinations in AI output | Compare, differentiate, examine |
| Evaluate | Judge whether AI is appropriate for a task; critique output quality | Assess, judge, justify |
| Create | Design a prompt strategy; build a human+AI workflow | Design, construct, formulate |

Beginner questions sit at Remember/Understand. Intermediate questions sit at Apply/Analyze. Advanced questions sit at Evaluate/Create.

A multi-agent MCQ generation framework validated by K-12 AI literacy experts confirms this structure: "A Multi-Agent MCQ Generation System uses learning objectives, Bloom's taxonomy levels, grade level, and specific scenarios to produce multiple-choice questions with correct options and distractors." — [Generating AI Literacy MCQs: A Multi-Agent LLM Approach, arXiv](https://arxiv.org/html/2412.00970v1)

---

## The Five Competency Domains to Cover

One widely validated framework organises AI literacy into five domains: "What is AI?, What can AI do?, How does AI work?, How should AI be used?, and How do people perceive AI?" — [Development of an AI literacy assessment for non-technical learners, ERIC](https://files.eric.ed.gov/fulltext/EJ1437452.pdf)

Questions testing **skill** (not just knowledge) live primarily in domains 3–5, where judgment, ethics, and appropriate use decisions are required.

---

## Example Question Structures by Level

### Beginner (Remember/Understand)
> *Which of the following best describes a large language model (LLM)?*
> - A) A system that searches the web and summarises results
> - B) A system trained on text data to predict likely next tokens
> - C) A database of pre-written answers to common questions
> - D) A rule-based expert system that follows if-then logic

This tests whether the respondent can correctly classify AI technology — a knowledge question. Distractors A, C, D represent common misconceptions.

### Intermediate — Applying (Apply)
> *You need to draft a legal summary of a 50-page contract. Which approach best uses an AI assistant?*
> - A) Paste the full contract and ask "summarise this"
> - B) Ask the AI to identify key clauses and obligations section by section, then review each output against the source
> - C) Ask the AI to summarise, then publish the output directly — LLMs are trained on legal text
> - D) Avoid AI entirely; legal documents are too sensitive for AI use

Correct answer: B. Tests whether the user knows to decompose tasks, verify outputs, and apply source-checking — not just whether they know AI can read text.

### Intermediate — Analyzing (Analyze / Hallucination Detection)
> *An AI assistant provides the following answer: "The EU AI Act was signed into law in March 2023, establishing a tiered risk classification system." What is the most critical first step before using this claim in a report?*
> - A) Rephrase the claim in your own words to avoid plagiarism
> - B) Cross-check the date and key facts against a primary source, as LLMs frequently confabulate specific dates
> - C) Ask the AI to confirm the claim a second time
> - D) Accept the claim — the AI was trained on EU regulatory data

Correct answer: B. Tests hallucination awareness and source verification habit. Research on hallucination evaluation shows that "a model can score high on benchmarks yet amplify stereotypes or discriminate in outputs" — [Towards trustworthy LLMs, Springer Nature](https://link.springer.com/article/10.1007/s10462-024-10896-y) — so respondents who choose C (re-querying the same AI) reveal a critical skills gap.

### Advanced — Evaluating (Evaluate / Bias Awareness)
> *Your team uses an AI tool to screen CVs for a software engineering role. The tool flags 72% of female candidates as "low fit" vs. 31% of male candidates with equivalent experience. Which of the following is the most appropriate response?*
> - A) Accept the tool's outputs — it is trained on historical hiring data, which is objective
> - B) Adjust the threshold so more female candidates pass before reviewing the tool's design
> - C) Pause use of the tool, audit the training data for historical bias, and implement human review of all screened-out candidates
> - D) Run the tool again with anonymised CVs to see if the pattern changes

Correct answer: C. Tests ability to evaluate systemic AI bias, not just spot a surface anomaly. Option D (anonymising) shows partial understanding; C shows full evaluation-level judgment about when to suspend AI use entirely.

### Advanced — Judgment About When to Use AI (Evaluate)
> *A colleague suggests automating customer complaint triage using an LLM to classify and route tickets. Which factor most critically determines whether this is appropriate without human review?*
> - A) Whether the LLM is a state-of-the-art model
> - B) Whether the complaints involve high-stakes decisions such as safety, legal rights, or financial penalties
> - C) Whether the company has a data privacy policy in place
> - D) Whether the average complaint is fewer than 500 words

Correct answer: B. Tests judgment about deployment context and risk — an advanced competency. "Effective AI integration requires students to first master foundational skills… students cannot meaningfully engage AI for higher-order critical evaluation without first independently mastering the lower-level analytical and synthesis skills." — [OLC Insights: Bloom's for AI Adoption](https://onlinelearningconsortium.org/olc-insights/2025/10/blooms-for-ai-adoption/)

---

## Writing Rubric for AI Skill Questions

Based on the ten-item rubric used by AI literacy experts in published MCQ research — [arXiv 2412.00970](https://arxiv.org/html/2412.00970v1) — and instrument development best practices, a good AI skill question should meet all of:

1. **Scenario-grounded**: The stem describes a realistic work context, not a definition request
2. **Skill-targeting**: The correct answer requires doing something, not just recalling something
3. **Discriminating distractors**: Each wrong answer reflects a real misconception or partial knowledge gap — not an obviously absurd option
4. **Single defensible answer**: Only one option is clearly correct given the scenario
5. **Bloom-labelled**: The question is consciously placed at the intended cognitive level
6. **Source-independent**: The question does not depend on knowing a specific tool's UI — it tests transferable judgment

---

## Inferred Findings

**Inference 1: Re-querying the same AI as a verification strategy is a reliable "skill gap" distractor** across multiple question types.
- Based on: ["Towards trustworthy LLMs, Springer Nature"](https://link.springer.com/article/10.1007/s10462-024-10896-y) (LLMs confabulate consistently across queries); ["Developing and validating AI literacy measures, ScienceDirect"](https://www.sciencedirect.com/science/article/pii/S2666920X24000857) (self-perception deviates from real skill)
- Reasoning: A beginner who believes AI outputs are accurate will re-query the same model to "double-check." This pattern appears as a plausible distractor because it mirrors something a careful person might do — but it demonstrates failure to understand that the same model will produce the same type of error.

**Inference 2: The Apply→Analyze transition (intermediate zone) is the most diagnostically valuable band for workplace AI assessments**, because this is where prompt decomposition, output verification, and hallucination-checking habits appear — skills that define practical productivity with AI tools.
- Based on: [eSchool News: Balancing Bloom and AI](https://www.eschoolnews.com/digital-learning/2024/05/27/balancing-bloom-assessment-and-ai/); [arXiv multi-agent MCQ system](https://arxiv.org/html/2412.00970v1)
- Reasoning: Bloom's levels 1–2 (recall/understand) are easily handled by anyone who has read an AI explainer. Levels 5–6 (evaluate/create) require extended work samples. Levels 3–4 (apply/analyze) are assessable via MCQ and represent the skills that differentiate daily AI users who are effective from those who are not.

## Unverified Observations

- The GLAT (Generative AI Literacy Assessment Test, arXiv 2411.00283) is cited as a validated 20-item instrument with structural validity confirmed by both classical test theory and item response theory. The full item bank was not accessible for review in this research session, so individual question examples cannot be cited directly.
- The MAILS (Meta AI Literacy Scale, arXiv 2302.09319) includes self-assessment items that can be cross-referenced with performance-based items to measure the gap between perceived and actual skill — a potentially useful calibration technique for multi-level assessments.

---

## Sources

- https://arxiv.org/html/2412.00970v1
- https://arxiv.org/html/2411.00283v1
- https://www.sciencedirect.com/science/article/pii/S2666920X24000857
- https://files.eric.ed.gov/fulltext/EJ1437452.pdf
- https://www.nature.com/articles/s41539-024-00264-4
- https://pmc.ncbi.nlm.nih.gov/articles/PMC11303566/
- https://bera-journals.onlinelibrary.wiley.com/doi/full/10.1111/bjet.13411
- https://link.springer.com/article/10.1007/s10462-024-10896-y
- https://www.eschoolnews.com/digital-learning/2024/05/27/balancing-bloom-assessment-and-ai/
- https://onlinelearningconsortium.org/olc-insights/2025/10/blooms-for-ai-adoption/
- https://ecampus.oregonstate.edu/faculty/artificial-intelligence-tools/blooms-taxonomy-revisited/

---
*Executed: 2026-04-30 | Mode: independent*


## Section 3 — Actionable Design Guidelines (Synthesis)

### Prompt 3: Concrete recommendations for the web test

# Prompt 03: actionable-design-guidelines

> **Prompt:** Actionable guidelines for designing the web-based AI competency test

---

## (a) Recommended Test Structure

**Total item count: 24 questions** across three levels and two diagnostic dimensions (breadth and depth).

| Level | Bloom's Targets | Item Count | Rationale |
|---|---|---|---|
| Beginner | Remember / Understand | 6 | Anchor floor; fast to complete; screens true novices |
| Intermediate | Apply / Analyze | 12 | Highest-value diagnostic band (Prompt 2); double weight |
| Advanced | Evaluate / (judgment proxy for Create) | 6 | Ceiling anchor; separates high performers |

The 2:1 weighting toward Intermediate is deliberate. The Apply/Analyze transition is where self-reported literacy diverges most sharply from demonstrated skill (Prompt 2), making it the richest source of placement signal. Beginner and Advanced items serve primarily as boundary anchors for the IRT Test Information Function, which should peak at the Beginner/Intermediate and Intermediate/Advanced cut-score theta values rather than at extreme ends of the scale (Prompt 1).

**Dimensional coverage:** Within each level, distribute items across at least three AI skill dimensions (e.g., task decomposition, output evaluation, bias/risk judgment, tool selection). No single dimension should account for more than 40% of items at any level. This guards against narrow construct coverage inflating or deflating a participant's apparent level.

**Target completion time: 20–25 minutes.** At approximately 60–90 seconds per item this is achievable without time pressure, which is important because advanced items use longer situational stems.

---

## (b) Question Format Specification

**Stem type by level:**

- Beginner items: short definitional or classification stems (1–3 sentences). Example archetype: classify AI output type, identify a term. These test Remember/Understand as standalone propositions (Prompt 2, archetype 1).
- Intermediate items: situational stems with an embedded decision point (3–6 sentences). The stem must describe a realistic workplace scenario — a task handed to a colleague, a generated output to review, a workflow to configure — and ask what the test-taker would do or what the output reveals. This mirrors the five archetypes in Prompt 2 (task decomposition, hallucination detection) and satisfies the 6-criterion rubric requirement for scenario-grounding.
- Advanced items: multi-constraint situational stems (5–8 sentences) presenting competing considerations — accuracy vs. speed, auditability vs. efficiency, bias risk vs. business need — and asking for a reasoned selection or judgment call. These correspond to the bias-auditing/suspension and deployment-judgment archetypes (Prompt 2).

**Distractor design rules (apply to all levels):**

1. All four options must be plausible given the stem context. Eliminate any distractor that a naive reader would immediately discard.
2. At least two distractors should represent common practitioner errors, not absurd alternatives. For Intermediate/Advanced items, common errors include over-trusting fluent-sounding AI output, conflating AI confidence with accuracy, and ignoring auditability requirements.
3. Distractors must not overlap in meaning. If two options could both be defended as partially correct, rewrite or collapse them.
4. Avoid "all of the above" and "none of the above" — these inflate guessing advantage and reduce discrimination.
5. The single defensible answer must be defensible by reference to a principle or practice, not by elimination (Prompt 2, criterion 4).

**Stem length discipline:** Cap beginner stems at 60 words, intermediate at 120 words, advanced at 200 words. Longer stems at lower levels penalise reading speed rather than AI competency.

---

## (c) Scoring and Reporting Logic

**Preferred model: IRT 3PL.** Each item is parameterised with discrimination (a), difficulty (b), and guessing (c) values estimated from pilot data. EAP (Expected A Posteriori) scoring is used to convert response patterns to a theta estimate, which is then mapped to three level bands via pre-set cut scores at the Beginner/Intermediate and Intermediate/Advanced theta boundaries (Prompt 1).

**Classical proxy (pre-pilot phase):** Until IRT parameters are available from a pilot sample, use Bloom's-weighted scoring: Remember/Understand items weight 1 point each; Apply/Analyze items weight 1.5 points each; Evaluate items weight 2 points each. Apply a decision rule: score ≥ 85% of Intermediate+Advanced weighted points → Advanced; score ≥ 60% → Intermediate; below → Beginner. This is a temporary proxy, not a validated placement model.

**Reported output to the test-taker:**

- Level diagnosis: Beginner / Intermediate / Advanced with a one-sentence plain-language description of what that means for workplace AI use.
- Dimensional profile: a radar or bar chart showing performance across the 3–4 skill dimensions, so the participant can see whether they are strong in task decomposition but weak in bias/risk judgment, for example.
- Progress baseline: the theta score (or weighted proxy score) is stored with a timestamp so it can be compared to a re-test score after training, enabling direct pre/post measurement on the same scale (Prompt 1).

Do not report raw item scores or reveal which items were answered incorrectly, to preserve item security for re-testing.

---

## (d) Validation Approach — Minimum Viable Pilot

**Sample requirement:** 150–200 completed responses before treating IRT parameters as stable. This is the practical lower bound for 3PL estimation with 24 items. Aim for roughly equal representation across the three target levels (confirm level via manager nomination or a brief job-task inventory, not self-report).

**Step-by-step pilot process:**

1. **Expert review (pre-pilot):** Have 3–5 subject-matter experts independently identify the keyed answer and Bloom's label for each item. Flag any item where fewer than 4 of 5 experts agree on the key.
2. **Cognitive interview (n=8–10):** Ask participants to think aloud while completing the test. Identify stems that are misread, distractors that are ambiguous, or scenario contexts that feel implausible. Revise before main pilot.
3. **Main pilot (n=150–200):** Collect response data. Compute classical item statistics first: flag items with p < 0.20 or p > 0.90 (too hard or too easy), and D < 0.20 (poor discrimination) (Prompt 1). Remove or revise flagged items before IRT calibration.
4. **IRT calibration:** Fit 3PL model. Confirm KR-20 ≥ 0.70 for the full bank and ≥ 0.65 for each level sub-bank (Prompt 1). Plot Test Information Function and verify peaks at cut-score theta values.
5. **Cut-score setting:** Use a modified Angoff procedure with 5–7 subject-matter experts to set the two cut scores, then cross-validate against manager-rated performance on the pilot sample.
6. **Launch readiness gate:** Proceed only if KR-20 ≥ 0.70, all retained items have D ≥ 0.25, and the two cut scores correctly classify ≥ 75% of pilot participants versus manager nominations.

---

## (e) Adaptive Testing Consideration

**Recommendation: implement a lightweight routing rule, not full computerised adaptive testing (CAT), for the initial launch.**

Full CAT requires a calibrated item bank of 80–120 items and stable IRT parameters — neither is available at launch. However, a two-stage routing design is feasible immediately:

- Stage 1: all participants answer the 12 Intermediate items first (the highest-value diagnostic band, Prompt 2). Estimated time: 12–15 minutes.
- Stage 2 routing: participants who score in the bottom third of Stage 1 receive the 6 Beginner items; those in the top third receive the 6 Advanced items; the middle third receives a balanced 3+3 mix. This preserves 24 total items while concentrating measurement precision where the boundary is unclear.

This design reduces floor/ceiling waste, shortens the effective test for clear Beginner and clear Advanced participants, and requires no CAT engine — just a simple score threshold applied after Stage 1 submission. It can be implemented with standard branching logic in any web assessment platform.

After the pilot generates stable IRT parameters and the item bank expands to 60+ items, migrate to true CAT to maximise precision per item.

---

## Inferred Findings

**IF-1: Bloom's-weighted classical scoring is a viable temporary proxy for IRT theta placement.**
Based on: Prompt 1 (classical proxy described as Bloom's-weighted score → profile → decision rule; IRT preferred but classical acceptable) and Prompt 2 (Bloom's stratification is well-specified with clear level boundaries).
Reasoning: Both prompts independently specify Bloom's taxonomy as the structural backbone. If the level boundaries are already defined by Bloom's labels, a weighted scoring rule that mirrors those labels will approximate IRT-based placement with acceptable accuracy for a pre-pilot phase, even though it cannot provide direct pre/post comparison on a theta scale.

**IF-2: The Apply/Analyze band should carry double item weight to maximise diagnostic value for the target population (workplace AI users).**
Based on: Prompt 2 (Apply/Analyze is the highest-value diagnostic band; self-reported literacy diverges from actual skill most sharply here) and Prompt 1 (Test Information Function should peak at level-boundary theta values, not at extremes).
Reasoning: If the TIF should peak at boundaries, and the most practically important boundary is Beginner/Intermediate (where false self-assessments cluster), then concentrating items at that boundary — which means Apply/Analyze — directly serves both psychometric and practical goals simultaneously.

**IF-3: A two-stage routing design is preferable to flat-form administration even before full CAT is viable.**
Based on: Prompt 1 (IRT TIF should peak at cut-score thetas; items far from cut-score thetas contribute little measurement information) and Prompt 2 (Apply/Analyze is the highest-value band, implying beginner and advanced items have lower diagnostic yield for typical workplace populations).
Reasoning: If items at the extremes contribute less measurement information for the majority of test-takers, then administering them uniformly wastes completion time and increases dropout risk on a web-based assessment. Routing solves this without requiring a full CAT infrastructure.

---

## Unverified Observations

- A 20–25 minute completion time is assumed to be acceptable for a voluntary workplace assessment. This has not been validated against dropout rates or engagement data for this specific population; if completion rates fall below 70% in piloting, consider trimming to 18 items with a 15-minute target.
- The 150–200 pilot sample threshold for 3PL stability is a standard rule of thumb from applied psychometrics literature; the actual minimum depends on item parameter variability and may be lower for a constrained 24-item bank.

---

## Sources

No external URLs were consulted in this synthesis. All findings derive from Prompt 1 (MCQ design principles) and Prompt 2 (AI question writing), treated as prior research outputs.

---

*Executed: 2026-04-30 | Mode: sequential*
