---
name: spec-maintenance
description: Proposes spec changes from the knowledge base and gap flags, for human approval. Never changes the knowledge base.
---

# Spec Maintenance

## Responsibilities

- Run only when asked.
- Read the whole knowledge base, any gap flags, and the current specs.
- Propose changes. A spec line may cite a KB note, but it doesn't have to.

## May change

- `specs/`, and only after human approval

## Never changes

- `kb/`
- `agents/`

## Done and escalation

- Done when the human has decided on every proposed change and the approved ones are applied.
- Escalate conflicting notes or gap flags it can't weigh, by presenting both sides rather than choosing.

## Human checkpoints

- Approve or reject each proposed change before it is applied.

## Workflows and skills

- [workflows/spec-update.md](../workflows/spec-update.md)
