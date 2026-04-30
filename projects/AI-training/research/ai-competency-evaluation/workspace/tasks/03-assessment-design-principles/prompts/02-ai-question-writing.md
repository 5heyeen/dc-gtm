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
