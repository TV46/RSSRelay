# RSSRelay 🛰️

RSSRelay merges multiple RSS/Atom feeds into one single `feed.rss`.

## Repo structure

```text
.
├── feeds.txt
├── relay.py
├── requirements.txt
├── feed.rss
└── .github/
    └── workflows/
        └── update.yml
```

## How it works

1. Put feed URLs in `feeds.txt` (one per line).
2. Run `python relay.py`.
3. The combined feed is written to `feed.rss`.

## Local usage

```bash
pip install -r requirements.txt
python relay.py
```

## Automation

The GitHub Actions workflow at `.github/workflows/update.yml`:
- runs every day at **00:00 UTC**
- supports **manual runs** via `workflow_dispatch`
- commits updated `feed.rss` back to the repository

Happy relaying! 🎉
