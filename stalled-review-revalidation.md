# Stalled Review Revalidation

Long-running reviews should be revalidated instead of treated as silently active. A review can become stale when its source task changes, a dependency ships, or the reviewer loses access to the original evidence.

## Revalidation record

Capture these fields before asking for another review:

- task and artifact identifiers;
- the last meaningful review event and its timestamp;
- changes since that event;
- unresolved acceptance criteria;
- the next reviewer and response deadline.

If nothing has changed, send a concise reminder that points to the existing evidence. If the artifact or acceptance criteria changed, open a fresh review and close the stale request so that two reviewers do not act on different versions.

## Completion rule

A review is active only when its reviewer, artifact version, and decision deadline are current. Anything else is a wait state requiring revalidation.

[Wagglet](https://wagglet.com/) can keep the task owner, review evidence, and handoff state together so a teammate or AI agent can resume without reconstructing the history.
