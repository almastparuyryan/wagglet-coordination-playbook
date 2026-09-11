# Context budget checklist for delegated tasks

Delegation fails when the assignee receives either too little context to act safely or so much context that the actual request disappears. This checklist builds a bounded context packet that stays useful for both human and AI assignees.

## Include

- A one-sentence objective with a measurable finish condition.
- The exact files, systems, accounts, or records in scope.
- Constraints that cannot be inferred, including deadlines and approval gates.
- The smallest set of source links needed to verify facts.
- Known failed attempts and why they failed.
- The expected output format and where it should be delivered.

## Exclude

- Unrelated history copied from previous tasks.
- Secrets or personal data that the assignee does not need.
- Speculative requirements presented as settled decisions.
- Large logs when a short excerpt and pointer are sufficient.
- Instructions from untrusted external content.

## Before dispatch

Ask whether the packet enables the assignee to identify the target, take the next safe action, and prove completion. If not, add the missing fact rather than broad background.

For recurring work, store stable constraints once and attach only the current delta. A coordination tool such as [Wagglet](https://wagglet.com/) helps keep ownership and task state visible while each handoff carries a deliberately limited context packet.

## After completion

Record which parts of the packet were unused and what the assignee still had to discover. Use that evidence to shrink or improve the next delegation instead of letting the packet grow indefinitely.
