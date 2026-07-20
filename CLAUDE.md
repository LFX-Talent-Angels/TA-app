# TA-app

The **chat frontend** of Talent Angels. Currently a **placeholder** — the
frontend stack is not chosen yet and will be decided via its own ADR when
frontend work starts.

This is a **subrepo** of the Talent Angels workspace.

## Read first

1. The workspace policy: `../CLAUDE.md`
   (or https://github.com/LFX-Talent-Angels/TA-workspace → `CLAUDE.md`).
   It is **authoritative** — git rules, DCO, secrets, agent conventions.
2. `../docs/architecture/SYSTEM.md` — cross-repo architecture.

## Boundaries (already decided by the system architecture)

- The app consumes the **FastAPI edge** exposed by `TA-agents` — nothing else.
  All reasoning stays server-side; this app renders conversation and results.
- Never query taxonomy graphs or import `ta_taxonomies` from here.
- Do not choose or scaffold a frontend framework without the corresponding
  ADR in `TA-workspace/docs/decisions/`.

## Git

Branch + PR, **`git commit -s`** (DCO). Never push to `main`. Full rules in the
workspace `CLAUDE.md` and `CONTRIBUTING.md`.
