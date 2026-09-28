---
name: fork-setup
description: Set up a new fork with first-pass specs through an interview
run-by: fork-guide
---

# Fork Setup

## Steps

1. Ask the human to describe the domain and what the operation should achieve.
2. Walk through the questions in [docs/concerns.md](../docs/concerns.md). Record answers as given, and leave the rest open.
3. Propose spec units in the domain's own terms (for example `playbook.md`, `risk.md`, `daily-routine.md`).
4. **Checkpoint**: the human confirms or adjusts the list of units.
5. Draft each spec with a `concerns:` header, following [specs/README.md](../specs/README.md). Use placeholders for anything not answered.
6. **Checkpoint**: the human reviews the drafts.
7. Write the approved specs, and update `README.md` to describe the fork.

## Done When

- [ ] Each spec unit exists with a `concerns:` header
- [ ] Unanswered questions are placeholders, not assumptions
- [ ] The thinnest concern is named as the next focus
