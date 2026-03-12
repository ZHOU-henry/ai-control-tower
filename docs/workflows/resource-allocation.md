# Resource Allocation

## Principle

Do not distribute effort equally just because there are four agents.

## Current Allocation Logic

- Athena: high leverage, moderate write volume
- Hermes: moderate compute, high source validation cost
- Hephaestus: highest sustained implementation load
- Themis: high reasoning load on narrower scopes

## Practical Decision

If stronger models, longer runtimes, or heavier context windows become scarce, bias them toward:

1. Hephaestus
2. Themis
3. Athena
4. Hermes

This is because code implementation and serious review are usually the tightest execution bottlenecks.

## Current Constraint

Right now all agents already run on the strongest available configured model. Keep the policy documented first; optimize runtime allocation only when it becomes a measurable bottleneck.
