# Agora Market Brief - 2026-03-13

## Question

What should `Agora` be in phase 1, given the current state of the agent ecosystem?

## Executive Summary

The current landscape strongly supports **frameworks**, **orchestration**, and **deployment platforms**, but does not by itself justify pretending that the first winning move is a fully generalized agent marketplace.

The better phase-1 position is:

- not "build a giant market"
- but "build an operator-facing AI Agent platform with curation, execution visibility, and reuse confidence"

This is a narrower and more defensible product wedge.

## Main Findings

### 1. Framework and orchestration are already crowded

Current open-source attention is concentrated around agent frameworks and orchestration stacks, not around successful neutral agent marketplaces.

GitHub snapshots collected on 2026-03-13:

- `microsoft/autogen` — 55k+ stars  
  URL: https://github.com/microsoft/autogen
- `crewAIInc/crewAI` — 45k+ stars  
  URL: https://github.com/crewAIInc/crewAI
- `langchain-ai/langgraph` — 26k+ stars  
  URL: https://github.com/langchain-ai/langgraph
- `openai/openai-agents-python` — 19k+ stars  
  URL: https://github.com/openai/openai-agents-python

Interpretation:

- the ecosystem already has serious supply of ways to build agents
- what remains weak is not "can I define an agent?" but "how do I operate, evaluate, and trust one in a practical workflow?"

### 2. The major platforms focus on deployment and operations

OpenAI's Agents SDK describes agentic applications as workflows with tools, handoffs, traces, and specialized agents.  
Source: OpenAI Agents SDK docs  
URL: https://developers.openai.com/api/docs/guides/agents-sdk

OpenAI's practical guide warns against premature complexity and recommends maximizing a single agent before adding more agents. It also frames manager and handoff patterns as orchestration choices rather than product strategy.  
Source: OpenAI practical guide PDF, pages 13-16 and 23-27  
URL: https://cdn.openai.com/business-guides-and-resources/a-practical-guide-to-building-agents.pdf

Relevant points:

- start incrementally
- add agents only when complexity justifies them
- layered guardrails matter

Interpretation for Agora:

- phase 1 should not pretend to solve every orchestration and governance problem at once
- it should expose a simple, understandable execution loop

### 3. Existing commercial/managed offerings emphasize deploy-monitor-scale

CrewAI AMP explicitly presents itself as an agent management platform for deploying, monitoring, scaling, and integrating crews, with GitHub integration and observability.  
Source: CrewAI AMP docs  
URL: https://docs.crewai.com/en/enterprise/introduction

LangGraph platform deployment docs emphasize deployment workflow, durable execution, retries, replay, and operational infrastructure.  
Source: LangGraph / LangSmith deployment docs  
URL: https://docs.langchain.com/langsmith/deployments

Microsoft Agent Framework documentation emphasizes building, memory, workflows, hosting, and migration paths.  
Source: Microsoft Learn Agent Framework docs  
URL: https://learn.microsoft.com/en-us/agent-framework/

Interpretation:

- the current market bias is toward infrastructure and operations
- there is room for a clearer product layer focused on discoverability, execution visibility, and trust signals

### 4. The biggest early product risk is fake marketplace scope

A full marketplace requires:

- supply liquidity
- demand liquidity
- trust
- ranking
- evaluation
- standard metadata
- commercial mechanics

Trying to solve all of that in v0 is the fastest way to ship a polished empty shell.

## Product Implication

Agora phase 1 should be an **AI Agent Platform MVP** with:

- curated agent catalog
- task intake and routing
- execution record
- operator review and trust signals

It should **not** start as:

- a generalized app store
- a revenue sharing system
- an enterprise policy monster

## Source Reliability Notes

- OpenAI, Microsoft, CrewAI, and LangChain docs are first-party product or framework sources.
- GitHub repo metadata is useful for current ecosystem attention, but star counts are a signal, not proof of product-market fit.
- No paid analyst reports were used in this draft.

## Risks And Caveats

- This brief is ecosystem-structure evidence, not direct customer interview evidence.
- We still need user-side validation on which workflow hurts most:
  - discovery
  - selection
  - execution
  - review
- We should avoid overstating "market demand" until Hermes gathers direct use-case evidence.

## Recommendation

Lock `Agora v0` as:

**An operator-facing AI Agent platform prototype with curation, execution visibility, and reuse confidence.**

That is a sharper wedge than "the marketplace for all agents."
