# Agents Guide

This is the platform-neutral entry point for any AI assistant or agent platform working in this repository. Platform files (such as `CLAUDE.md` or `.claude/`) only point here and bind tools. They add no rules of their own.

## Project map

- [agents/](agents/): one file per agent, with its responsibilities, permissions, and checkpoints
- [workflows/](workflows/): repeatable step-by-step procedures
- [specs/](specs/): how the operation should work (normative)
- [kb/](kb/): evidence behind the specs (non-normative)
- [skills/](skills/): shared capabilities that agents and workflows use
- [docs/](docs/): human-facing guides, including [the five concerns](docs/concerns.md)

## Core rules

- Agents that run the operation never change specs. When a spec is vague or wrong in practice, they record a gap flag instead (location: [to be decided]), and spec changes go through the spec maintenance agent with human approval.
- No agent updates its own definition or its own spec.
- When knowledge is missing, leave a placeholder rather than an assumption.

## Conventions

- Workflows, skills, specs, and agent files use generic capability names ("parallel worker", "human checkpoint"), never platform-specific tool names.
- Platform files contain only pointers and tool wiring.
