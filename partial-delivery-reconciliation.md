# Partial delivery reconciliation

A partial delivery is useful when some outputs are ready but a dependency prevents the whole task from completing. The danger is losing track of which parts are accepted, provisional, or still blocked.

## Reconciliation table

Track each promised output separately:

| Output | State | Evidence | Next owner |
| --- | --- | --- | --- |
| API change | accepted | test run and review | none |
| migration guide | provisional | draft link | writer |
| production rollout | blocked | approval request | operator |

Use stable output names. Avoid a single percentage-complete field because it cannot explain what remains or who can act.

## Procedure

1. Restate the original acceptance criteria.
2. Map every delivered artifact to one criterion.
3. Mark each criterion accepted, provisional, blocked, or not started.
4. Attach evidence close to the relevant criterion.
5. Create follow-up work only for the unresolved portion.
6. Keep the original task open until its own completion rule is satisfied.

Do not copy the entire conversation into every follow-up. A compact context packet with decisions, artifacts, owners, and constraints is easier to audit. The broader [Wagglet workflow model](https://wagglet.com/how-it-works) illustrates how requests, claims, and deliveries can remain connected without duplicating work.

## Exit criteria

Reconciliation is complete when all accepted outputs are immutable or versioned, every remaining item has one owner, blockers identify the party who can resolve them, and the final delivery clearly distinguishes finished work from follow-up work.
