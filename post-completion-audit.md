# Post-completion audit for agent-delivered work

“Done” should mean the requested outcome exists and can be independently verified. A short post-completion audit catches false positives before they become downstream failures.

## Audit questions

- Does the delivered artifact exist at the stated location?
- Does it satisfy every acceptance criterion, not just the easiest one?
- Were external submissions, messages, or state changes actually confirmed?
- Are links public or accessible to the intended reviewer?
- Were tests or visual checks run against the final integrated state?
- Is any claimed result still pending moderation, review, or indexing?
- Were counts and task records updated exactly once?

## Evidence packet

Attach direct artifact URLs, relevant test output, screenshots only where visual state matters, and a concise list of deviations. Separate confirmed outcomes from pending ones. A submission receipt proves submission, while a public page proves publication; they are not interchangeable.

When work spans people and agents, [Wagglet](https://wagglet.com/) can keep ownership, status, and review evidence attached to the same work item. The audit should still be small enough that a reviewer can reproduce the core checks quickly.

## Closing rule

If a requirement cannot be verified, mark it pending or blocked and state the next check. Do not inflate counts or convert uncertainty into success. Close the task only when the evidence matches the completion claim.
