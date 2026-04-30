# Research: Test Architecture & Scoring Model

**Prompt chain:** tasks/06-test-architecture/prompt-chain.md
**Executed:** 2026-04-30
**Prompts executed:** 2 (sequential — synthesises Tasks 01–05)

---

## Part 1 — Framework, Blueprint & Scoring Architecture

### Test Overview, Competency Framework, Item Blueprint, Question Format, Scoring Model

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


---

## Part 2 — Sample Questions, Validation & Implementation

### Sample Question Bank, Validation Roadmap, Implementation Notes

# Prompt 02: sample-questions-and-validation

> **Prompt:** Sample question bank (6 questions), validation roadmap, and implementation notes

---

## Section 6: Sample Question Bank

Each question is labelled with dimension, level, Bloom's verb, correct answer, and distractor rationale.

---

### Q1 — Dimension 1: Conceptual Understanding | Level: Beginner | Bloom's: Identify

**Scenario (38 words):**
Your colleague says "the AI just made something up about our company's Q3 revenue." Which term best describes this type of AI error?

**Options:**
- A) Overfitting
- B) Hallucination
- C) Prompt injection
- D) Temperature spike

**Correct answer:** B

**Explanation:** When a generative AI model produces plausible-sounding but factually incorrect content, this is called hallucination — a well-established term in LLM literature.

**Distractor rationale:**
- A) Overfitting — plausible misconception; learners who have heard ML terminology but confuse training-time errors with inference-time errors
- C) Prompt injection — plausible for learners who have heard about AI security issues but conflate attack vectors with output errors
- D) Temperature spike — invented-sounding but attractive to learners who have encountered the "temperature" parameter and assume high temperature = errors

---

### Q2 — Dimension 2: Prompt Literacy / Applied Use | Level: Intermediate | Bloom's: Apply

**Scenario (95 words):**
You are drafting a tender response for a large public-sector client. You ask Claude to write the executive summary, but the first draft is too generic — it doesn't mention your firm's specific methodology or the client's stated priorities from the brief. Which prompt modification is most likely to produce a significantly better result on the next attempt?

**Options:**
- A) Add "Be more specific and professional" at the end of your prompt
- B) Increase the output length limit to 2000 words
- C) Provide a 3-sentence description of your firm's methodology and paste in the two key sentences from the client brief that state their priorities
- D) Switch from Claude to ChatGPT and repeat the same prompt

**Correct answer:** C

**Explanation:** Providing concrete context (methodology description + client priority quotes) directly addresses the cause of the generic output — missing specifics. This applies the "context injection" principle at the Intermediate level.

**Distractor rationale:**
- A) Vague instruction to "be more specific" — the most common beginner error: asking the model to fix a problem without giving it the information needed to do so
- B) Longer output — common misconception that output length correlates with output quality
- D) Switching models — common workaround behaviour; tests whether learner understands that prompt quality, not model choice, is the limiting factor here

---

### Q3 — Dimension 3: Critical Evaluation | Level: Intermediate | Bloom's: Analyse

**Scenario (110 words):**
You ask an AI assistant to summarise a 40-page regulatory report. The summary is well-written and covers five key themes. You notice the summary includes this sentence: "The report recommends a mandatory 30-day notification period for all AI system changes." You search the original document and cannot find this exact requirement — the report discusses notification timelines but gives no specific figure.

What should you do before sharing this summary with a client?

**Options:**
- A) Delete only that sentence and share the rest — the other content looks accurate
- B) Add a disclaimer saying "AI-generated summary" and share as-is
- C) Treat the unverified sentence as a potential hallucination, search the original for the actual requirement, and correct or remove the figure before sharing
- D) Ask the AI to regenerate the summary with a higher accuracy setting

**Correct answer:** C

**Explanation:** A specific numeric claim not found in the source document is a classic hallucination signal. The correct response is to verify against the source and correct — not to assume surrounding content is valid just because one item is suspect.

**Distractor rationale:**
- A) Partial fix without re-checking — intermediate-level error: assumes isolated hallucination rather than considering other unverified claims
- B) Disclaimer-and-share — a common but inadequate response; tests whether learner understands that a disclaimer does not transfer accuracy responsibility
- D) "Higher accuracy setting" — does not exist; tests whether learner knows that regenerating with the same prompt is not a verification method

---

### Q4 — Dimension 4: Ethics & Responsibility | Level: Beginner | Bloom's: Identify

**Scenario (55 words):**
A project manager at a Norwegian consulting firm wants to paste a client's full contract (including company name, project budget, and contact details) into ChatGPT to generate a project risk summary. What is the primary concern with this approach?

**Options:**
- A) ChatGPT will produce a lower-quality summary than a specialist tool
- B) The output may be too long to read efficiently
- C) Sharing identifiable client data with a third-party AI service may violate GDPR and the client's confidentiality agreement
- D) The contract language will confuse the AI

**Correct answer:** C

**Explanation:** Pasting identifiable personal and commercial data into a consumer AI service raises clear GDPR and confidentiality concerns — a foundational AI ethics competency for any professional.

**Distractor rationale:**
- A) Quality concern — plausible distraction; tests whether learner prioritises ethics over performance
- B) Length concern — irrelevant; tests whether learner can identify the correct type of risk
- D) AI comprehension — common assumption that formal language is problematic for AI; tests misconceptions about LLM capability

---

### Q5 — Dimension 5: Workflow Integration | Level: Advanced | Bloom's: Evaluate

**Scenario (155 words):**
Your team has been using an AI assistant for three months to draft client status reports. The team lead wants to make this the standard process. A junior team member raises a concern: "The AI sometimes gets the timeline details wrong because it doesn't have access to our project management system."

You are evaluating two proposed solutions:
- **Option A:** Connect the AI to your project management system via an API integration so it can pull live data
- **Option B:** Keep the current process but add a mandatory human review step where the report author checks all dates and milestones against the system before sending

Which response best evaluates the trade-offs between these options?

**Options:**
- A) Option A is always better — automation reduces human error
- B) Option B is always better — human review catches all errors
- C) Option A reduces errors at scale but introduces API maintenance overhead and data security scope; Option B is lower risk to implement but creates a review bottleneck as volume grows — the right choice depends on report volume and available technical resources
- D) Neither option addresses the root cause; the AI should be replaced with a specialist project reporting tool

**Correct answer:** C

**Explanation:** An Advanced-level response recognises that both options have legitimate trade-offs and frames the decision in terms of scale, risk, and resource constraints — rather than defaulting to either automation or human oversight as universally superior.

**Distractor rationale:**
- A) "Automation always wins" — a common intermediate-to-advanced misconception; tests overconfidence in AI automation
- B) "Human review always wins" — the opposite bias; tests whether learner can move beyond reflexive caution
- D) Replace the tool — a judgment-avoidance response; tests whether learner can evaluate the given options rather than reframe the question

---

### Q6 — Dimension 6: Agentic AI & Orchestration | Level: Intermediate | Bloom's: Apply

**Scenario (100 words):**
You are setting up an AI agent to help your team monitor competitor websites weekly and summarise changes in their service offerings. The agent uses a web browsing tool and a summarisation tool. During testing, the agent successfully fetches pages and writes summaries — but sometimes it fetches the same page multiple times in one run, inflating your API costs.

Which agent design change most directly addresses this problem?

**Options:**
- A) Use a more capable model — it will fetch pages more efficiently
- B) Add a memory or state-tracking component that records which URLs have already been fetched in the current run
- C) Increase the agent's temperature to reduce repetition
- D) Switch from an agent architecture to a single long prompt

**Correct answer:** B

**Explanation:** Repeated fetching is a state management problem — the agent lacks memory of what it has already done in the current session. Adding a visited-URL tracker (a simple form of agent memory) directly solves this.

**Distractor rationale:**
- A) More capable model — common misconception that model capability solves architecture problems; tests whether learner understands that agent reliability is a design concern, not a model-size concern
- C) Temperature adjustment — plausible to learners who associate temperature with repetition in text generation, but this is an architectural/memory issue, not a sampling parameter issue
- D) Single prompt — a regression to non-agentic design; tests whether learner understands when agent architecture is appropriate

---

## Section 7: Validation Roadmap

### Step 1 — Expert Review
- **Who:** 3–5 subject-matter experts: 1 AI literacy researcher, 1 L&D psychometrician, 1 senior AI practitioner (technical), 1 non-technical professional who regularly uses AI tools
- **Method:** Each expert reviews every item independently against the 6-criterion rubric (scenario-grounded, skill-targeting, discriminating distractors, single defensible answer, Bloom-labelled, source-independent)
- **Criteria:** Items with < 3/5 expert approval are revised or culled. All correct answers must achieve 100% expert agreement. Any distractor rated "implausible" by ≥ 2 experts is replaced.
- **Output:** Revised 30-item pool (6 extra items as reserves to replace culled items post-pilot)

### Step 2 — Cognitive Interviews
- **Who:** 8–12 participants spanning the target audience range (mix of non-technical professionals and technical practitioners)
- **Protocol:** Think-aloud protocol — participants read each question and verbalise their reasoning. Facilitator probes: "What does this question ask you to do?" / "What made you choose that answer?"
- **Criteria:** Flag any item where ≥ 2 participants misread the question intent, find the scenario unrealistic, or cannot distinguish between two answer options on clear grounds
- **Output:** Revised items with improved clarity; any irredeemably ambiguous items replaced from reserves

### Step 3 — Pilot Administration
- **Who:** n = 150–200 participants, stratified by role (≥ 40 non-technical professionals, ≥ 40 technical practitioners, remainder mixed)
- **Recruitment:** Internal networks, partner organisations, LinkedIn outreach — voluntary, no incentive required for this phase
- **Platform:** Online delivery, timed (25-minute limit enforced), randomised item order within each stage, no feedback shown during administration
- **Data collected:** Item responses, time-on-task per item, completion rate, dropout point

### Step 4 — Classical Item Analysis
| Metric | Threshold | Action if fails |
|--------|-----------|-----------------|
| Difficulty (p) | 0.20–0.90 | Flag for review; items p < 0.10 or p > 0.95 are culled |
| Discrimination (D) | ≥ 0.20 (acceptable), ≥ 0.40 (good) | Items D < 0.20 are replaced |
| Distractor uptake | Each wrong option chosen by ≥ 5% | Rewrite distractors with near-zero uptake |
| KR-20 (overall) | ≥ 0.70 | If below threshold, identify weakest items and replace |

### Step 5 — Cut-Score Setting & Go/No-Go Gate
- **Method:** Modified Angoff procedure — each expert estimates the probability that a "minimally competent" Beginner, Intermediate, and Advanced candidate answers each item correctly; means become provisional cut scores
- **Go/No-Go gate:** The instrument may launch when ≥ 75% of participants are correctly classified into their expert-nominated level (requires a subsample of n ≥ 30 with verified competency levels from manager nominations or prior assessment)
- **IRT migration trigger:** Once n ≥ 300 responses are collected post-launch, run IRT 3PL calibration; migrate to theta-based scoring if model fit is acceptable (RMSEA < 0.06, CFI > 0.95)

---

## Section 8: Implementation Notes

### Features to Avoid Building
1. **Coding challenge / live execution environment** — HackerRank already dominates this space; it adds infrastructure complexity without differentiation for the non-technical primary audience
2. **Certification or badge credential** — Vendor certs (Microsoft, Google, AWS) have established trust; a new credential from an unknown issuer has no market value without accreditation investment
3. **LMS or course recommendation engine** — Pluralsight, Coursera, and Microsoft Skills Navigator already do this; building it duplicates existing infrastructure and distracts from the diagnostic core value

### Tech Stack Considerations
- **Delivery:** Any modern web framework with branching logic (Stage 1 → Stage 2 routing can be implemented with simple conditional logic, no CAT engine required)
- **Scoring:** Server-side calculation of Bloom's-weighted score and level assignment; store raw item responses for future IRT calibration
- **Reporting:** Radar chart with 6 axes (one per dimension); single-page PDF export for the participant; CSV/dashboard export for L&D managers (cohort view)
- **Data storage:** Store individual theta baselines with timestamps to enable pre/post comparison; comply with GDPR (Norwegian Personopplysningsloven) — no third-party data sharing without explicit consent

### EU AI Act Article 4 Compliance Framing
EU AI Act Article 4 (in force February 2025, enforcement August 2026) requires all organisations deploying AI systems to ensure staff have "sufficient AI literacy." The ACA provides:
- A documented baseline assessment for compliance records
- An org-level gap report showing which roles/teams need upskilling
- Pre/post measurement to demonstrate training effectiveness to regulators
- Vendor-neutral scope (not tied to a specific AI vendor's tools or platform)

This positions the ACA as a compliance tool as well as an L&D tool — a dual value proposition for Norwegian and EU clients.

### Recommended Next Steps
1. **Complete this research report** → save to `projects/AI-training/ai-competency-research.md`
2. **Commission expert review** of the 6 sample questions above + expand to 30-item pool
3. **Build MVP web test** — two-stage routing, 24 items, radar chart output, CSV export for L&D managers
4. **Run pilot** with 150–200 participants from Metier's network and partner organisations
5. **Refine and launch** — public URL, GDPR-compliant, EU AI Act Article 4 positioning

---

## Inferred Findings

**Inferred:** The two-stage routing design (all participants take Intermediate items first) is the minimum viable adaptive design for an organisation without a dedicated psychometrician or CAT engine.
**Based on:** Task 03 research (IRT 3PL migration path requires n ≥ 300 calibrated items before it adds value over classical scoring); Task 04 research (no existing platform offers two-stage routing without requiring a full CAT infrastructure).
**Reasoning:** By deduction, the two-stage design fills the gap between no adaptation (flat 24-item test) and full CAT, using only branching logic that any web developer can implement — and it is the right design choice until the item bank matures enough for IRT calibration.

**Inferred:** The EU AI Act Article 4 compliance framing is a stronger commercial differentiator for Norwegian/EU clients than the L&D diagnostic framing alone.
**Based on:** Task 02 research (Article 4 enforcement August 2026, no prescriptive curriculum specified); Task 04 research (no existing platform explicitly positions itself as an Article 4 compliance documentation tool).
**Reasoning:** By triangulation — the regulatory gap (no mandated curriculum) and the market gap (no compliance-positioned diagnostic tool) combine to create a positioning opportunity that is neither filled by existing vendors nor addressed by the frameworks themselves.

## Unverified Observations

- The "75% correct-classification gate" in Section 7 Step 5 is a commonly cited practitioner standard for diagnostic test validation but could not be sourced to a specific psychometric standard during this synthesis. It is consistent with ISO/IEC 17024 spirit but should be confirmed with a qualified psychometrician before adoption as a hard go/no-go criterion.
- The GDPR/Personopplysningsloven note in Section 8 is a general legal observation, not verified legal advice. A Norwegian data protection lawyer should review the data storage and consent model before launch.

## Sources

- Prior research tasks 01–05 (internal — all files in `workspace/tasks/`)

---
*Executed: 2026-04-30 | Mode: sequential*
