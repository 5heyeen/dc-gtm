# Prompt 01: framework-and-blueprint

> **Prompt:** Test overview, competency framework, item blueprint, question format, and scoring architecture

---

## Section 1: Test Overview

| Field | Detail |
|---|---|
| **Test Name** | AI Competency Assessment (ACA) |
| **Purpose** | Diagnose individual AI literacy level across six competency dimensions; establish a theta baseline for pre/post measurement of training effectiveness |
| **Audience Tiers** | Tier 1: Professionals new to AI (primary); Tier 2: Mid-level practitioners with informal AI exposure; Tier 3: Technical professionals requiring advanced calibration |
| **Total Items** | 24 (12 Stage 1 Intermediate + 6 Stage 2 routed items) |
| **Duration** | 20–25 minutes |
| **Delivery Format** | Adaptive two-stage digital assessment; browser-based; no specialist software required |
| **EU AI Act Relevance** | Article 4 of the EU AI Act (enforcement August 2026) requires organisations deploying AI systems to ensure staff possess adequate AI literacy. This assessment provides a documented, auditable baseline measure of that literacy, supporting compliance demonstration and gap-targeted training plans. |

---

## Section 2: Competency Framework Table

| Dimension | Beginner (Remember / Understand) | Intermediate (Apply / Analyze) | Advanced (Evaluate) | Expert (Create / Strategise) | Audience Tag |
|---|---|---|---|---|---|
| **1. Conceptual Understanding** | Defines core AI/ML terms (e.g., model, training data, hallucination). Distinguishes AI from traditional software. | Explains how a specific AI output was produced given a known model type. Identifies which AI approach fits a described business problem. | Evaluates trade-offs between AI architectures for a given use-case context. Critiques claims made about AI capabilities in vendor materials. | Designs a conceptual AI systems roadmap for an organisation. Synthesises cross-domain AI concepts into novel frameworks. | Both |
| **2. Prompt Literacy / Applied Use** | Recognises what makes a prompt clear vs. ambiguous. Reproduces a basic prompt structure given an example. | Applies prompt engineering techniques (role, context, constraints) to improve output quality. Iterates a prompt chain to accomplish a multi-step task. | Evaluates prompt designs against quality criteria (accuracy, safety, efficiency). Diagnoses failure modes in a given prompt sequence. | Creates reusable prompt libraries and governance standards. Strategises prompt architecture for enterprise-scale deployment. | Non-Technical |
| **3. Critical Evaluation** | Identifies obvious AI errors or fabricated facts in a short output. Recognises that AI outputs require human review. | Analyses an AI-generated document to surface subtle inaccuracies and bias indicators. Applies a structured checklist to evaluate output reliability. | Evaluates conflicting AI outputs using evidence-based criteria. Designs a repeatable quality-assurance protocol for AI-assisted work. | Establishes organisational standards for AI output validation. Creates audit frameworks for continuous AI output quality monitoring. | Both |
| **4. Ethics & Responsibility** | Names key AI risk categories (bias, privacy, transparency). Identifies a scenario involving inappropriate AI use. | Applies an ethical framework to a realistic workplace AI dilemma. Analyses a dataset for potential bias sources and their downstream effects. | Evaluates an AI deployment against regulatory requirements (including EU AI Act). Assesses trade-offs between business value and ethical risk in a deployment decision. | Designs an organisational AI ethics policy with enforcement mechanisms. Strategises stakeholder engagement for responsible AI governance. | Both |
| **5. Workflow Integration** | Describes where AI tools could assist in a familiar workflow. Recognises manual steps that are suitable vs. unsuitable for AI automation. | Applies an AI tool to streamline a described multi-step professional workflow. Maps human–AI handoff points and identifies appropriate checkpoints. | Evaluates the productivity impact and failure risks of an AI-integrated workflow design. Diagnoses bottlenecks and redesign options in an existing AI-augmented process. | Creates a change-management plan for AI integration across a business unit. Strategises workforce capability development alongside AI adoption. | Non-Technical |
| **6. Agentic AI & Orchestration** | Defines what an AI agent is and how it differs from a single-prompt interaction. Recognises examples of agentic behaviour (tool use, planning, memory). | Applies knowledge of agentic system components to trace an agent's decision path through a described scenario. Identifies failure points in a multi-agent pipeline. | Evaluates the risks and oversight requirements for deploying an autonomous AI agent in a business context. Assesses orchestration designs for reliability and safety. | Designs a multi-agent orchestration architecture for a complex organisational problem. Creates governance and monitoring standards for agentic AI systems. | Technical |

---

## Section 3: Item Blueprint

### Distribution Table

| Dimension | Beginner Items | Intermediate Items | Advanced Items | Dimension Total |
|---|---|---|---|---|
| 1. Conceptual Understanding | 1 | 2 | 1 | 4 |
| 2. Prompt Literacy / Applied Use | 1 | 2 | 1 | 4 |
| 3. Critical Evaluation | 1 | 2 | 1 | 4 |
| 4. Ethics & Responsibility | 1 | 2 | 1 | 4 |
| 5. Workflow Integration | 1 | 2 | 1 | 4 |
| 6. Agentic AI & Orchestration | 1 | 2 | 1 | 4 |
| **Total** | **6** | **12** | **6** | **24** |

### Distribution Rationale

- **Intermediate = 12 items (50%):** Stage 1 uses all 12 Intermediate items for every test-taker. These items sit at Bloom's Apply/Analyze — the pivot level that separates passive awareness from demonstrated use. A 12-item Stage 1 provides sufficient signal (6 dimensions × 2 items each) for reliable routing with a short test duration.
- **Beginner = 6 items (25%):** Routed to test-takers who score below the Stage 1 cut-score. One item per dimension confirms foundational knowledge and produces a diagnostic profile, not merely a failure flag. Low item count is intentional — Beginner items carry lower information value for the target audience.
- **Advanced = 6 items (25%):** Routed to test-takers who meet or exceed the Stage 1 cut-score. One item per dimension probes Evaluate-level capability. Equal count with Beginner maintains symmetry in total test length across routes (18 items per test-taker).
- **Expert level:** Not assessed in the current instrument. Expert descriptors in the competency framework serve as curriculum targets and role-profile anchors, not test items.

---

## Section 4: Question Format Specification

### Beginner Items (Remember / Understand)

| Parameter | Specification |
|---|---|
| **Stem type** | Single-concept recognition or definition recall. Short scenario (1–2 sentences) or direct question. |
| **Format** | Four-option single-select MCQ |
| **Scenario length** | ≤ 40 words |
| **Distractor rules** | 1 clearly wrong distractor (confidence anchor); 2 plausible distractors based on common misconceptions identified in prior research; 1 correct answer. Distractors must not use negation ("which is NOT") as the sole discriminator. |
| **Example stem pattern** | "A colleague says the AI 'made up' a citation that doesn't exist. Which term best describes this behaviour?" |

### Intermediate Items (Apply / Analyze)

| Parameter | Specification |
|---|---|
| **Stem type** | Situated workplace scenario requiring the test-taker to apply a concept or analyse a presented output/situation. |
| **Format** | Four-option single-select MCQ; one extended-scenario anchor per dimension permitted (shared stem with 2 items) |
| **Scenario length** | 60–120 words |
| **Distractor rules** | All 3 distractors must be plausible actions or interpretations a non-expert would genuinely consider. No distractor may be obviously absurd. At least 1 distractor must represent a common but ineffective AI practice (e.g., accepting output without review, over-specifying a prompt). Correct answer must require application or analysis, not mere recall. |
| **Example stem pattern** | "You have used an AI assistant to draft a regulatory summary. The output reads fluently but cites a regulation you cannot find. What is the most appropriate next step?" |

### Advanced Items (Evaluate)

| Parameter | Specification |
|---|---|
| **Stem type** | Complex, multi-variable scenario requiring the test-taker to evaluate competing options, weigh trade-offs, or critique a design/decision. |
| **Format** | Four-option single-select MCQ with extended scenario; or structured best-answer item where all options are partially correct and the test-taker must select the most defensible answer. |
| **Scenario length** | 100–180 words |
| **Distractor rules** | All options must represent defensible positions; discrimination comes from depth of reasoning, not factual error. Each distractor must fail on a specific evaluative criterion (e.g., ignores risk, lacks proportionality, conflates two standards). The correct answer must be justifiable by explicit reference to a principle, standard, or evidence pattern — not merely "best practice" intuition. |
| **Example stem pattern** | "An organisation plans to deploy a generative AI tool to support HR screening of job applications. A risk review identifies three concerns: [list]. The CISO recommends full deployment deferral; the HR Director proposes proceeding with enhanced monitoring. Which response best balances EU AI Act compliance obligations with operational need?" |

---

## Section 5: Scoring Architecture

### Two-Stage Routing Logic

```
Stage 1 (All test-takers)
  └── 12 Intermediate items (2 per dimension)
  └── Weighted Stage 1 Score = sum of (items correct × 1.5 pts each)
  └── Maximum Stage 1 Score = 18 pts

Routing Decision (applied after Stage 1)
  ├── Score < 9 pts  (< 50% of max)  → Route to Stage 2-B (Beginner track)
  └── Score ≥ 9 pts  (≥ 50% of max)  → Route to Stage 2-A (Advanced track)

Stage 2-B — Beginner Track
  └── 6 Beginner items (1 per dimension)
  └── Weighted Stage 2-B Score = sum of (items correct × 1.0 pt each)
  └── Maximum Stage 2-B Score = 6 pts

Stage 2-A — Advanced Track
  └── 6 Advanced items (1 per dimension)
  └── Weighted Stage 2-A Score = sum of (items correct × 2.0 pts each)
  └── Maximum Stage 2-A Score = 12 pts
```

### Bloom's-Weighted Total Score Formula

**For Beginner-routed test-takers:**

> Total Score = (Stage 1 correct × 1.5) + (Stage 2-B correct × 1.0)
> Maximum = 18 + 6 = **24 pts**

**For Advanced-routed test-takers:**

> Total Score = (Stage 1 correct × 1.5) + (Stage 2-A correct × 2.0)
> Maximum = 18 + 12 = **30 pts**

Note: The unequal maximums are intentional. Total scores are converted to a standardised 0–100 scale for reporting. The weighting reflects Bloom's principle that higher-order skills carry greater epistemic value.

**Standardised Score:**

> Standardised Score = (Total Score / Maximum Score for route) × 100

### Level Diagnosis Thresholds (Standardised Score)

| Standardised Score | Diagnosed Level |
|---|---|
| 0–39 | Beginner |
| 40–64 | Intermediate |
| 65–84 | Advanced |
| 85–100 | Expert (flag for qualitative confirmation) |

### IRT Migration Path

- **Pilot phase (cohorts 1–3, target n ≥ 150):** Collect response data using classical scoring. Retain item-level response vectors for all test-takers.
- **Calibration phase:** Fit a 3-Parameter Logistic (3PL) IRT model per item, estimating discrimination (a), difficulty (b), and pseudo-guessing (c) parameters. Flag items with a < 0.5 (poor discrimination) or c > 0.25 (excessive guessing) for revision.
- **Theta estimation:** Replace classical total scores with individual theta (θ) estimates on the standard normal IRT scale (mean 0, SD 1). Theta values stored as longitudinal baseline for pre/post measurement of training impact.
- **Adaptive routing refinement:** Post-calibration, the Stage 1 cut-score may be replaced with a provisional theta threshold (θ = 0.0) derived from IRT, rather than the classical 50% cut.

### Output Format

Each completed assessment produces:

1. **Level Diagnosis** — One of four levels with standardised score and confidence band.
2. **Dimensional Radar Chart** — Six-axis chart showing proportion-correct per dimension (Stage 1 + Stage 2 combined), enabling identification of uneven profiles.
3. **Stored Theta Baseline** — IRT theta estimate (post-calibration) or standardised score proxy (pilot phase), stored per individual for pre/post comparison.
4. **Gap Summary** — Narrative flag of the two lowest-scoring dimensions with mapped recommended training priorities.

---

## Inferred Findings

- The equal 1-item-per-dimension allocation in Stage 2 (both routes) is an inference from the constraint of 6 items per route across 6 dimensions. This is the minimum viable allocation for dimensional diagnosis; it limits within-dimension reliability at Stage 2 and should be monitored during pilot. (Inferred from test spec parameters and measurement design principles — not explicitly stated in prior research tasks.)
- The Beginner-route maximum of 24 pts vs. Advanced-route maximum of 30 pts creates a non-equivalent scale that requires standardisation before level thresholds can be applied uniformly. The formula above addresses this, but the threshold values in the Level Diagnosis table should be treated as provisional pending empirical pilot data. (Inferred.)
- Expert level items are excluded from the active assessment on the inference that the primary audience (professionals new to AI) will not reach Expert performance at scale in the near term, and that Expert-level item development requires substantially more resource per item. (Inferred from audience description.)

## Unverified Observations

- The routing cut-score of 50% of Stage 1 maximum (9/18 pts) is a provisional design choice. Optimal cut-scores for two-stage adaptive tests are typically set empirically using conditional standard error of measurement data from pilot runs. The 50% threshold has not been validated against the specific item pool. (Unverified — pending pilot.)
- EU AI Act Article 4 enforcement is cited as August 2026. Regulatory guidance on what constitutes "adequate AI literacy" under Article 4 had not been finalised at the time of this research. The mapping of this assessment to Article 4 compliance is therefore based on the plain text of the regulation, not on implementing guidance. (Unverified — regulatory guidance status.)

## Sources

- Prior research tasks 01–05 (AI competency framework synthesis, audience analysis, Bloom's taxonomy alignment, test specification parameters, EU AI Act Article 4 context)

---
*Executed: 2026-04-30 | Mode: sequential*
