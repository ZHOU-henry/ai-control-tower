# Agora Use-Case Evidence - 2026-03-13

## Question

What user-side workflows are repeatedly emphasized by major agent platforms, and what do those patterns imply for `Agora v0`?

## Executive Summary

Across major official agent platforms, the repeated themes are:

- answer questions with grounded knowledge
- automate repetitive service or employee workflows
- route or execute tasks
- provide visibility, governance, or evaluation

This supports `Agora v0` focusing on:

- discoverability
- task intake
- execution visibility
- operator review

not on speculative marketplace mechanics.

## Main Evidence

### 1. OpenAI frames agents around workflows, data, actions, and orchestration

OpenAI's practical guide defines agents as systems that independently accomplish tasks on a user's behalf and gives examples like resolving customer service issues, booking reservations, committing code changes, or generating reports. It highlights:

- **data access** for context
- **action** for system interaction
- **orchestration** for workflow execution

Source:

- OpenAI practical guide to building agents  
  https://openai.com/business/guides-and-resources/a-practical-guide-to-building-ai-agents/

Implication for Agora:

- users need a visible path from request -> execution -> result
- pure chat without workflow structure is not enough

### 2. Microsoft positions agents as expert systems that answer, act, automate, and escalate

Microsoft describes agents as expert systems that:

- answer user questions by retrieving or summarizing information
- take actions and automate workflows
- operate independently and escalate

It also emphasizes deployment across channels and responsible AI / governance.

Sources:

- Microsoft Copilot Studio  
  https://www.microsoft.com/en-us/microsoft-365-copilot/microsoft-copilot-studio
- Microsoft Learn: Copilot Studio fundamentals  
  https://learn.microsoft.com/en-us/microsoft-copilot-studio/fundamentals-what-is-copilot-studio

Implication for Agora:

- agent records need to make capability and limits understandable
- task routing and escalation should be first-class concepts

### 3. Salesforce emphasizes trusted self-service, grounded responses, and business workflow execution

Salesforce highlights:

- autonomous AI for self-service
- answering customers across channels
- grounding responses in trusted business data
- order status, returns, account management, knowledge access, and repetitive service workflows

Sources:

- Agentforce use cases  
  https://www.salesforce.com/agentforce/use-cases/
- Salesforce Service AI / Agentforce pages  
  https://www.salesforce.com/service/ai/

Implication for Agora:

- users care about practical operational jobs, not abstract agent theory
- trust signals and execution visibility matter as much as raw model capability

### 4. Atlassian Rovo explicitly surfaces agent browse, profiles, permissions, evaluation, and verification

Atlassian documents product surfaces for:

- browsing agents
- viewing agent profiles
- permissions and governance
- tracking usage
- evaluating performance
- verification status

Source:

- Atlassian Rovo agents support docs  
  https://support.atlassian.com/rovo/docs/agents/

Implication for Agora:

- the catalog itself is not fluff; it is part of the product
- agent profile, evaluation, and verification patterns are real product primitives

## Product Synthesis

The ecosystem evidence points to a consistent phase-1 model:

1. user identifies a suitable agent
2. user submits a bounded task
3. system runs or routes the work
4. user inspects what happened
5. user decides whether to trust, reuse, or escalate

## Recommendation

Use this user-side shape as the main Agora product loop:

- Catalog
- Task Intake
- Run Record
- Operator Review

That is the most evidence-aligned path for phase 1.

## Caveat

This evidence comes from first-party platform positioning and product documentation. It is strong for identifying recurring patterns, but it is not a substitute for direct customer interviews or usage analytics.
