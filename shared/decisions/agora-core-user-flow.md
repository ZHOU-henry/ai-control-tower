# Agora Core User Flow

## Decision

`Agora v0` should optimize for a single operator loop:

1. **Discover**
   The user browses a curated agent catalog and understands what an agent is for.
2. **Select**
   The user chooses an agent based on capability, constraints, and trust signals.
3. **Submit**
   The user creates a task request with enough context to run the workflow.
4. **Observe**
   The user watches the execution record, status changes, and outputs.
5. **Review**
   The user judges whether the result is reusable, acceptable, or needs escalation.

## Why This Flow

This flow matches the strongest defensible wedge for phase 1:

- curation
- execution visibility
- reuse confidence

It does **not** require solving:

- marketplace liquidity
- pricing
- provider reputation at internet scale
- generalized multi-tenant policy systems

## Phase-1 Screens Implied By This Flow

### 1. Catalog

Shows:

- agent name
- summary
- tags
- trust / provenance indicators
- constraints and ideal use cases

### 2. Agent Detail

Shows:

- what the agent does
- what data or tools it needs
- what kinds of tasks fit
- example tasks

### 3. Task Intake

Lets the user:

- choose an agent
- enter a task
- attach optional context
- submit the run

### 4. Run Detail

Shows:

- current status
- execution timeline
- outputs
- warnings or escalation

### 5. Operator Review

Lets the user:

- mark the result useful or not
- capture review notes
- decide whether to rerun, escalate, or reuse

## Product Rule

If a feature does not make this loop clearer, faster, or more trustworthy in phase 1, it probably should not be in scope yet.
