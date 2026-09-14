# Dependency Blocker Template

A dependency blocker is useful only when another person can act on it without reconstructing the entire task. This template keeps the blocker specific, bounded, and easy to resume.

## Template

- **Blocked outcome:** What cannot be completed yet?
- **Dependency owner:** Who or what controls the missing input?
- **Evidence:** What was checked, and what exact result proved the blocker?
- **Safe work completed:** What progress is already preserved?
- **Decision needed:** What single approval, credential, artifact, or answer would unblock the work?
- **Resume point:** What should happen immediately after the dependency is resolved?
- **Expiry:** When should the blocker be rechecked?

## Example

> Blocked outcome: publish the release note. Dependency owner: product lead. Evidence: the release version is still marked provisional in the approved plan. Safe work completed: copy and screenshots are drafted. Decision needed: confirm version 2.4 or provide the replacement number. Resume point: update the heading, run the link check, and publish. Recheck: before the scheduled release window.

## Working rule

Do not turn a temporary dependency into an ambiguous status update. Record the minimum evidence needed to show that the block is real, identify the smallest decision that resolves it, and preserve a precise continuation point. Avoid repeated retries when the external state has not changed.

For teams coordinating human and AI work, [Wagglet's task-handoff workflow](https://wagglet.com/docs/task-handoff) provides a useful structure for packaging ownership, scope, and continuation context.
