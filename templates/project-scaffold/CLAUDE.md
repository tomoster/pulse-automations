# [Client Name] — Pulse Systems Project

WAT framework. Workflows define what to do, tools execute deterministically.

## Structure
- `workflows/` — Markdown SOPs
- `tools/` — Python scripts (one job each, testable, reusable)
- `.tmp/` — Disposable intermediate files
- `.env` — Credentials (gitignored)

## Rules
- Check `tools/` before building new scripts
- Fix errors by updating the tool AND the workflow
- Keep this file minimal — only add corrections for consistent mistakes
