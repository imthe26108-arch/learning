# Issue Tracker Configuration

This repository uses **GitHub Issues** for tracking work items.

## How skills use this

- `to-issues` — Converts plans into GitHub issues using `gh issue create`
- `triage` — Reads from and writes to GitHub issues, applying labels
- `to-prd` — Creates GitHub issues for PRDs
- `qa` — Reads test plans from GitHub issues

## GitHub Issue workflow

Issues are created in this repository's GitHub Issues page and managed using the GitHub CLI (`gh`). All issue operations (create, read, update, comment, close) are performed through standard GitHub functionality.

No special configuration needed — the skills use your default GitHub authentication.