# The Five Concerns

A lens for asking questions, not a file structure. The questions are here, and the answers live in the [specs](../specs/). Use them in the fork interview, when reviewing specs, when designing agents, and when sorting out lessons learned.

## Strategy

- What is the operation trying to achieve, and how is success measured?
- What rules decide what to do, and when not to act?
- What limits and priorities apply when goals conflict?

## Execution

- What actions can be taken, and under what conditions?
- Which actions need a human's approval first?
- What happens when an action fails or is interrupted?

## Observability

- What needs watching, and how often?
- What should trigger an alert, and who or what receives it?
- What must be recorded so it can be reviewed later?

## Collaboration

- Where do people approve, decide, or take over?
- What does each person need to see, and when?
- How do agents hand work to each other or to a person?

## Review

- How are outcomes judged against the strategy?
- How often does review happen, and what does it produce?
- How do lessons become knowledge, gap flags, or spec changes?
