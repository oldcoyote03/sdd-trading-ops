# Day Trading Operations

A specification-driven operational system for day trading, built from the SDD template.

---

## What is This?

This repository runs day-trading operations using specification-driven design:

- Specifications define strategic rules, execution workflows, monitoring targets, collaboration protocols, and feedback loops
- Agents interpret specs and make operational decisions when implemented
- Outcomes are logged and feed back into continuous improvement

The system is organized around five core features:

| Feature | Purpose |
|---------|---------|
| **Strategic** | Decision rules, priorities, and frameworks |
| **Execution** | What actions can be taken, when, by whom, with what approvals |
| **Observability** | What to monitor, alert on, visualize |
| **Collaboration** | Who is involved, what visibility they have, what they must approve |
| **Review** | How outcomes are analyzed and lessons loop back into improvements |

---

## Roles in This System

Choose your role to get started:

- **Portfolio Manager** → [docs/portfolio-manager.md](docs/portfolio-manager.md) — Oversees portfolio priorities and operating constraints
- **Analyst** → [docs/analyst.md](docs/analyst.md) — Reviews data, identifies trends, and supports improved decisioning
- **Executioner** → [docs/executioner.md](docs/executioner.md) — Executes approved actions within defined limits
- **Compliance Officer** → [docs/compliance-officer.md](docs/compliance-officer.md) — Monitors policy, control boundaries, and risk concerns
- **Accountant** → [docs/accountant.md](docs/accountant.md) — Reconciles activity and supports financial traceability

---

## Getting Started

### First Time?

1. Read your role guide above
2. Understand the specs in [specs/day-trading](specs/day-trading)
3. Review [IMPLEMENTATION.md](IMPLEMENTATION.md) for the operational setup

### For Operators

- Monitor alerts and dashboards described in the role guides
- Approve or reject actions when required
- Review outcomes at the end of the trading day or review period according to [specs/day-trading/review.md](specs/day-trading/review.md)

### For Implementers

See [IMPLEMENTATION.md](IMPLEMENTATION.md) for:
- How to build agents
- How to set up data integrations
- How to validate against specs
- How to run operational cycles

### For Spec Authors

- Modify specs in [specs/day-trading](specs/day-trading) as the domain evolves
- Keep specs versioned with clear commits
- Notify the team of significant changes

---

## Key Docs

- **Strategic Spec**: [specs/day-trading/strategic.md](specs/day-trading/strategic.md) — Decision rules and priorities
- **Execution Spec**: [specs/day-trading/execution.md](specs/day-trading/execution.md) — Executable actions and approvals
- **Observability Spec**: [specs/day-trading/observability.md](specs/day-trading/observability.md) — Monitoring and alerts
- **Collaboration Spec**: [specs/day-trading/collaboration.md](specs/day-trading/collaboration.md) — Roles and workflows
- **Review Spec**: [specs/day-trading/review.md](specs/day-trading/review.md) — Analysis and improvement loops

---

## Reference

For more on the template architecture and design patterns:
- See [ARCHITECTURE.md](ARCHITECTURE.md)
- See [reference](reference) for agent interfaces and feature explanations

For the fork process itself:
- Continue with [.fork-guide/INSTRUCTIONS.md](.fork-guide/INSTRUCTIONS.md)

---

## Quick Links

- **Dashboards**: [http://localhost:5000](http://localhost:5000) when running
- **Audit Logs**: See [IMPLEMENTATION.md](IMPLEMENTATION.md) for audit log access
- **Issues/Feedback**: Use your repository issue tracker

---

## Questions?

- "What should I do as Portfolio Manager?" → See [docs/portfolio-manager.md](docs/portfolio-manager.md)
- "How is the system built?" → See [IMPLEMENTATION.md](IMPLEMENTATION.md)
- "Why this rule/workflow?" → See the relevant spec file
- "How do I change something?" → Update the spec, commit, and notify the team
