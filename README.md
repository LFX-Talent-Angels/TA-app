# TA-app

> **Talent Angels** chat frontend — the app where users talk to the assistant.

Part of the [`LFX-Talent-Angels`](https://github.com/LFX-Talent-Angels) org. For
project-wide docs, onboarding, and rules, see
[`TA-workspace`](https://github.com/LFX-Talent-Angels/TA-workspace).

## Status: placeholder

This repo reserves the app's place in the architecture (see ADR-0004 and
`TA-workspace/docs/architecture/SYSTEM.md`). **No frontend stack has been
chosen yet** — that decision gets its own ADR when frontend work starts.

What is already decided (by the system architecture):

- The app talks to the assistant runtime in
  [`TA-agents`](https://github.com/LFX-Talent-Angels/TA-agents) through its
  **thin FastAPI edge** — all reasoning stays server-side in the agent loop.
- The app never queries taxonomy graphs directly; suites are an internal
  concern of `TA-taxonomies`.

## Contributing

Same rules as every Talent Angels repo: branch, `git commit -s` (DCO), open a
PR, request a mentor review. See the workspace
[`CONTRIBUTING.md`](https://github.com/LFX-Talent-Angels/TA-workspace/blob/main/CONTRIBUTING.md).

## License

Apache-2.0 — see [`LICENSE`](./LICENSE).
