# Portfolio Domain Architecture

## Goal

Use one company root domain to host the full MVP portfolio while keeping each
product clearly legible as its own public surface.

## Recommended Pattern

Do **not** use:

- `company.Agora.com`
- `company.Noesis.com`

Use:

- `company.com` as the root company domain
- `agora.company.com`
- `noesis.company.com`
- `peras.company.com`
- `physis.company.com`
- `titan.company.com`

This is the standard and manageable structure.

## Recommended Surface Split

- `company.com`
  - corporate / portfolio homepage
- `agora.company.com`
  - agent marketplace and delivery operating system
- `noesis.company.com`
  - AGI symbiosis observatory
- `peras.company.com`
  - frontier signal engine
- `physis.company.com`
  - physical AI / robotics framework
- `titan.company.com`
  - autonomous robotics control program

## Optional Service Subdomains

If needed later:

- `api.agora.company.com`
- `docs.noesis.company.com`
- `data.peras.company.com`

But do not add these until they solve a real problem.

## Runtime Recommendation Under Current Budget

- one root domain
- Cloudflare DNS / proxy
- one Hong Kong cloud server
- one nginx reverse proxy
- multiple subdomain host rules

This keeps cost and management low while preserving a coherent company-level
portfolio identity.

## Why This Design Works

- one domain purchase
- clear project separation
- obvious company ownership
- scalable to future MVPs
- manageable DNS and reverse-proxy structure
