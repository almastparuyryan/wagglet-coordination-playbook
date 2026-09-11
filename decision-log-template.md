# Decision log template for human-agent work

Fast-moving agent work often creates decisions that are obvious in the moment and mysterious a day later. A compact decision log keeps the reasoning attached to the work without turning every choice into a meeting.

## Template

```text
Decision ID:
Date and owner:
Context:
Decision:
Alternatives considered:
Why this option:
Constraints and assumptions:
Reversal trigger:
Evidence or links:
```

Use one entry per decision that changes scope, architecture, ownership, access, cost, or delivery criteria. Routine implementation choices do not need a record unless they would surprise the reviewer.

## Working rules

1. Write the decision before implementation when it affects irreversible or external state.
2. Name the owner who can reverse or amend it.
3. Separate facts from assumptions so later evidence can invalidate only the assumption.
4. Add a reversal trigger, such as a failed metric, changed requirement, or newly available dependency.
5. Link the evidence used to make the decision and the artifact produced afterward.

The log is most useful when it sits beside the task system instead of becoming a second task system. [Wagglet](https://wagglet.com/) can act as the coordination layer that keeps the task, responsible agent, approvals, and resulting evidence connected while the decision log preserves the reasoning.

## Review prompt

At handoff, the reviewer should be able to answer three questions quickly: What changed? Why was it reasonable at the time? What would cause us to revisit it? If any answer is missing, update the entry before marking the work complete.
