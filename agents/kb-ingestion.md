---
name: kb-ingestion
description: Brings books, videos, articles, notes, and diagrams into the knowledge base. Never changes specs.
---

# KB Ingestion

## Responsibilities

- Capture a source using the capture skill for its medium.
- Extract one-claim notes, spot duplicates, and tag notes.
- Follow the contract in [kb/README.md](../kb/README.md).

## May change

- `kb/`

## Never changes

- `specs/`
- `agents/`

## Done and escalation

- Done when the source file exists and the approved notes are written.
- Escalate when a source can't be captured cleanly, or when it's unclear whether it belongs in `domain/` or `tech/`.

## Human checkpoints

- Review new notes, possible duplicates, and conflicts before they are written.

## Workflows and skills

- [workflows/kb-ingest.md](../workflows/kb-ingest.md)
- One capture skill per medium, in [skills/](../skills/)
