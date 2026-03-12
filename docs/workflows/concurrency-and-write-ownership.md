# Concurrency And Write Ownership

## Core Principle

Use **phase-parallel, file-serial** collaboration.

That means:

- agents may work in parallel on different artifact types
- agents should not edit the same file family, branch, or repo surface at the same time unless the work is intentionally coordinated

## Recommended Pattern

- Athena and Hermes can work in parallel on plans and research.
- Hephaestus owns implementation branches when code changes are underway.
- Themis can review in parallel, but should write findings into audit artifacts rather than editing implementation files directly.
- Final merge decisions should be explicit and serialized.

## Write Ownership

- planning docs: Athena
- research briefs and source maps: Hermes
- code and tests: Hephaestus
- findings, gates, and risk registers: Themis

## Why This Is Safer

- avoids file clobbering
- reduces hidden merge conflicts
- makes responsibility legible
- keeps audit trails clearer
