# Agora v0 Scope Decision

## Decision

`Agora v0` should be defined as an **AI Agent Platform MVP**, not a full two-sided marketplace.

## Why

The current agent ecosystem is already crowded with:

- agent development frameworks
- orchestration frameworks
- deployment and management platforms
- workflow builders

What is still weak across the landscape is a clean, operator-facing loop that lets users:

1. discover a vetted agent capability
2. understand what it is for
3. run or route a task through it
4. review the execution record
5. decide whether it is worth deeper adoption

That loop is much more realistic for v0 than trying to solve full marketplace liquidity, pricing, settlement, and enterprise trust all at once.

## Product Definition

Agora v0 is an open-source AI Agent platform prototype with four core surfaces:

1. **Agent Catalog**
   A curated listing of agent capabilities, tags, descriptions, source references, and operational constraints.
2. **Task Intake**
   A lightweight way to submit a need, route it to an agent workflow, and track the request state.
3. **Execution Record**
   A visible trace of what happened, what tools were used, and what output was produced.
4. **Operator Review**
   A simple review layer for status, quality notes, and reuse confidence.

## v0 In Scope

- curated agent listings
- task submission and routing
- basic execution record / run history
- operator-facing review panel
- lightweight quality and provenance indicators

## v0 Out Of Scope

- open marketplace liquidity mechanics
- automated pricing and revenue distribution
- on-chain settlement
- trusted execution hardware
- full enterprise tenancy and policy engine
- generalized multi-agent economy claims

## Success Criteria

- a user can understand what an agent does before running it
- a user can submit a task and receive a tracked result
- a user can inspect the execution record after the run
- the system can display enough metadata to support trust and reuse decisions
- the implementation boundary is small enough to scaffold and demo quickly

## Strategic Consequence

Agora should be built first as an **operator-grade AI Agent platform**.

If that works, marketplace mechanics can be layered later.

If we try to build the marketplace first, we risk building a shell with no trustworthy core.
