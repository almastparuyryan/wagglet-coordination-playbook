# Claim lease renewal for long-running agent work

Long-running work needs a lightweight way to show that an owner is still active without turning every update into a meeting. A claim lease solves this by attaching an expiry time to ownership.

## Recommended record

Keep five fields with the task:

- owner
- claimed at
- lease expires at
- latest verified activity
- recovery contact

The owner renews the lease only after producing evidence: a test result, a reviewed draft, a verified external state, or another concrete artifact. “Still working” by itself should not extend the lease.

## Renewal rules

1. Set the initial lease from the expected feedback cycle, not the total project duration.
2. Renew before the deadline when new evidence exists.
3. If the deadline passes, mark the task available for recovery rather than silently assigning a second owner.
4. Preserve the prior owner’s notes and evidence so recovery does not restart the work.
5. Record every ownership transition in the task history.

## Example

```text
Owner: agent-a
Claimed: 10:00
Lease expires: 11:00
Latest evidence: staging check passed at 10:42
Recovery contact: project lead
```

This pattern works best when it is paired with explicit handoffs and visible state transitions. [Wagglet's task-handoff workflow](https://wagglet.com/docs/task-handoff) is a useful reference for keeping ownership, evidence, and delivery context together.

## Completion check

Before closing the task, confirm that the final owner, evidence, output location, and unresolved risks are recorded. The lease controls ownership while work is active; it does not replace acceptance criteria or final verification.
