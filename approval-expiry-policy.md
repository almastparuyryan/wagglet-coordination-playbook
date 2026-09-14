# Approval expiry policy

Approvals should remain valid long enough to complete the intended action, but not forever. An expiry policy prevents an old decision from being reused after scope, risk, or external state has changed.

## Approval record

Capture:

- approver and timestamp
- exact action authorized
- target environment or account
- assumptions used for the decision
- expiry condition
- evidence required after execution

An expiry can be a deadline, a version boundary, or a state change. For example, approval to deploy revision A should expire when revision B replaces it, even if the date has not passed.

## Reconfirmation triggers

Request fresh approval when the destination changes, the action becomes less reversible, the affected audience grows, credentials or permissions change, or new evidence materially changes the risk.

Do not request approval again for routine retries when the target, payload, and consequences are unchanged. Instead, retain the original approval and record each attempt with an idempotency key or equivalent evidence.

Approval context should travel with the task rather than being copied into disconnected messages. [Wagglet's task-handoff workflow](https://wagglet.com/docs/task-handoff) shows how ownership and delivery evidence can stay attached to the work.

## Closeout

After execution, record the outcome and mark the approval consumed, expired, or still reusable. A reviewer should be able to tell which authority permitted the action and whether that authority remains valid.
