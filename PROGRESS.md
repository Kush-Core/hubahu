# Progress

## Current
- Stage: prerequisites and repo setup
- Next step: create the public GitHub repo and push; then pre-commit with Ruff

## Done
- 2026-10-25: Machine inventory (macOS, Apple M1, 8 GB RAM, Docker VM 3.83 GiB).
- 2026-10-25: uv workspace at `backend/` with members core, api, worker;
  boundary verified (worker-only env cannot import hubahu_api).

## Decisions
- uv workspace lives in `backend/`; frontend will live in `frontend/` (built with Claude Code).
- Claude Code is used only for the frontend.

## Open risks
- pynini 2.1.7 has no Linux arm64 or macOS wheels (verified on PyPI). Decide in the normalization spike.
- 8 GB RAM and a 3.83 GiB Docker VM may not fit the 600M fp32 model. Decide in the speed spike.
- Neon minimum compute size: unverified. Confirm in the Neon console.

## Later (out of scope for v1)
- (none yet)
