# Agents Guide

This file is the platform-neutral entry point for any AI assistant or agent platform working in this repository. Platform-specific files (for example `CLAUDE.md` or `.claude/`) only point here and bind tools; they add no rules of their own.

## Project Map

- [specs/day-trading/](specs/day-trading/) — the specs every agent follows, plus the knowledge base in [kb/](specs/day-trading/kb/)
- [skills/](skills/) — reusable capabilities (`skills/<name>/SKILL.md`, optional `scripts/`)
- [workflows/](workflows/) — repeatable step-by-step procedures (`workflows/<name>.md`)
- [reference/](reference/) — feature definitions and agent interface contracts

## Agents

Every agent is a row in this table and follows one spec. Permissions, approvals, and output formats are defined in the spec, not here.

| Agent | Spec | Needs (generic) | May change | Never changes |
|---|---|---|---|---|
| Strategic | [strategic.md](specs/day-trading/strategic.md) | read specs, logs | its logs, gap flags | any spec |
| Execution | [execution.md](specs/day-trading/execution.md) | read specs, broker access | its logs, gap flags | any spec |
| Observability | [observability.md](specs/day-trading/observability.md) | read specs, market data | its logs, gap flags | any spec |
| Collaboration | [collaboration.md](specs/day-trading/collaboration.md) | read specs, notifications | its logs, gap flags | any spec |
| Review | [review.md](specs/day-trading/review.md) | read specs, logs, trade history | its logs, reports, gap flags | any spec |
| KB ingestion | [kb-ingestion.md](specs/day-trading/kb-ingestion.md) | read/write files, web, shell, images | `specs/day-trading/kb/` | any spec |
| Spec maintenance | [spec-maintenance.md](specs/day-trading/spec-maintenance.md) | read/write files | proposed spec changes (human approves) | `specs/day-trading/kb/` |

**Gap flags**: feature agents never edit their own spec. When a spec is vague or wrong in practice, they record a gap flag for the spec maintenance agent. Location: [to be decided].

## Workflows

| Workflow | Run by |
|---|---|
| [kb-ingest.md](workflows/kb-ingest.md) | KB ingestion |
| [spec-update.md](workflows/spec-update.md) | Spec maintenance |

## Skills

None defined yet. Add each skill as `skills/<name>/SKILL.md` and list it here. The Python modules in `skills/core/` are early examples and not yet part of this model.

## Conventions

- Workflows, skills, and specs use generic capability names, never platform-specific tool names.
- Platform hooks contain only pointers and tool wiring.
