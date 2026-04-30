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
