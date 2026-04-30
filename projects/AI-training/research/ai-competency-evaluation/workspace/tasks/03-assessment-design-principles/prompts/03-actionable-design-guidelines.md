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
