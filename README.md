# SDD Trading Ops

A specification-driven setup for running operations with AI agents. Specs say how the operation should work, the knowledge base holds the evidence behind them, and agents do the work within what the specs allow.

## How it grows

Building this out is a loop, not a straight line:

1. **Gather knowledge**: bring sources into the [knowledge base](kb/).
2. **Update specs**: turn knowledge and experience into [specs](specs/), with human approval.
3. **Build or adjust agents**: define [agents](agents/) that act on the specs.
4. **Operate**: agents run, and people approve, decide, or take over at checkpoints.
5. **Learn**: gaps and lessons feed the next pass.

At each turn, ask which of the [five concerns](docs/concerns.md) is thinnest right now, and work on that next.

## Where to start

- New to the project: read [AGENTS.md](AGENTS.md) for the map.
- Setting up a fork: run [workflows/fork-setup.md](workflows/fork-setup.md).
- Human role guides: [docs/](docs/).
