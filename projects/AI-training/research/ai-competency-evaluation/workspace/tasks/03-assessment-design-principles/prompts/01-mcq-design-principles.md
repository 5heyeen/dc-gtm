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
