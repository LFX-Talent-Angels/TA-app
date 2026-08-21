# AGENTS.md — TA-app

The **chat frontend** of Talent Angels. Currently a **placeholder** — the
frontend stack is not chosen yet and will be decided via its own ADR when
frontend work starts.

This file is the source of truth for humans and for every AI coding agent
(Claude Code, Codex, Cursor, Antigravity, Gemini, Aider, and any other).
`CLAUDE.md` is a one-line import of this file.

This is a **subrepo** of the Talent Angels workspace.

## Read first

1. The workspace policy: `../AGENTS.md`
   (or https://github.com/LFX-Talent-Angels/TA-workspace → `AGENTS.md`).
   It is **authoritative** — branch flow, DCO, secrets, agent conventions.
2. `../docs/architecture/SYSTEM.md` — cross-repo architecture.

## Boundaries (already decided by the system architecture)

- The app consumes the **FastAPI edge** exposed by `TA-agents` — nothing else.
  All reasoning stays server-side; this app renders conversation and results.
- Never query taxonomy graphs or import `ta_taxonomies` from here.
- Do not choose or scaffold a frontend framework without the corresponding
  ADR in `TA-workspace/docs/decisions/`.

## Branches and pull requests

| Branch | What it is        | To merge into it                            |
| ------ | ----------------- | ------------------------------------------- |
| `dev`  | Integration trunk | 1 approval from any contributor + green CI  |
| `main` | What we publish   | 1 approval **from a code owner** + green CI |

- **Open every pull request against `dev`.** `main` only receives promotions
  from `dev`.
- Never push directly to `dev` or `main`.
- **Every commit signed off**: `git commit -s` (DCO). Pull requests without it
  are blocked.
- Without write access, fork and open the pull request from your fork. With
  write access, push the branch to this repo directly.
- Never commit `.env*` files or secrets.

Full details in the workspace `AGENTS.md` and `CONTRIBUTING.md`.
