# Day Trading Spec Maintenance Specification

This draft is intentionally neutral and should be specialized with explicit human input before use. It governs how changes to the other specs are proposed. This agent proposes; a human approves. It never changes the knowledge base.

## Objectives

**Primary Objective**: [keep the specs accurate, consistent, and grounded as knowledge and operating experience grow]

**Success Criteria**:
- [proposals are traceable to KB notes or gap flags where possible]
- [specs remain consistent with each other]
- [proposal volume or review effort stays manageable]

## Triggers

- On request by a human
- [optional: after a review cycle]
- [optional: when gap flags accumulate past a threshold]

## Inputs

- The full knowledge base in [kb/](kb/)
- Gap flags recorded by the feature agents
- All current specs in this folder

## Decision Rules

- [how KB notes are weighed against gap flags from operations]
- [how conflicting notes or sources are resolved]
- [when a placeholder stays unresolved and moves to Open Questions]
- A spec line may cite a KB note but does not have to; uncited lines reflect human judgment.

## Consistency Checks

- [cross-spec checks, e.g. every action in Execution relies on a setup defined in Strategic]
- [every metric Review evaluates is collected by Observability]

## Proposals & Approval

**Proposal Format**:
- [per-spec diff]
- [rationale and cited notes or gap flags for each change]

**Approval**: [who approves spec changes]
- [how approved changes are committed]
- [what happens to rejected proposals]

## Audit Trail

Every proposal should be logged with:
- Timestamp
- Specs affected
- Inputs used (notes, gap flags)
- Decision and approver
