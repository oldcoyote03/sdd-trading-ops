# Day Trading Collaboration Specification

This draft is intentionally neutral. Replace placeholders with explicit roles, responsibilities, approvals, and notification paths once the domain and operating model are defined.

## Roles & Responsibilities

### Role: Portfolio Manager

**Responsibilities**:
- [portfolio objective and prioritization responsibility]
- [allocation or planning responsibility]
- [escalation or monitoring responsibility]

**Authority**:
- [decision or action the role can take]
- [boundaries or limits]
- [override or approval authority]

**Escalation**:
- [what triggers escalation]
- [who receives the escalation]

### Role: Analyst

**Responsibilities**:
- [research and monitoring responsibility]
- [review or support role]

**Authority**:
- [approval or limits]

**Escalation**:
- [common escalation trigger]

### Role: Executioner

**Responsibilities**:
- [execution and operational responsibility]
- [exception handling responsibility]

**Authority**:
- [permission to act within defined windows]
- [limits on order or timing actions]

**Escalation**:
- [when to pause or escalate]

### Role: Compliance Officer

**Responsibilities**:
- [control and policy monitoring responsibility]
- [review and documentation responsibility]

**Authority**:
- [approval or veto authority for compliance constraints]
- [limits on operational exceptions]

**Escalation**:
- [trigger for regulatory or policy escalation]

### Role: Accountant

**Responsibilities**:
- [recordkeeping and reconciliation responsibility]
- [financial reporting or audit support]

**Authority**:
- [review or approval authority for accounting accuracy]
- [limits on operational adjustments]

**Escalation**:
- [when discrepancy is detected]

## Information Visibility

### Portfolio Manager

**Spec Sections Visible**:
- Strategic: [full / summary / none]
- Execution: [full / limited]
- Observability: [full / summary]
- Collaboration: [full / own role only]
- Review: [full / summary]

**Data Access**:
- Real-time: [what they may see]
- Historical: [what they may review]
- Reporting: [what they receive]

### Analyst

**Spec Sections Visible**:
- Strategic: [full / summary / none]
- Execution: [full / limited]
- Observability: [full / summary]
- Collaboration: [full / own role only]
- Review: [full / summary]

### Executioner

**Spec Sections Visible**:
- Strategic: [summary only]
- Execution: [full]
- Observability: [full]
- Collaboration: [own role only]
- Review: [summary]

### Compliance Officer

**Spec Sections Visible**:
- Strategic: [summary]
- Execution: [full]
- Observability: [full]
- Collaboration: [full]
- Review: [summary]

### Accountant

**Spec Sections Visible**:
- Strategic: [summary]
- Execution: [summary]
- Observability: [summary]
- Collaboration: [summary]
- Review: [full]

## Approval Workflows

### Workflow: [Approval Trigger]

**Approver**: [role or process]
**Conditions**: [when approval is required]
**SLA**: [timing expectation]
**Fallback**: [what to do if approval is not given]

## Communication & Notification

### Event: [Notification Name]

**Recipients**: [role or group]
**Channel**: [email, dashboard, message, or in-app]
**Urgency**: [low | medium | high | critical]
**Message**: [sample notification or template]

## Onboarding & Offboarding

### New Role Onboarding

1. [learning or training step]
2. [practice or shadowing step]
3. [live operation or evidence step]
4. [final authorization or review]

### Role Removal or Transfer

**Scenario**: [transition or change event]
1. [operational action]
2. [handoff or audit action]
3. [review or finalization step]

## Conflicts & Escalation

**Scenario**: [conflict condition]
- **Resolution**: [how disagreement is handled]
- **Escalation**: [who reviews or resolves the issue]
