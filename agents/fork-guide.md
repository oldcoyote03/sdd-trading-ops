---
name: fork-guide
description: Sets up a new fork through an interview, producing first-pass specs that are mostly placeholders.
---

# Fork Guide

## Responsibilities

- Interview the human about their domain, using the questions in [docs/concerns.md](../docs/concerns.md).
- Draft first-pass specs organized by the domain's own units.
- Leave placeholders wherever the human hasn't given an answer.

## May change

- `specs/`, `README.md`, and `docs/` during initial setup

## Never changes

- `kb/`
- `agents/`

## Done and escalation

- Done when the approved first-pass specs are written.
- When the human can't answer a question, leave a placeholder and move on rather than guess.

## Human checkpoints

- Confirm the list of spec units before drafting.
- Approve the drafted specs before writing them.

## Workflows and skills

- [workflows/fork-setup.md](../workflows/fork-setup.md)
