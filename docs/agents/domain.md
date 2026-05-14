# Domain Documentation Configuration

This repository uses **single-context** layout for domain documentation.

## Layout

```
repo-root/
├── CONTEXT.md           # Main domain language and concepts
└── docs/
    └── adr/            # Architectural Decision Records
        ├── 0001-some-decision.md
        └── ...
```

## How skills use this

- `improve-codebase-architecture` — Reads `CONTEXT.md` to understand domain language, then suggests improvements
- `diagnose` — Consults `CONTEXT.md` when debugging to understand system behavior
- `tdd` — References `CONTEXT.md` to ensure tests align with domain concepts
- `grill-with-docs` — Validates plans against `CONTEXT.md` and ADRs

## Reading rules

1. **Always read `CONTEXT.md` first** — Contains the current domain model and terminology
2. **Check `docs/adr/` for historical decisions** — ADRs document why past choices were made
3. **Prefer `CONTEXT.md` over ADRs** for current understanding (ADRs may be outdated)
4. **Look for section headers** that match the area you're working on

## Creating domain docs

If `CONTEXT.md` doesn't exist yet, skills will create it based on the conversation context. ADRs should be created when making significant architectural decisions that future maintainers need to understand.