# Prompt 02: evals-and-finetuning

> **Prompt:** Advanced AI evals and fine-tuning competency markers with example MCQ questions per level

---

## Domain 3: AI Evaluation / Evals

### Intermediate Competency Markers (using existing benchmarks)

**1. Running and interpreting established benchmarks (HELM, MT-Bench)**
An intermediate practitioner understands the scope of existing benchmarks and what each one measures. HELM evaluates models "holistically across multiple metrics including accuracy, calibration, robustness, fairness, bias, toxicity, and efficiency" — [LXT AI Blog](https://www.lxt.ai/blog/llm-benchmarks/). MT-Bench uses "80 high-quality, multi-turn questions tailored to assess conversation flow and instruction-following capabilities" — [MT-Bench on Klu](https://klu.ai/glossary/mt-bench-eval). Competency at this level means selecting the right benchmark for the task and correctly reading leaderboard scores.

**2. Understanding LLM-as-judge as an evaluation pattern**
The LLM-as-judge approach uses strong models (e.g., GPT-4) to score model outputs. "Strong LLM judges like GPT-4 can match both controlled and crowdsourced human preferences well, achieving over 80% agreement, the same level of agreement between humans." — [Judging LLM-as-a-Judge, arXiv:2306.05685](https://arxiv.org/abs/2306.05685). Intermediate competency means being able to set up a basic LLM-as-judge pipeline and interpret its scores.

**3. Recognising benchmark limitations and failure modes**
An intermediate practitioner knows that static benchmarks can become saturated and that LLM-as-a-judge has "limitations, such as its inability to detect hallucinations and penalize LLM generated answers accordingly, and potential errors when grading math/reasoning questions." — [arXiv:2306.05685](https://arxiv.org/abs/2306.05685). Awareness of AgentBench's design — which "requires sustained goal-directed behaviour over multiple steps" and "covers tool use, memory, and planning simultaneously" — signals readiness to evaluate agents beyond static QA. — [LXT AI Blog](https://www.lxt.ai/blog/llm-benchmarks/)

**Example Intermediate MCQ:**

> You run MT-Bench on two instruction-tuned models. Model A scores 7.8/10; Model B scores 7.2/10. A colleague says Model B is clearly inferior for your customer-support chatbot. What is the most important caveat?
>
> A) MT-Bench scores are not reproducible across different judge models  
> B) MT-Bench assesses general multi-turn conversation; it may not reflect performance on your specific domain and task distribution  
> C) GPT-4 judges always favour longer responses regardless of quality  
> D) Scores below 8.0 indicate the model is not production-ready  
>
> **Correct answer: B**

---

### Advanced Eval Design Markers

**1. Designing custom task-specific evaluation rubrics and golden datasets**
Advanced practitioners build evals from scratch: "Start from real failure modes in your traces, pick the right metric, write a clear rubric, and validate the judge against a golden dataset (aim for 75–90% agreement with human labels) before you scale it." — [Monte Carlo Data – LLM-as-Judge Best Practices](https://www.montecarlodata.com/blog-llm-as-judge/). Binary evaluations ("Polite" vs. "Impolite") are preferred over continuous scales for reliability. — [Evidently AI LLM-as-a-Judge Guide](https://www.evidentlyai.com/llm-guide/llm-as-a-judge)

**2. Judge calibration and bias mitigation**
Calibrating a judge means testing it against human annotation and correcting for systematic biases. The AUTOCALIBRATE method is described as "a multi-stage, gradient-free approach that automatically calibrates and aligns an LLM-based evaluator to match human preferences for NLG quality assessment." — [Monte Carlo Data – LLM-as-Judge Best Practices](https://www.montecarlodata.com/blog-llm-as-judge/). Known biases to control for include position bias (favouring the first response) and verbosity bias. A 100% pass rate is a warning sign, not success: "treating a 100% pass rate as success instead of a sign the eval isn't hard enough" is listed as a top pitfall. — [Monte Carlo Data](https://www.montecarlodata.com/blog-llm-as-judge/)

**3. Multi-environment and agentic evaluation design**
Advanced eval designers move beyond single-turn scoring to multi-step agent evaluation. AgentBench "tests agent performance across diverse interactive environments including operating systems, databases, knowledge graphs, and web browsers" — [LXT AI Blog](https://www.lxt.ai/blog/llm-benchmarks/). Designing eval harnesses that capture intermediate reasoning steps, tool-call correctness, and task-completion rate across trajectories — not just final outputs — is a hallmark of advanced competency.

**Example Advanced MCQ:**

> You build an LLM-as-judge pipeline to evaluate 10,000 customer-support responses daily. After launch you notice the judge gives 98% of responses a passing score. What should you do first?
>
> A) Increase the judge's temperature to introduce more variance in scores  
> B) Validate the judge against a human-annotated golden set; a near-perfect pass rate likely signals a rubric that is too easy or inputs that are incorrectly formatted  
> C) Switch to a smaller, cheaper judge model to reduce cost  
> D) Accept the results — high pass rates indicate high model quality  
>
> **Correct answer: B**

---

## Domain 4: Fine-tuning and Model Adaptation

### Intermediate Competency Markers

**1. Knowing when to fine-tune vs. prompt engineer**
The recommended decision hierarchy is to "start with the lowest-complexity approach (prompt engineering), graduating to fine tuning when necessary." — [Databricks LLM Fine-Tuning Guide](https://www.databricks.com/blog/llm-fine-tuning). Fine-tuning is warranted when style/format consistency, latency constraints, or persistent domain knowledge cannot be achieved through prompting alone. Misapplying fine-tuning to problems solvable by prompting wastes resources and risks overfitting.

**2. Understanding LoRA and PEFT mechanics**
Intermediate competency means knowing that LoRA "uses only small adapter matrices instead of updating all model parameters" and that the rank hyperparameter controls the capacity of the adapter. — [Databricks LoRA Guide](https://www.databricks.com/blog/efficient-fine-tuning-lora-guide-llms). A practitioner at this level can configure a PEFT run using the Hugging Face `peft` library, select an appropriate rank, and explain why QLoRA (LoRA + bitsandbytes quantisation) reduces GPU memory requirements. — [Medium: PEFT, LoRA & QLoRA](https://medium.com/@akankshasinha247/peft-lora-qlora-smarter-faster-fine-tuning-for-domain-llms-3d7b7fdf9671)

**3. Instruction tuning format and supervised fine-tuning basics**
For instruction following, "supervised fine-tuning further trains a pretrained model to generate text conditioned on a provided prompt, using prompt-response pairs formatted in a consistent manner." — [apxml.com LoRA/PEFT Course](https://apxml.com/courses/lora-peft-efficient-llm-training). Intermediate practitioners can prepare instruction datasets in standard chat formats (e.g., Alpaca, ShareGPT), apply loss masking so gradients flow only through response tokens, and run a basic training loop.

**Example Intermediate MCQ:**

> A product team wants their LLM to always respond in a specific JSON schema. They have 200 labelled examples. What is the most appropriate first step?
>
> A) Pre-train a new model from scratch on domain data  
> B) Use few-shot prompting with JSON examples in the system prompt; if quality is insufficient, proceed to supervised fine-tuning with the 200 examples  
> C) Fine-tune immediately using full parameter updates to maximise signal  
> D) Increase model size to improve instruction-following ability  
>
> **Correct answer: B**

---

### Advanced / Expert Competency Markers

**1. Hyperparameter tuning and rank selection for LoRA**
Expert practitioners understand that "LoRA's fixed-rank assumption means every layer received the same adaptation capacity regardless of its importance" — [mbrenndoerfer.com – PEFT Beyond LoRA](https://mbrenndoerfer.com/writing/peft-beyond-lora-advanced-parameter-efficient-finetuning-techniques) — and know when to apply adaptive-rank methods like AdaLoRA. The typical fine-tuning learning rate range of 10⁻⁵ to 10⁻⁴ reflects "accumulated empirical evidence across many domains and model families." — [Databricks LLM Fine-Tuning Guide](https://www.databricks.com/blog/llm-fine-tuning). Knowing which layers to target (attention projection matrices vs. MLP) and how rank interacts with dataset size is expert-level knowledge.

**2. Catastrophic forgetting: diagnosis and mitigation**
Catastrophic forgetting means "models forgetting previously acquired knowledge when learning new data." — [Towards AI: Fine-Tuning Without Catastrophic Forgetting](https://towardsai.net/p/machine-learning/fine-tuning-large-language-models-llms-without-catastrophic-forgetting). The primary mitigation is PEFT: "by freezing most of the base model's weights and only updating adapter parameters, PEFT preserves general language understanding while acquiring task-specific capability." — [Legion Intel Blog](https://www.legionintel.com/blog/navigating-the-challenges-of-fine-tuning-and-catastrophic-forgetting). Advanced practitioners also evaluate on held-out general benchmarks (e.g., MMLU) pre- and post-fine-tuning to quantify regression, and use regularisation or replay techniques for continual fine-tuning scenarios.

**3. Data curation as the primary quality lever**
"Data preparation is frequently the most time-consuming phase of LLM fine tuning and the factor most directly responsible for final model quality. The principle that a smaller dataset of high-quality examples consistently outperforms a larger dataset with noisy data is well established." — [Databricks LLM Fine-Tuning Guide](https://www.databricks.com/blog/llm-fine-tuning). Expert-level data curation includes deduplication, quality filtering, domain balance analysis, detecting and removing near-duplicate or poisoned examples, and deliberately designing adversarial or edge-case examples to address identified failure modes.

**Example Advanced MCQ:**

> After fine-tuning a 7B model on 5,000 customer-service examples using full-parameter fine-tuning with a learning rate of 1e-4, evaluation shows strong task performance but a 12-point drop on MMLU. What is the most likely cause and the best remediation?
>
> A) The dataset is too small; collect 50,000 more examples and retrain  
> B) Catastrophic forgetting caused by aggressive full-parameter updates; switch to LoRA/PEFT with a lower learning rate (1e-5) to preserve base model knowledge while acquiring task-specific capability  
> C) The MMLU benchmark is incompatible with instruction-tuned models; the result can be ignored  
> D) Use a higher-rank LoRA adapter to increase model expressiveness  
>
> **Correct answer: B**

---

## Inferred Findings

- The boundary between "intermediate" and "advanced" eval competency largely hinges on whether the practitioner is *consuming* existing benchmarks vs. *designing* and *calibrating* new evaluation systems. The 75–90% human-agreement threshold for judge validation is an operationalisable gate for this distinction.
- For fine-tuning, the field has converged on PEFT/LoRA as the default approach even for expert practitioners — full fine-tuning is now the exception, not the norm. Expert differentiation lies in rank selection, continual learning strategy, and data curation rigour, not in access to more compute.

## Unverified Observations

- The claim that "fine-tuning with LLM-generated data reduces non-target task degradation compared to fine-tuning with ground truth data" (attributed to search result summaries from Databricks) could not be verified against the primary source due to a 403 block on the Databricks blog. Treat as plausible but unconfirmed until primary source is accessible.
- AUTOCALIBRATE as a named method was referenced in search summaries but the primary paper could not be fetched to confirm methodology details.

## Sources
- https://arxiv.org/abs/2306.05685
- https://arxiv.org/html/2306.05685v4
- https://klu.ai/glossary/mt-bench-eval
- https://www.lxt.ai/blog/llm-benchmarks/
- https://www.montecarlodata.com/blog-llm-as-judge/
- https://www.evidentlyai.com/llm-guide/llm-as-a-judge
- https://langfuse.com/docs/evaluation/evaluation-methods/llm-as-a-judge
- https://arxiv.org/abs/2411.15594
- https://www.databricks.com/blog/llm-fine-tuning
- https://www.databricks.com/blog/efficient-fine-tuning-lora-guide-llms
- https://mbrenndoerfer.com/writing/peft-beyond-lora-advanced-parameter-efficient-finetuning-techniques
- https://medium.com/@akankshasinha247/peft-lora-qlora-smarter-faster-fine-tuning-for-domain-llms-3d7b7fdf9671
- https://apxml.com/courses/lora-peft-efficient-llm-training
- https://towardsai.net/p/machine-learning/fine-tuning-large-language-models-llms-without-catastrophic-forgetting
- https://www.legionintel.com/blog/navigating-the-challenges-of-fine-tuning-and-catastrophic-forgetting
- https://arxiv.org/abs/2308.08747
- https://arxiv.org/html/2401.05605v1
- https://arxiv.org/pdf/2403.14608

---
*Executed: 2026-04-30 | Mode: independent*
