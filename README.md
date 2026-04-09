# HuggingFace Download Stats Tracker

Automatically tracks daily download counts for all your models and datasets on the HuggingFace Hub.

## Features

- Per-model and per-dataset download tracking
- Daily aggregated totals with historical CSV logs
- Auto-generated dashboard in `logs/README.md`
- GitHub Actions cron job for daily updates
- Manual trigger via `workflow_dispatch`

## Setup

1. Fork/clone this repo
2. Edit `hf_download_stats.py` — change `--author` default to your HF username
3. Push to GitHub — the Action runs daily at 9:07 AM UTC

## Manual Run

```bash
pip install huggingface_hub

# Print stats to terminal
python hf_download_stats.py

# Print + log to CSV + update dashboard
python hf_download_stats.py --log

# Different user
python hf_download_stats.py --author your-username --log
```

## Output Files

| File | Description |
|------|-------------|
| `logs/README.md` | Dashboard with latest stats tables |
| `logs/downloads_per_repo.csv` | Per-repo daily downloads |
| `logs/downloads_daily.csv` | Aggregated daily totals |

## Dashboard

See [logs/README.md](logs/README.md) for the latest stats.
