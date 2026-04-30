# Prompt 01: rag-and-agents

> **Prompt:** Advanced RAG and agentic AI competency markers with example MCQ questions per level

---

## Domain 1: RAG (Retrieval-Augmented Generation)

### Intermediate Competency — 3 Key Concepts

**1. Basic retrieval pipeline construction**
Setting up an end-to-end RAG pipeline: document ingestion, chunking, embedding, vector store indexing, and prompt-augmented generation. "Chunk size, overlap, reranking, and query reformulation have an outsized effect on accuracy" — [LlamaIndex RAG: Building retrieval systems](https://www.statsig.com/perspectives/llamaindex-rag-retrieval). An intermediate practitioner can configure these parameters and wire together a functional pipeline using LlamaIndex or LangChain.

**2. Hybrid search (BM25 + dense retrieval)**
Combining keyword-based (BM25/lexical) search with semantic vector search, then merging results via Reciprocal Rank Fusion (RRF). "Pair a keyword-based retriever with dense embeddings, then combine their results using Reciprocal Rank Fusion (RRF) — a standard way of merging ranked lists." — [Hybrid Search Alpha Tuning For RAG | LlamaIndex](https://www.llamaindex.ai/blog/llamaindex-enhancing-retrieval-performance-with-alpha-tuning-in-hybrid-search-in-rag-135d0c9b8a00). Mastery here marks a clear step beyond naive single-vector retrieval.

**3. Reranking retrieved results**
Applying a cross-encoder or model-based reranker (e.g., ColBERT) to re-order the top-k candidates after initial retrieval. "Start with re-ranking: apply a cross-encoder on the top-k candidates or use MMR to balance relevance and diversity." — [Advanced RAG: ColBERT Reranker and LlamaIndex](https://www.pondhouse-data.com/blog/advanced-rag-colbert-reranker). This separates practitioners who understand two-stage retrieval from those relying on a single embedding pass.

**Intermediate MCQ example:**

> In a standard two-stage RAG pipeline, what is the purpose of a reranker applied after initial vector retrieval?
>
> A) To generate the final answer from retrieved chunks  
> B) To re-order the top-k candidates by relevance using a more precise cross-encoder model  
> C) To split documents into smaller chunks before indexing  
> D) To convert query text into dense embeddings  
>
> *Correct answer: B*

---

### Advanced / Expert Competency — 3 Key Concepts

**1. RAG evaluation with RAGAS (multi-dimensional metrics)**
RAGAS is "a framework for reference-free evaluation of Retrieval Augmented Generation (RAG) pipelines" that uses LLM-based metrics including faithfulness, answer relevancy, context precision, context recall, noise sensitivity, and context entities recall. "Evaluating RAG architectures is challenging because there are several dimensions to consider: the ability of the retrieval system to identify relevant and focused context passages, the ability of the LLM to exploit such passages in a faithful way, or the quality of the generation itself." — [RAGAS paper, arXiv:2309.15217](https://arxiv.org/abs/2309.15217). Expert-level practitioners design evaluation pipelines across all these dimensions.

**2. Query understanding and decomposition (agentic/multi-step retrieval)**
Going beyond single-query retrieval to query transformation, sub-query decomposition, and multi-hop reasoning. "Advanced RAG is about steady, incremental improvements across retrieval, context management, and generation... add query understanding and context distillation, and bring in multi-step reasoning with a knowledge graph." — [Advanced RAG Techniques | Neo4j](https://neo4j.com/blog/genai/advanced-rag-techniques/). Expert practitioners implement agentic retrieval where the system iteratively reformulates queries based on intermediate results.

**3. Agentic RAG and knowledge graph integration**
Treating retrieval as an agent-controlled loop rather than a single pass: "Agentic retrieval moves beyond naive RAG toward systems where the retriever itself plans, decomposes, and iterates." — [Agentic Retrieval Guide | LlamaIndex](https://www.llamaindex.ai/blog/rag-is-dead-long-live-agentic-retrieval). This includes routing queries to heterogeneous sources (structured DBs, knowledge graphs, APIs) and using tool-calling to orchestrate retrieval steps.

**Advanced MCQ example:**

> A RAG system returns answers with high answer relevancy but low faithfulness scores in RAGAS evaluation. What does this most likely indicate?
>
> A) The retriever is returning irrelevant documents  
> B) The LLM is generating plausible-sounding answers that are not grounded in the retrieved context  
> C) The chunk size is too small for the embedding model  
> D) The BM25 index is out of date  
>
> *Correct answer: B*

---

## Domain 2: Agentic AI / Agent Orchestration

### Intermediate (Builder) Competency — 3 Key Concepts

**1. Single-agent tool use and ReAct loops**
Implementing an agent that uses the Reason + Act (ReAct) pattern — iteratively calling tools, observing results, and reasoning toward a goal. Builders can wire together tool definitions, handle tool outputs, and manage the agent's context window. "LangGraph enables implementation of Reflection, Reflexion, and ReAct agent architectures to design workflows that evaluate and refine their own outputs." — [LangGraph AI Framework 2025 | Latenode](https://latenode.com/blog/ai-frameworks-technical-infrastructure/langgraph-multi-agent-orchestration/langgraph-ai-framework-2025-complete-architecture-guide-multi-agent-orchestration-analysis).

**2. Sequential and prompt-chaining workflows**
Constructing deterministic, multi-step workflows where the output of one LLM call feeds the next. Anthropic identifies Prompt-Chaining as one of six foundational patterns: alongside Evaluator-Optimizer, Context-Augmentation, Parallelization, Routing, and Orchestrator-Workers. "Developers should start with simple prompts, optimize them with comprehensive evaluation, and add multi-step agentic systems only when simpler solutions fall short." — [Building Effective AI Agents | Anthropic](https://www.anthropic.com/research/building-effective-agents). Builders know when a chained workflow is sufficient versus when a dynamic agent is needed.

**3. Stateful graph construction with LangGraph**
Building agent workflows as directed graphs with persistent state — nodes (actions), edges (transitions), and conditional routing. "LangGraph is a Python-based framework designed to manage multi-agent workflows using graph architectures, organizing actions as nodes in a directed graph to enable conditional decision-making, parallel execution, and persistent state management." — [LangGraph Multi-Agent Orchestration | Latenode](https://latenode.com/blog/ai-frameworks-technical-infrastructure/langgraph-multi-agent-orchestration/langgraph-multi-agent-orchestration-complete-framework-guide-architecture-analysis-2025).

**Builder MCQ example:**

> In LangGraph, what differentiates a conditional edge from a standard edge?
>
> A) Conditional edges carry state data between nodes; standard edges do not  
> B) Conditional edges route to different nodes based on runtime evaluation of the current state; standard edges always go to a fixed next node  
> C) Conditional edges pause execution pending human approval; standard edges execute immediately  
> D) Conditional edges are used only in subgraphs; standard edges are used in the main graph  
>
> *Correct answer: B*

---

### Advanced / Architect Competency — 3 Key Concepts

**1. Multi-agent orchestrator-worker architecture with parallelism**
Designing systems where a lead orchestrator decomposes goals and dispatches tasks to specialized subagents running in parallel. "Anthropic's Research system uses a multi-agent architecture with an orchestrator-worker pattern, where a lead agent coordinates the process while delegating to specialized subagents that operate in parallel." — [How we built our multi-agent research system | Anthropic](https://www.anthropic.com/engineering/multi-agent-research-system). Architects specify task boundaries, output contracts, and failure recovery strategies across the agent mesh.

**2. Subgraph modularity, reusability, and inter-agent communication**
Decomposing large agent systems into independently testable subgraphs with clear interfaces. "Subgraphs group related agents into reusable components — for example, a document processing subgraph might include agents for text extraction, formatting analysis, and content classification, operating independently while contributing to the broader workflow." — [LangGraph AI Framework 2025 | Latenode](https://latenode.com/blog/ai-frameworks-technical-infrastructure/langgraph-multi-agent-orchestration/langgraph-ai-framework-2025-complete-architecture-guide-multi-agent-orchestration-analysis). Architects design the inter-subgraph communication protocol, state schema, and versioning.

**3. Evaluator-optimizer loops, reflection, and self-correction**
Building agents that assess their own outputs against criteria, then iteratively refine them — closing the loop between generation and evaluation. Anthropic's Evaluator-Optimizer pattern is listed as one of its six composable foundational patterns for production agents. "To use LangGraph effectively, teams need a strong grasp of graph theory, state machines, and distributed systems architecture." — [LangGraph AI Framework 2025 | Latenode](https://latenode.com/blog/ai-frameworks-technical-infrastructure/langgraph-multi-agent-orchestration/langgraph-ai-framework-2025-complete-architecture-guide-multi-agent-orchestration-analysis). At architect level, practitioners also design termination criteria and loop-escape conditions to prevent infinite refinement cycles.

**Architect MCQ example:**

> In Anthropic's Orchestrator-Workers pattern for a multi-agent research system, what is the primary responsibility of the orchestrator agent?
>
> A) Executing tool calls and writing final outputs to storage  
> B) Decomposing the user's goal into subtasks and assigning them to specialized subagents, then synthesizing their outputs  
> C) Maintaining the vector store index and routing semantic queries  
> D) Acting as the only agent with access to external APIs to prevent redundant calls  
>
> *Correct answer: B*

---

## Inferred Findings

- The boundary between intermediate and advanced RAG maps cleanly onto the boundary between single-pass retrieval and multi-stage, evaluation-driven pipelines. RAGAS operationalises this divide: intermediate practitioners build pipelines; advanced practitioners measure and optimise them across multiple dimensions (faithfulness, context precision, noise sensitivity).
- The builder-to-architect divide in agentic AI mirrors a shift from imperative scripting (write the workflow) to systems design (define contracts, failure modes, observability, and inter-agent governance). LangGraph's requirement for "graph theory, state machines, and distributed systems architecture" is a good proxy test for architect-level readiness.

## Unverified Observations

- LlamaIndex claims a "35% boost in retrieval accuracy" in 2025, cited in search summaries but the underlying benchmark methodology was not verified from primary source.
- The claim that RAGAS processes "over 5 million evaluations monthly" appears in search summaries but was not confirmed from the official RAGAS docs (403 on direct fetch).

## Sources

- [LlamaIndex RAG: Building retrieval systems — Statsig](https://www.statsig.com/perspectives/llamaindex-rag-retrieval)
- [Advanced RAG: ColBERT Reranker and LlamaIndex — Pondhouse Data](https://www.pondhouse-data.com/blog/advanced-rag-colbert-reranker)
- [Advanced RAG Techniques for High-Performance LLM Applications — Neo4j](https://neo4j.com/blog/genai/advanced-rag-techniques/)
- [Hybrid Search Alpha Tuning For RAG — LlamaIndex Blog](https://www.llamaindex.ai/blog/llamaindex-enhancing-retrieval-performance-with-alpha-tuning-in-hybrid-search-in-rag-135d0c9b8a00)
- [Agentic Retrieval Guide: Beyond Naive RAG — LlamaIndex Blog](https://www.llamaindex.ai/blog/rag-is-dead-long-live-agentic-retrieval)
- [RAGAS: Automated Evaluation of Retrieval Augmented Generation — arXiv:2309.15217](https://arxiv.org/abs/2309.15217)
- [RAGAS Metrics Documentation](https://docs.ragas.io/en/stable/concepts/metrics/)
- [Building Effective AI Agents — Anthropic](https://www.anthropic.com/research/building-effective-agents)
- [How we built our multi-agent research system — Anthropic Engineering](https://www.anthropic.com/engineering/multi-agent-research-system)
- [LangGraph AI Framework 2025: Complete Architecture Guide — Latenode](https://latenode.com/blog/ai-frameworks-technical-infrastructure/langgraph-multi-agent-orchestration/langgraph-ai-framework-2025-complete-architecture-guide-multi-agent-orchestration-analysis)
- [LangGraph Multi-Agent Orchestration — Latenode](https://latenode.com/blog/ai-frameworks-technical-infrastructure/langgraph-multi-agent-orchestration/langgraph-multi-agent-orchestration-complete-framework-guide-architecture-analysis-2025)
- [Building Agentic Workflows with LangGraph and Granite — IBM](https://www.ibm.com/think/tutorials/build-agentic-workflows-langgraph-granite)
- [Agent Orchestration: LangChain, LangGraph, AutoGen — Medium](https://medium.com/@akankshasinha247/agent-orchestration-when-to-use-langchain-langgraph-autogen-or-build-an-agentic-rag-system-cc298f785ea4)

---
*Executed: 2026-04-30 | Mode: independent*
