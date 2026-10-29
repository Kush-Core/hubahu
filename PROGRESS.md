# Progress

## Current
- Stage: de-risking spikes
- Next step: model access and outputs — accept the model's terms on Hugging Face,
  create a read-scoped token (stored outside the repo), download the ONNX assets into `models/`

## Done
- 2026-10-25: Prerequisites and repo stage complete.
- 2026-10-25: Machine inventory (macOS, Apple M1, 8 GB RAM, Docker VM 3.83 GiB).
- 2026-10-25: uv workspace at `backend/` with members core, api, worker;
  boundary verified (worker-only env cannot import hubahu_api).
- 2026-10-25: Public repo github.com/Kush-Core/hubahu (MIT), `main` pushed.
- 2026-10-25: pre-commit with Ruff 0.16.10 and repo hygiene hooks.
- 2026-10-29: Verified Ruff uses `backend/pyproject.toml` for all members.

## Decisions
- uv workspace lives in `backend/`; frontend will live in `frontend/` (built with Claude Code).
- Claude Code is used only for the frontend.

## Open risks
- pynini 2.1.7 has no Linux arm64 or macOS wheels (verified on PyPI). Decide in the normalization spike.
- 8 GB RAM and a 3.83 GiB Docker VM may not fit the 600M fp32 model. Decide in the speed spike.
- Neon minimum compute size: unverified. Confirm in the Neon console.
- ONNX audio preprocessor may be TorchScript (needs CPU PyTorch). Check `model_onnx.py` in the model spike.
