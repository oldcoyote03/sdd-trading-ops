# Specs

Specs are normative: they say how the operation should work. Agents act within them, and [spec maintenance](../agents/spec-maintenance.md) proposes changes to them for human approval. You can also edit them directly.

## Organization

- Organize specs by the domain's own units (for example `playbook.md`, `risk.md`, `daily-routine.md`), not by concern.
- Start each spec with a one-line header naming the [concerns](../docs/concerns.md) it touches:

  ```
  concerns: [strategy, execution]
  ```

- To view one concern, list the specs that declare it. Nothing else is maintained for it.

## Rules

- Leave a placeholder (`[to be decided]`) wherever knowledge or a human decision hasn't settled the answer.
- A spec line may cite a KB note, but it doesn't have to.

The first pass is created by [workflows/fork-setup.md](../workflows/fork-setup.md).
