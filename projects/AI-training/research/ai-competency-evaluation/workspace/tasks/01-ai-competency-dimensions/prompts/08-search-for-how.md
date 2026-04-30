# Prompt 08: search-for-how

> **Prompt:** How are agentic AI skills defined and levelled — from using simple agent tools to designing multi-agent systems?

---

Agentic AI competency is emerging as a structured skill domain, defined across documentation from leading frameworks (Anthropic, LangChain/LangGraph, AutoGen, CrewAI) and a growing body of formal curricula. Competency is broadly grouped around five conceptual pillars — tool use, memory/state, planning/reasoning, orchestration, and multi-agent coordination — and practitioners progress through recognizable levels from consumer-of-tools through to architect of complex systems.

## The Core Conceptual Pillars

Anthropic's canonical reference draws a foundational distinction: "Workflows are systems where LLMs and tools are orchestrated through predefined code paths. Agents, on the other hand, are systems where LLMs dynamically direct their own processes and tool usage, maintaining control over how they accomplish tasks." — [Building Effective AI Agents](https://www.anthropic.com/research/building-effective-agents). This workflow-vs-agent distinction is the first conceptual gate every practitioner must cross.

The key concepts someone must understand to work effectively with agents, drawn from framework documentation, are:

1. **Tool use and function calling** — enabling an LLM to invoke external functions, APIs, or search. "Tool calling, structured outputs, and short-term memory are options for tailoring LLMs to your needs." — [LangGraph Documentation](https://www.langchain.com/langgraph)
2. **Memory and state management** — "LangGraph lets you define states—data and context stored across steps to maintain memory and decision history—and supports persistent memory and state storage, so agents can remember essential details throughout long-running processes." — [LangGraph](https://www.langchain.com/langgraph)
3. **Planning and reasoning patterns** — including ReAct (Reason + Act), chain-of-thought, and tree-of-thought. "Agentic AI Design Patterns are reusable templates that guide how intelligent agents perceive, reason, act, and adapt." — [Agentic AI Courses & Training Guide](https://www.hashmeta.ai/en/generative-ai/agentic-ai-courses-training)
4. **Orchestration patterns** — Anthropic documents three core patterns: prompt chaining (sequential steps), orchestrator-workers (dynamic delegation), and evaluator-optimizer (feedback loop). "In the orchestrator-workers workflow, a central LLM dynamically breaks down tasks, delegates them to worker LLMs, and synthesizes their results." — [Building Effective AI Agents](https://www.anthropic.com/research/building-effective-agents)
5. **Multi-agent coordination** — "CrewAI emphasizes role-based multi-agent systems where each agent can have a specialized function within a team, allowing natural task division and collaboration." — [Top AI Agent Frameworks 2026](https://www.intuz.com/blog/top-5-ai-agent-frameworks-2025)

## Skill Levels as Defined by Curricula

Formal training programs map these concepts to a three-tier progression:

**Level 1 — User/Consumer (Foundational)**
Understands what an agent is and can use pre-built agent tools. "Foundational principles of agentic AI cover AI systems that go beyond passive prediction to actively perceive, reason, act, and adapt within dynamic environments." — [Agentic AI Courses & Training Guide](https://www.hashmeta.ai/en/generative-ai/agentic-ai-courses-training). At this level, practitioners use tools like AgentGPT or no-code CrewAI interfaces. "For beginners, starting with AgentGPT or CrewAI offers a gentler learning curve." — [Top AI Agent Frameworks in 2025](https://www.codecademy.com/article/top-ai-agent-frameworks-in-2025)

**Level 2 — Builder/Developer (Intermediate)**
Constructs single-agent systems using frameworks, configures tool use, implements RAG, and builds defined workflows. "Programs start with foundational expertise connecting LLMs using proven design patterns, then upskill with new frameworks: OpenAI Agents SDK, CrewAI, LangGraph and Autogen." — [Agentic AI Courses & Training Guide](https://www.hashmeta.ai/en/generative-ai/agentic-ai-courses-training). Anthropic also defines "Agent Skills" as a practitioner concept at this level: "Agent Skills are organized folders of instructions, scripts, and resources that agents can discover and load dynamically to perform better at specific tasks." — [Agent Skills Overview](https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview)

**Level 3 — Architect/Designer (Advanced)**
Designs multi-agent systems from scratch, manages inter-agent communication, state sharing, and failure modes. "Advanced courses teach learners to build coordinated teams of AI agents through the entire process of creating multi-agent systems, from architectural design to implementation in Python, mastering how to orchestrate complex workflows, manage data flow and state, and use advanced techniques like multi-agent RAG." — [Agentic AI Courses & Training Guide](https://www.hashmeta.ai/en/generative-ai/agentic-ai-courses-training). LangGraph is the primary production framework at this level: "LangGraph is a low-level orchestration framework for building, managing, and deploying long-running, stateful agents." — [LangGraph](https://www.langchain.com/langgraph). AutoGen specifically targets this tier with its design for "multi-agent collaboration and asynchronous task execution" and "human-in-the-loop oversight." — [Top AI Agent Frameworks 2026](https://www.intuz.com/blog/top-5-ai-agent-frameworks-2025)

## Key Practitioner Principles

Anthropic's guide offers three meta-principles that cut across levels: "maintain simplicity in your agent's design, start with simple prompts, optimize them with comprehensive evaluation, and add multi-step agentic systems only when simpler solutions fall short." — [Building Effective AI Agents](https://www.anthropic.com/research/building-effective-agents). This implies that even advanced practitioners must be able to argue *against* complexity — a key competency marker distinguishing mature practitioners from framework-users.

Formal certification is now available: Johns Hopkins offers an "Agentic AI Certificate Program" and Udacity offers an "Agentic AI Nanodegree," both signalling that the field has reached sufficient maturity for credentialed skill recognition — [JHU Certificate](https://online.lifelonglearning.jhu.edu/jhu-certificate-program-agentic-ai), [Udacity Nanodegree](https://www.udacity.com/course/agentic-ai--nd900).

---

## Inferred Findings

**Inference 1: The workflow-vs-agent boundary is the primary skill threshold.**
Based on: Anthropic's explicit distinction between "predefined code paths" (workflows) and "dynamically directed processes" (agents) — [Anthropic](https://www.anthropic.com/research/building-effective-agents) — and the consistent framing across curricula that foundational learners work with workflows before advancing to autonomous agents — [Hashmeta AI](https://www.hashmeta.ai/en/generative-ai/agentic-ai-courses-training). Reasoning: every curriculum reviewed introduces this distinction as gating content, suggesting it maps to the Level 1→2 transition.

**Inference 2: Production competency requires evaluation and observability skills, not just building skills.**
Based on: Anthropic's principle to "measure everything, add complexity only when it delivers measurable value" — [Anthropic](https://www.anthropic.com/research/building-effective-agents) — and LangGraph's explicit mention of "support for debugging as well as deployment" — [LangGraph](https://www.langchain.com/langgraph). Reasoning: intermediate-to-advanced practitioners who cannot evaluate agent behaviour in production are unlikely to be considered competent regardless of their ability to construct agents.

---

## Unverified Observations

- Microsoft AutoGen's documentation may include a more explicit competency or role-based skill taxonomy, but the AutoGen docs were not directly accessible in this research pass and could not be verified.
- The CrewAI platform's own documentation may define operator-level skill requirements distinct from developer-level ones, but this was not confirmed from first-party sources.

---

## Sources
- https://www.anthropic.com/research/building-effective-agents
- https://platform.claude.com/docs/en/agents-and-tools/agent-skills/overview
- https://www.langchain.com/langgraph
- https://www.intuz.com/blog/top-5-ai-agent-frameworks-2025
- https://www.codecademy.com/article/top-ai-agent-frameworks-in-2025
- https://www.hashmeta.ai/en/generative-ai/agentic-ai-courses-training
- https://online.lifelonglearning.jhu.edu/jhu-certificate-program-agentic-ai
- https://www.udacity.com/course/agentic-ai--nd900
- https://learn.deeplearning.ai/courses/agentic-ai/information
- https://www.coursera.org/learn/agentic-ai-with-langgraph-crewai-autogen-and-beeai

---
*Executed: 2026-04-30 | Mode: independent*
