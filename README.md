# Awesome AI Agents 🧠🤖

A curated catalog of **AI agent frameworks, libraries, and tools** from the 2024–2025 wave, organized by category — plus a community-sourced **gap analysis** of the pain points and missing features you should know about before committing to a stack.

> **Methodology:** This catalog was compiled from (1) recent web articles/blog posts comparing agentic frameworks, (2) GitHub repo popularity searches, and (3) a deep dive into the issue trackers of the most popular projects to surface *recurring complaints and feature gaps* — not just marketing claims.

---

## Table of Contents

1. [The Landscape at a Glance](#the-landscape-at-a-glance)
2. [General-Purpose / Orchestration Frameworks](#general-purpose--orchestration-frameworks)
3. [Multi-Agent Frameworks](#multi-agent-frameworks)
4. [TypeScript / Web-Native Frameworks](#typescript--web-native-frameworks)
5. [Protocols & Interop Standards](#protocols--interop-standards)
6. [Specialized / Niche Frameworks](#specialized--niche-frameworks)
7. [Observability, Evaluation & Governance](#observability-evaluation--governance)
8. [⚠️ Gap Analysis: What the Community Is Complaining About](#️-gap-analysis-what-the-community-is-complaining-about)
9. [How to Choose](#how-to-choose)
10. [Sources](#sources)

---

## The Landscape at a Glance

The agentic AI ecosystem **exploded in 2024–2025**. What started as research projects (AutoGen, MetaGPT) became production infrastructure at companies like Klarna, Replit, and LinkedIn. The frameworks broadly fall into a few philosophical camps:

| Philosophy | Representative tools | Best for |
|---|---|---|
| **Graph / state-machine** (explicit control) | LangGraph, LangChain, Haystack | Complex, auditable workflows |
| **Role-based teams** (agent collaboration) | CrewAI, AutoGen, MetaGPT, Swarm | Rapid multi-agent prototyping |
| **Type-safe / web-native** | Mastra, Vercel AI SDK, Pydantic AI, Agno | JS/TS teams, typed workflows |
| **Lightweight / minimal** | OpenAI Agents SDK, Smolagents, Swarm | Simple single/multi-agent tasks |
| **Voice / realtime** | LiveKit Agents, TEN Framework | Voice & multimodal agents |
| **Protocols / interop** | MCP, A2A, Semantic Kernel | Cross-system agent communication |

> **Key insight:** *None of them solve the hard problem of agent reliability.* They all provide scaffolding; the production-grade concerns (state, recovery, observability, security) are largely left to you.

---

## General-Purpose / Orchestration Frameworks

| Project | Stars (approx.) | Language | Notes |
|---|---|---|---|
| [langchain-ai/langchain](https://github.com/langchain-ai/langchain) | ~146K | Python | The "agent engineering platform" — largest ecosystem, extensive connectors. |
| [langchain-ai/langgraph](https://github.com/langchain-ai/langgraph) | ~42K | Python | Low-level graph orchestration on top of LangChain; checkpoints & time-travel. |
| [deepset-ai/haystack](https://github.com/deepset-ai/haystack) | ~26K | Python | Production-oriented pipelines + agent workflows. |
| [microsoft/agent-framework](https://github.com/microsoft/agent-framework) | ~13K | Python/.NET | Microsoft's successor to Semantic Kernel; multi-agent orchestration. |
| [microsoft/semantic-kernel](https://github.com/microsoft/semantic-kernel) | ~22K | C#/Python | Model-agnostic SDK for agents & plugins. |

---

## Multi-Agent Frameworks

| Project | Stars (approx.) | Language | Notes |
|---|---|---|---|
| [FoundationAgents/MetaGPT](https://github.com/FoundationAgents/MetaGPT) | ~70K | Python | "AI software company" — SOP-driven multi-agent collaboration. |
| [microsoft/autogen](https://github.com/microsoft/autogen) | ~61K | Python | Multi-agent conversation framework; note: **maintenance mode** reported in 2025, with the Assistants API being deprecated. |
| [crewAIInc/crewAI](https://github.com/crewAIInc/crewAI) | ~58K | Python | Role-based "crews" — used by ~60% of Fortune 500 (per vendor claims). |
| [openai/openai-agents-python](https://github.com/openai/openai-agents-python) | ~29K | Python | Lightweight multi-agent framework from OpenAI. |
| [openai/swarm](https://github.com/openai/swarm) | ~22K | Python | *Educational* ergonomic multi-agent orchestration (not for production). |
| [VRSEN/agency-swarm](https://github.com/VRSEN/agency-swarm) | ~4.5K | Python | Reliable multi-agent orchestration. |
| [kyegomez/swarms](https://github.com/kyegomez/swarms) | ~7K | Python | Enterprise-grade multi-agent orchestration. |
| [agentuniverse-ai/agentUniverse](https://github.com/agentuniverse-ai/agentUniverse) | ~2.3K | Python | LLM multi-agent framework. |

---

## TypeScript / Web-Native Frameworks

| Project | Stars (approx.) | Language | Notes |
|---|---|---|---|
| [mastra-ai/mastra](https://github.com/mastra-ai/mastra) | ~28K | TypeScript | Modern TS framework from the Gatsby team; workflows, RAG, agents. |
| [VoltAgent/voltagent](https://github.com/VoltAgent/voltagent) | ~10K | TypeScript | Open-source TS AI agent engineering platform. |
| [BuilderIO/agent-native](https://github.com/BuilderIO/agent-native) | ~4.8K | TypeScript | Framework for building agentic apps. |
| [langchain-ai/langgraphjs](https://github.com/langchain-ai/langgraphjs) | ~3.3K | TypeScript | LangGraph for JS/TS. |
| [i-am-bee/beeai-framework](https://github.com/i-am-bee/beeai-framework) | ~3.4K | Python/TS | Production-ready agents in Python and TypeScript. |

---

## Protocols & Interop Standards

| Project / Standard | Notes |
|---|---|
| **MCP (Model Context Protocol)** | Anthropic's open standard for connecting AI to tools/data. Early adopters: Block, Apollo, Zed, Replit, Codeium, Sourcegraph. |
| **A2A (Agent-to-Agent)** | Google's protocol for agent discovery & cross-agent communication. |
| **Semantic Kernel** | Microsoft's model-agnostic orchestration SDK. |
| **Google ADK** | Agent Development Kit (Python + Java) powering Agentspace. |
| **AWS Strands Agents** | Model-driven AWS toolkit for building/running agents. |

---

## Specialized / Niche Frameworks

| Project | Stars (approx.) | Focus |
|---|---|---|
| [livekit/agents](https://github.com/livekit/agents) | ~14K | Realtime **voice** AI agents. |
| [TEN-framework/ten-framework](https://github.com/TEN-framework/ten-framework) | ~11K | Conversational voice AI agents. |
| [zai-org/Open-AutoGLM](https://github.com/zai-org/Open-AutoGLM) | ~26K | "AI Phone" — phone-controlling agent model. |
| [agent0ai/agent-zero](https://github.com/agent0ai/agent-zero) | ~19K | General-purpose autonomous agent. |
| [fetchai/uAgents](https://github.com/fetchai/uAgents) | ~1.6K | Decentralized agents. |
| [langroid/langroid](https://github.com/langroid/langroid) | ~2K | Multi-agent programming from ex-CMU/UW researchers. |

---

## Observability, Evaluation & Governance

| Project | Stars (approx.) | Focus |
|---|---|---|
| [raga-ai-hub/RagaAI-Catalyst](https://github.com/raga-ai-hub/RagaAI-Catalyst) | ~16K | Agent observability, tracing, evaluation. |
| LangSmith / LangFuse | — | Commercial tracing/eval for LangChain and others. |
| [Azure/agentops](https://github.com/Azure/agentops) | ~13 | Continuous evaluation & observability accelerator. |

---

## ⚠️ Gap Analysis: What the Community Is Complaining About

Digging into the issue trackers of LangGraph, CrewAI, AutoGen, OpenAI Agents SDK, and Mastra reveals **recurring, high-signal gaps**. These are the themes that appear again and again (with representative issues):

### 1. 🔐 Security, Governance & Guardrails (the #1 theme)
The single most common class of feature requests across every major framework:
- **No pre-execution guardrail hook** — "repeat-after-me" prompt-injection attacks trigger unconfirmed tool calls (LangGraph [#8817](https://github.com/langchain-ai/langgraph/issues/8817)).
- **Tool selection has no notion of trust** — a similarly-named tool with a flashier description can out-compete the correct one (LangGraph [#8818](https://github.com/langchain-ai/langgraph/issues/8818)).
- **Governance middleware for tool-call authorization** requested en masse (CrewAI [#5888](https://github.com/crewAIInc/crewAI/issues/5888), [#6025](https://github.com/crewAIInc/crewAI/issues/6025); AutoGen [#7405](https://github.com/microsoft/autogen/issues/7405) GuardrailProvider, [#7353](https://github.com/microsoft/autogen/issues/7353) cryptographic action receipts).
- **Cross-agent memory poisoning** — no write guards to prevent one agent corrupting shared memory (CrewAI [#6043](https://github.com/crewAIInc/crewAI/issues/6043)).

### 2. 🔁 Idempotency & Safe Retries
- **Tool re-execution on retry has no idempotency guard** — duplicate payments/emails/trades possible (CrewAI [#5802](https://github.com/crewAIInc/crewAI/issues/5802), 164 comments — one of the most-upvoted issues).
- **Naive retry logic** — retrying `HTTPError` 4xx responses (which should *not* be retried) alongside 5xx (LangGraph [#8840](https://github.com/langchain-ai/langgraph/issues/8840)).
- No dead-letter queues or human-in-the-loop escalation paths in most frameworks.

### 3. 🧠 State, Memory & Durability
- **Crash before first durable checkpoint silently drops an accepted run** with no failure record (LangGraph [#8764](https://github.com/langchain-ai/langgraph/issues/8764), 32 comments).
- **Session/interrupt persistence bugs** — orphaned `function_call_output`, duplicated pending input on lost acknowledgement (OpenAI Agents SDK [#4827](https://github.com/openai/openai-agents-python/issues/4827), [#4775](https://github.com/openai/openai-agents-python/issues/4775)).
- **Memory processors block the agent loop** with DB reads/token counting (Mastra [#15677](https://github.com/mastra-ai/mastra/issues/15677)), and sync observation failures block user turns for ~4 min (Mastra [#21849](https://github.com/mastra-ai/mastra/issues/21849)).
- **AutoGen** has an open RFC for a cross-agent shared memory store (scoped agent/group/global) — currently missing ([#7748](https://github.com/microsoft/autogen/issues/7748)).

### 4. 🔄 Infinite Loops & Termination
- No **native deterministic guardrail to prevent infinite agent delegation and tool loops** (CrewAI [#6414](https://github.com/crewAIInc/crewAI/issues/6414), [#6219](https://github.com/crewAIInc/crewAI/issues/6219)).
- AutoGen asks for a "mission keeper" role — a goal-integrity node beyond the "boss agent" pattern ([#7487](https://github.com/microsoft/autogen/issues/7487)).

### 5. 📚 Documentation & DX
- **LangGraph's learning curve is real** — abstraction layering + insufficient doc cohesion (widely reported).
- Docs examples pass options in places where they're **silently ignored** (LangGraph [#8920](https://github.com/langchain-ai/langgraph/issues/8920)).
- Missing production code-execution docs (CrewAI [#6180](https://github.com/crewAIInc/crewAI/issues/6180)).

### 6. 🚀 Performance & Scalability
- **Checkpointing/state overhead** limits high-throughput (thousands of concurrent agents) scenarios in LangGraph.
- **Small/open-source model friction** — CrewAI struggles with ≤7B-param models' function-calling.
- **Tool soup** at scale: flat tool lists don't handle discoverability, versioning, or access control.

### 7. 💰 Pricing & Ecosystem Lock-in
- CrewAI's hosted plan tiers have **wide gaps** (jumps to ~$6,000/yr past Basic).
- AutoGen in **maintenance mode** + Assistants API deprecation → migration risk.
- Observability often **vendor-locked** (LangSmith) or incomplete (OpenAI tracing spans show "No spans found", [#2477](https://github.com/openai/openai-agents-python/issues/2477)).

### 8. 🔭 Observability Gaps
- Errors swallowed and replaced with **generic messages** — lose root cause (CrewAI [#6262](https://github.com/crewAIInc/crewAI/issues/6262)).
- Tracing exporters **drop whole batches on HTTP 429** instead of respecting `Retry-After` (OpenAI Agents SDK [#5023](https://github.com/openai/openai-agents-python/issues/5023)).
- Sensitive data defaulting to being traced (OpenAI Agents SDK [#2393](https://github.com/openai/openai-agents-python/issues/2393)).

---

## How to Choose

| If you need… | Start here |
|---|---|
| **Explicit control, audit trails, complex branching** | LangGraph |
| **Fast multi-agent prototyping ("team" metaphor)** | CrewAI |
| **TypeScript / typed workflows** | Mastra |
| **Lightweight, minimal abstraction** | OpenAI Agents SDK |
| **Realtime voice agents** | LiveKit Agents |
| **Research / AI-to-AI collaboration** | AutoGen (but note maintenance mode) |
| **Cross-system interop** | MCP + A2A |

**Golden rule:** Prototype fast, but budget for the production layer. Multiple sources (Gartner, ACM Queue, Stack Overflow 2026) report that **78–90% of agent projects stall or get re-architected** between demo and deployment — primarily due to the gaps above (state, recovery, observability, security) that frameworks don't solve out of the box.

---

## Sources

- [Fusefy — Agentic AI Frameworks Comparison](https://www.fusefy.ai/aivibes/guide-to-agentic-ai-frameworks/)
- [aiHola — Choosing an AI Agent Framework (6 major options)](https://aihola.com/article/ai-agent-frameworks-comparison-2025)
- [Agentik OS — Why AI Agent Frameworks Fail in Production](https://www.agentik-os.com/blog/the-real-reason-ai-agent-frameworks-fail-in-production)
- [arXiv 2511.14136 — Evaluating Agentic AI](https://arxiv.org/html/2511.14136v1)
- GitHub issue trackers: `langchain-ai/langgraph`, `crewAIInc/crewAI`, `microsoft/autogen`, `openai/openai-agents-python`, `mastra-ai/mastra`

---

## Contributing

PRs welcome! If you'd like to add a framework, fix a star count, or contribute a verified gap/issue reference, please open a pull request. Star counts are approximate and drift quickly — feel free to correct them.

---

*Last updated: September 2026. Star counts are approximate snapshots.*