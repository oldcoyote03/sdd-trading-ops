# Implementation Guide: Day Trading

This guide explains how to build and run the operational system for the day-trading fork.

## Prerequisites

Before implementing agents, ensure:

- [ ] All specs in `specs/day-trading/` are completed and validated
- [ ] Role guides in `docs/` have been reviewed by domain experts
- [ ] You have access to required data sources (market feeds, execution venues, internal data stores)

## Architecture Overview

The system has three layers:

1. **Specification Layer** (`specs/day-trading/`)
   - What should happen (five spec files: Strategic, Execution, Observability, Collaboration, Review)

2. **Intelligence Layer** (`agents/`)
   - Agents that read specs and make decisions
   - Built using reusable skills from `skills/core/` and future domain-specific skills from `skills/domain/`

3. **Orchestration Layer** (external)
   - Event triggers, workflow engines, data integrations, logging
   - This is intentionally uncommitted for now while the neutral scaffold is being reviewed

## Agent Implementation

### Agents to Build

List the agents you'll implement and what specs each reads:

- **Strategy Agent**: Reads and refines `specs/day-trading/strategic.md`
  - Responsibilities: [describe]
  - Skills needed: [list]

- **Execution Agent**: Reads `specs/day-trading/execution.md` and `collaboration.md`
  - Responsibilities: [describe]
  - Skills needed: [list]

- **Observability Agent**: Reads `specs/day-trading/observability.md`
  - Responsibilities: [describe]
  - Skills needed: [list]

- **Collaboration Agent**: Reads `specs/day-trading/collaboration.md`
  - Responsibilities: [describe]
  - Skills needed: [list]

- **Review Agent**: Reads `specs/day-trading/review.md`
  - Responsibilities: [describe]
  - Skills needed: [list]

### Skills

#### Reusable (from `skills/core/`)

- `audit_log/` — Log all operational decisions
- `observability/` — Monitor data and generate alerts
- `spec_query/` — Query and parse spec files

#### Domain-Specific (in `skills/domain/`)

Create these skills for the domain when implementation begins:

- market_data_fetcher: fetch live market data and relevant state feeds
- trade_executor: route execution requests through the appropriate execution workflow
- position_tracker: calculate exposures, P&L, and operational status
- compliance_validator: check rules and approval conditions before action

## Data Integration

### Data Sources

List external data sources and how to connect:

- [Data source 1]: [API/DB details, connection string]
- [Data source 2]: [API/DB details, connection string]

### Event Triggers

What events cause agents to activate?

- [Trigger 1]: [description, timing, handler]
- [Trigger 2]: [description, timing, handler]

## Dashboards and Alerts

### Key Dashboards

Describe dashboards for each role:

- **Portfolio Manager Dashboard**: [what they see, refresh rate, key metrics]
- **Analyst Dashboard**: [what they see, refresh rate, key metrics]
- **Executioner Dashboard**: [what they see, refresh rate, key metrics]
- **Compliance Officer Dashboard**: [what they see, refresh rate, key metrics]
- **Accountant Dashboard**: [what they see, refresh rate, key metrics]

### Alert Routing

How are alerts sent to roles?

- [Alert type 1] → [role(s)], via [channel: email/Slack/webhook/etc.]
- [Alert type 2] → [role(s)], via [channel]

## Running the System

### Local Development

Steps to run locally:

```bash
# 1. Install dependencies
pip install -r requirements.txt

# 2. Configure environment
cp .env.example .env
# Edit .env with your data source credentials

# 3. Run agents
python agents/strategy_agent.py
python agents/execution_agent.py
python agents/observability_agent.py
python agents/collaboration_agent.py
python agents/review_agent.py

# 4. Open dashboards
open http://localhost:5000  # or your dashboard URL
```

### Production Deployment

[Describe how to deploy to production: containerization, orchestration, monitoring, etc.]

## Operational Cycles

### First Cycle (Dry Run)

Recommended steps to validate the system:

1. Run agents in read-only mode (no actual executions)
2. Verify specs are being read correctly
3. Verify alerts are being generated correctly
4. Have roles review alert content and dashboards
5. Make spec adjustments based on feedback

### Regular Operations

Once validated:

1. Enable write/execution mode
2. Start with low-confidence actions (e.g., reduced exposure)
3. Monitor agent decisions and outcomes
4. Run daily/weekly reviews (Review Agent)
5. Feed insights back to specs (improvement loop)

## Troubleshooting

### Common Issues

- [Issue 1]: [diagnosis, resolution]
- [Issue 2]: [diagnosis, resolution]

### Logging and Audit

All agent decisions are logged to `audit_log/`. To review:

```bash
python -m skills.core.audit_log --read --domain day-trading --date [YYYY-MM-DD]
```

### Spec Validation

To check specs for completeness before running:

```bash
python .fork-guide/templates/spec-validator.py specs/day-trading/
```

## Getting Help

- **Spec questions**: See role guides and `specs/day-trading/README.md`
- **Agent questions**: See `agents/[agent-name].py` docstrings
- **System questions**: See `reference/` for architecture and contracts
