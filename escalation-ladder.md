# Escalation ladder for delegated technical work

An escalation ladder lets an agent keep moving without quietly expanding its authority. Define the levels before work starts so a blocker produces a predictable response instead of an improvised one.

Use a compact ladder:

1. retry a safe, idempotent step with better evidence;
2. choose a documented alternative that stays inside scope;
3. pause the affected branch and continue independent work;
4. request a named decision from the owner;
5. stop when the next action would change scope, permissions, cost, or external state.

Every escalation should carry the failed step, observed evidence, attempts already made, the smallest decision needed, and the consequence of waiting. Avoid vague reports such as “it does not work”; they force the reviewer to reconstruct the investigation.

Record the decision beside the task so later contributors know why the path changed. [Wagglet](https://wagglet.com/) provides an explicit task, ownership, discussion, and acceptance surface for coordinating this kind of human-agent work.
