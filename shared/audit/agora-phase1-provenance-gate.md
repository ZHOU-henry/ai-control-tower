# Agora Phase 1 Provenance And Release Gate

## Purpose

Define the minimum provenance, license, and release discipline required before `Agora` phase-1 work is treated as merge-ready or demo-ready.

## Gate Scope

This gate applies to:

- code imported or adapted from outside repositories
- copied snippets from docs or articles
- external UI assets or icons
- datasets, prompts, examples, and templates
- technical claims used in product framing

## Severity Model

### Blocker

Must stop merge or release:

- upstream source has no license
- license terms are unclear
- required notice or attribution is missing
- imported material appears incompatible with planned use
- security or provenance of the source cannot be established

### Major

Must be resolved or explicitly accepted:

- provenance is incomplete
- source is known but not recorded in repo artifacts
- copied behavior is undocumented
- third-party dependency choice introduces avoidable legal or operational risk

### Minor

Can merge with follow-up:

- attribution wording needs cleanup
- a provenance record exists but is not yet normalized
- references are valid but not yet summarized for reuse

## Minimum Merge Requirements

1. Every imported third-party code or asset has a clear source URL.
2. The upstream license is recorded.
3. Required attribution or NOTICE obligations are preserved.
4. No `no license` code is copied into the repo.
5. Any GPL/AGPL/LGPL or unclear-license material is escalated before import.
6. Product or technical claims tied to external evidence cite the source.

## Minimum Demo / Release Requirements

1. Core scope is stable enough to explain honestly.
2. Known blocker-class provenance issues are zero.
3. Major provenance issues are zero or explicitly accepted by Henry.
4. The execution record and trust signals shown in the demo are real, not faked.
5. The product does not claim marketplace completeness, enterprise readiness, or compliance guarantees it does not actually have.

## Preferred Reuse Pattern

- learn from outside work
- cite it
- reimplement cleanly where practical
- copy only when the license is clearly compatible and the obligations are manageable

## Current Agora Phase-1 Interpretation

Allowed by default:

- inspiration from official docs and clearly licensed repos
- permissive-license code reuse with preserved obligations
- summarized research from first-party docs and public repo metadata

Not allowed by default:

- copying from repositories without a clear license
- copying tutorial/demo code into production paths without provenance notes
- importing assets or datasets without usage rights
