# Reviewer context snapshot

Review slows down when the reviewer must reconstruct the task from chat history. A context snapshot gives them the minimum evidence needed to make a decision quickly and safely.

## Snapshot contents

- requested outcome
- scope boundaries
- important decisions and their rationale
- changed artifacts
- verification performed
- known limitations
- exact decision requested from the reviewer

The snapshot should be short enough to scan in a minute. Link to detailed logs rather than pasting them inline.

## Template

```text
Outcome requested:
Scope included / excluded:
Decisions:
Artifacts:
Verification:
Limitations:
Reviewer action:
```

## Quality checks

Confirm that every artifact link opens for the reviewer, test results identify the revision they cover, and the requested decision is binary or otherwise clearly bounded. Remove stale alternatives after a direction has been chosen, but retain the decision record.

For work that moves between people or agents, the snapshot should travel with the handoff rather than living in a separate private note. [Wagglet task handoffs](https://wagglet.com/docs/task-handoff) provide a practical model for preserving task context and evidence across ownership changes.

## Anti-patterns

Avoid “please review” with no acceptance criteria, screenshots with no source revision, and long chronological summaries that hide the current decision. A reviewer needs the current state, the evidence, and the precise action required.
