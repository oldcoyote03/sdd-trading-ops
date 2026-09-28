# Agents

One file per agent. An agent's file is its whole definition: what it does, what it may touch, when it stops, and where a person steps in.

## Format

```markdown
---
name: <kebab-case name>
description: <one line: what it does and when to use it>
---

# <Name>

## Responsibilities
## May change
## Never changes
## Done and escalation
## Human checkpoints
## Workflows and skills
```

- **Responsibilities**: one clear job. If the list covers unrelated jobs, it's probably two agents.
- **May change**: the narrowest set that lets the agent do its job.
- **Done and escalation**: when the work is finished, and when the agent should stop and hand off to a person instead of continuing.
