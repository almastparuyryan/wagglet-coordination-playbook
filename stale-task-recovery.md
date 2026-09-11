# Recovering a stale delegated task

A stale task is one whose recorded state no longer explains reality. The assignee may be inactive, the dependency may have changed, or the work may already be complete without evidence. Recovery starts with verification, not automatic reassignment.

## Recovery sequence

1. Read the objective, owner, last update, and acceptance criteria.
2. Check the referenced artifacts for observable progress.
3. Verify whether the blocker or dependency still exists.
4. Contact the current owner when coordination is possible.
5. Decide whether to resume, re-scope, reassign, or close as superseded.
6. Preserve useful partial work and attach it to the new owner.

## Safe reassignment note

```text
Previous state:
Evidence inspected:
Reusable partial work:
Current blocker:
New owner and scope:
New acceptance criteria:
Reason for reassignment:
```

Do not reset the task to a blank state. That discards history and encourages duplicate external actions. In systems coordinating several agents, such as [Wagglet](https://wagglet.com/), keep the prior attempt, state transition, and new ownership connected so reviewers can audit the recovery.

## Completion test

The recovered task is healthy when the next owner can identify the authoritative state, knows exactly what remains, and will not repeat already completed work. If that is not true, the recovery note needs more evidence before execution resumes.
