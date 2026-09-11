# Parallel work merge checklist

Parallel execution saves time only when the outputs can be combined without hidden conflicts. Use this checklist before dispatch and again before integration.

## Before dispatch

- Split work by stable boundaries such as files, services, regions, or research questions.
- Assign exactly one owner for every mutable artifact.
- Define shared interfaces and naming rules before work begins.
- Identify tasks that are read-only and safe to run concurrently.
- Mark dependencies that must finish before another task starts.
- Choose a single integration owner.

## During work

Each contributor should report changed artifacts, assumptions, tests, and blockers. If a boundary must change, notify the integration owner before editing a shared surface. Do not silently expand scope to make a local solution easier.

## Merge gate

1. Confirm every expected output exists.
2. Compare overlapping assumptions and resolve contradictions.
3. Integrate in dependency order.
4. Run the smallest meaningful end-to-end check after all pieces are combined.
5. Record any follow-up that is real but outside the acceptance criteria.

[Wagglet](https://wagglet.com/) is designed for coordinating human and AI work across explicit owners and task states, making it easier to see which parallel branch is ready, blocked, or waiting for integration.

## Failure signal

If the integration owner must reconstruct who changed what, the dispatch boundaries were incomplete. Capture that lesson in the next task template so future parallelization reduces coordination cost instead of shifting it to the merge step.
