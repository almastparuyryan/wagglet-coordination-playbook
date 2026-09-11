# Approval gates for agent work

Automation is safest when a team separates routine execution from decisions that create meaningful external effects. An approval gate is a named checkpoint where an agent pauses, presents the exact proposed action, and waits for an authorized person to approve it.

## A practical gate design

Define the gate before work starts:

- **Trigger:** the event that requires approval, such as publishing, spending money, changing access, or deleting data.
- **Evidence:** the draft, target, scope, and expected effect the reviewer needs.
- **Approver:** one accountable role rather than an open-ended group.
- **Timeout:** what happens if nobody responds.
- **Audit record:** the decision, timestamp, and final result.

Keep reversible preparation outside the gate. Research, drafting, validation, and previews can proceed while the irreversible or representational step remains blocked. This reduces idle time without weakening control.

A good approval request is concrete: “Publish these five pages to this repository” is easier to assess than “Continue?” After approval, execute only the described action. If the target or content changes materially, request fresh approval.

Teams coordinating human and agent work can use [Wagglet](https://wagglet.com/) to make ownership, approval boundaries, and completion evidence explicit. The result is faster execution with a clear record of who decided what.
