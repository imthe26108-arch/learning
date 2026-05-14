# Triage Labels Configuration

This repository uses the default triage label vocabulary.

## Label mapping

| Role | Label name | Purpose |
|------|------------|---------|
| `needs-triage` | `needs-triage` | Issue needs maintainer evaluation |
| `needs-info` | `needs-info` | Waiting on reporter for more information |
| `ready-for-agent` | `ready-for-agent` | Fully specified, ready for AI agent to pick up |
| `ready-for-human` | `ready-for-human` | Ready for human implementation |
| `wontfix` | `wontfix` | Issue will not be actioned |

## How skills use this

The `triage` skill moves issues through the state machine by applying these labels:

1. **New issue** → `needs-triage` (maintainer evaluates)
2. **Needs more info** → `needs-info` (waiting on reporter)
3. **Ready for work** → `ready-for-agent` or `ready-for-human` (based on complexity)
4. **Rejected** → `wontfix` (will not be worked on)

## Setting up labels

If these labels don't exist in your GitHub repository yet, you can create them using the GitHub UI or CLI:

```bash
gh label create "needs-triage" --color "#FFA500"
gh label create "needs-info" --color "#FFA500" 
gh label create "ready-for-agent" --color "#008000"
gh label create "ready-for-human" --color "#008000"
gh label create "wontfix" --color "#FF0000"
```