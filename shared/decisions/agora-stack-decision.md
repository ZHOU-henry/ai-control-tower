# Agora Stack Decision

## Decision

For `Agora` phase 1, use a **TypeScript-first monorepo** with:

- `pnpm workspaces` for package management
- `Turborepo` for task orchestration and caching
- `Next.js 16 App Router` for the web application
- `Fastify + TypeScript` for the API service
- `PostgreSQL` as the system of record
- `Prisma ORM` for database access and schema management

## Why This Stack

### 1. It matches the actual MVP shape

`Agora v0` is not a generic marketplace infrastructure product yet.

It needs to ship:

- an operator-facing web surface
- a task intake flow
- an execution record
- a reviewable data model

That is much closer to a modern product application than to a high-performance distributed systems problem.

### 2. It is fast enough to build and clear enough to maintain

Using TypeScript across web, API, and shared types minimizes coordination tax between Athena, Hermes, Hephaestus, and Themis.

For phase 1, reducing language and toolchain fragmentation is a higher-leverage choice than prematurely optimizing for maximum backend performance.

### 3. It leaves room for later specialization

This choice does **not** forbid Rust later.

If `Agora` eventually needs:

- high-throughput execution workers
- specialized runtime isolation
- heavier event processing
- low-latency systems components

those can be added later without making phase 1 slower now.

## Technical Shape

### Monorepo

- package manager: `pnpm workspaces`
- task runner: `Turborepo`

Reason:

- shared contracts and schemas will matter early
- monorepo coordination is simpler for a small, agent-assisted team

### Web

- framework: `Next.js 16 App Router`
- language: `TypeScript`

Reason:

- strong fit for operator-facing UI and server/client split
- modern React/Server Component model is now the normal path in the official docs
- good fit for catalog, task detail, execution record, and review surfaces

### API

- runtime: `Node.js 22`
- framework: `Fastify`
- language: `TypeScript`

Reason:

- explicit API boundary remains useful even with a strong web framework
- agent runs, task state changes, provenance checks, and execution records are cleaner behind a dedicated service boundary
- Fastify is lightweight, mature, and TypeScript-friendly

### Database

- `PostgreSQL` as the primary system of record
- `Prisma ORM` for schema and query layer

Reason:

- the product is naturally relational:
  - agents
  - tasks
  - runs
  - reviews
  - provenance records
- phase 1 benefits more from clarity and migrations than from exotic storage choices

### Queue / Background Work

- start with database-backed task state and background job discipline
- do **not** require Redis or a broker in phase 1

Reason:

- background work exists, but infra complexity should not outrun product proof

## What We Are Explicitly Not Choosing Now

### Not Rust for the phase-1 API

Rust is attractive, but for this phase it adds:

- language fragmentation
- slower iteration across product and schema changes
- more coordination overhead for AI-assisted implementation

This is a timing decision, not a rejection of Rust.

### Not a single giant Next.js-only backend

A pure full-stack Next app is tempting, but we want a clearer operational boundary for:

- run state
- execution records
- future webhooks
- future background work

### Not microservices

Phase 1 does not need distributed systems theater.

### Not Redis-first infrastructure

Premature queue or cache complexity is more likely to slow us down than help us.

## Source Notes

- Next.js App Router docs  
  https://nextjs.org/docs/app
- Next.js 16 release notes  
  https://nextjs.org/blog/next-16
- Fastify TypeScript docs  
  https://fastify.dev/docs/latest/Reference/TypeScript/
- Prisma PostgreSQL docs  
  https://docs.prisma.io/docs/orm/core-concepts/supported-databases/postgresql
- Prisma Postgres docs  
  https://docs.prisma.io/docs/postgres
- pnpm docs  
  https://pnpm.io/
- Turborepo basics  
  https://docs.vercel.com/academy/production-monorepos/turborepo-basics
- PostgreSQL docs  
  https://www.postgresql.org/docs/

## Final Position

For phase 1, the best stack is the one that lets us ship a clear, inspectable, provenance-aware product fastest without painting ourselves into a corner.

That stack is:

**Next.js 16 + Fastify + PostgreSQL + Prisma in a pnpm/Turborepo monorepo.**
