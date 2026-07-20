# AGENTS.md — TA-app

Routing for non-Claude agents (Codex, Antigravity, Cursor, Gemini, Aider, …)
working in `TA-app`, the chat frontend of Talent Angels.

## Read first

1. `../CLAUDE.md` — **authoritative** project policy (git, DCO, secrets,
   conventions). On GitHub: `LFX-Talent-Angels/TA-workspace`.
2. `../docs/architecture/SYSTEM.md` — cross-repo architecture.
3. `CLAUDE.md` in this repo — boundaries. Keep both files in sync.

## Rules (summary)

- **Placeholder repo**: the frontend stack is undecided. Do not scaffold a
  framework without its ADR in `TA-workspace/docs/decisions/`.
- The app talks only to the FastAPI edge of `TA-agents`; never to the graphs.
- Branch + PR flow. Every commit DCO signed-off (`git commit -s`). Never push
  to `main`. Never commit `.env*` files or secrets.
