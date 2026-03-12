# Memory Hygiene

## Goal

Keep agent context durable without letting memory files grow into unreadable sludge.

## Rule Of Layers

- `memory/YYYY-MM-DD.md`
  Raw daily notes, observations, and execution traces.
- `ACTIVE-CONTEXT.md`
  Only the current phase, current priorities, and active constraints.
- `MEMORY.md`
  Durable facts, preferences, lessons, and long-lived operating truths.
- `PROJECT-CHARTER.md`
  Mission, scope, sequencing, and non-goals.

## Promotion Rule

If something still matters after 5-10 days:

- move it into `ACTIVE-CONTEXT.md` if it is still active work
- move it into `MEMORY.md` if it is durable truth
- move it into `PROJECT-CHARTER.md` if it changes mission or scope

## Retention Rule

- Do not auto-delete old daily notes.
- Do not make startup prompts reread all history.
- Review weekly, summarize, then archive only with explicit intent.
