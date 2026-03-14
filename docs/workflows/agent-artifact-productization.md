# Agent Artifact Productization

## Goal

Turn the 5-agent operating model into explicit reusable artifacts rather than relying on implicit coordination.

## Artifact Flow

1. `Ashley/main` creates a synthesis frame.
2. `Athena/CPO` converts that frame into a dispatch artifact.
3. `Hermes/research` produces a structured research brief.
4. `Hephaestus/dev` works from an explicit dev work order.
5. `Themis/audit` closes the loop through an audit gate artifact.

## Template Source

Use:

- `shared/templates/main-agent-synthesis-template.md`
- `shared/templates/cpo-dispatch-template.md`
- `shared/templates/research-brief-template.md`
- `shared/templates/dev-work-order-template.md`
- `shared/templates/audit-gate-template.md`

## Why It Matters

- keeps agent roles explicit
- keeps shared memory in explicit artifacts instead of hidden chat state
- makes multi-agent work inspectable, teachable, and reusable
