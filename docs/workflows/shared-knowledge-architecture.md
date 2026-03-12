# Shared Knowledge Architecture

## Goal

Share useful project artifacts across agents without collapsing their private memory into one pool.

## Two-Layer Model

### 1. Curated Shared Layer

Use the versioned control-tower repo for cleaned, reusable artifacts:

- `shared/research/`
- `shared/decisions/`
- `shared/audit/`

These are meant to be read by all agents.

### 2. Raw Intake Layer

Use the local non-repo intake area for raw downloads and uncertain external material:

- `/Users/henry/projects/_intake/raw/`
- `/Users/henry/projects/_intake/license-reviews/`
- `/Users/henry/projects/_intake/staging/`

This layer is not "memory." It is a quarantine and intake zone.

## Important Boundary

- Private agent memory stays private.
- Shared repo artifacts are explicit collaboration artifacts.
- Raw intake should not be auto-promoted into shared knowledge until provenance and usefulness are reviewed.
