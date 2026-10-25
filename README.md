# Hubahu

Hubahu checks Hindi audio episodes against their scripts and reports only the places
where the audio does not say what the script says: skipped lines, misread words or
numbers, wrong names, and repeated content. Each flag has a timestamp and a short clip.

**Status:** v1 in development. See [PROGRESS.md](PROGRESS.md).

## Repository layout

| Path | Contents |
|---|---|
| `backend/` | uv workspace (Python 3.12) |
| `backend/core/` | Pure logic: normalization, CTC alignment, flagging, report models |
| `backend/api/` | HTTP API: auth, uploads, jobs, quotas, reports |
| `backend/worker/` | Job worker: decode, VAD, CTC inference, alignment |
| `docs/adr/` | Architecture decision records |

## Development

```bash
cd backend
uv sync --all-packages
```

## Architecture, measured numbers, limitations

To be written from measured results before the v1.0.0 release.