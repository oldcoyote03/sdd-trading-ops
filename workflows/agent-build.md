---
name: agent-build
description: Define a new agent, or adjust an existing one, from the specs
run-by: agent-builder
---

# Agent Build

## Steps

1. Name the need: which specs the agent acts on, and which concerns it touches.
2. Check for a simpler option: an existing agent, workflow, or skill that could cover the need. If one fits, propose that instead and stop here.
3. Draft `agents/<name>.md` in the format from [agents/README.md](../agents/README.md). Keep "May change" as narrow as possible, with a reason for each item, and define when the agent is done and when it escalates.
4. List the skills it needs, and mark any that don't exist yet.
5. **Checkpoint**: the human approves the definition, especially what it may change and its human checkpoints.
6. Write the agent file, and add a thin adapter for each platform in use.
7. Try the agent on a few representative tasks. Adjust the definition based on what happens.
8. **Checkpoint**: the human reviews the trial results.

## Done When

- [ ] A simpler option was considered first
- [ ] The agent file exists, with narrow permissions and clear done and escalation conditions
- [ ] An agent that runs the operation cannot change specs
- [ ] Platform adapters only point to the agent file
- [ ] Trial results were reviewed by a human
