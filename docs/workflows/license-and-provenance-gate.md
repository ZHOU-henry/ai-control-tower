# License And Provenance Gate

## Purpose

Prevent the portfolio from drifting into license or attribution problems while reusing open-source material.

## Gate Questions

1. Does the upstream material have a clear license?
2. Is that license compatible with how we want to use the material?
3. Are attribution, notice, and copyright obligations preserved?
4. Are there patent or trademark constraints that matter here?
5. Are we reusing the code itself, or only learning from the idea?

## Default Decisions

- `No license` -> do not copy
- `MIT / BSD / ISC / Apache-2.0` -> usually workable, still preserve obligations
- `GPL / AGPL / LGPL` -> stop and review before import
- unclear docs, datasets, assets, or models -> stop and review before import

## Preferred Pattern

- cite the source
- record provenance
- reimplement cleanly when possible
- only copy when the license clearly permits it and the compliance burden is acceptable
