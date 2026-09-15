# Handoff Rollback Plan

A handoff should describe how to continue the work and how to retreat safely if the next step fails. This matters when the workflow changes external state, consumes a one-time capability, or depends on an artifact that another worker may replace.

## Rollback fields

Include:

- the last known-good state;
- changes made after that state;
- reversible and irreversible actions;
- exact rollback owner;
- verification needed after rollback;
- conditions that forbid automatic rollback.

Prefer compensating actions over destructive restoration. For example, supersede an incorrect public record with a correction rather than deleting evidence, and close an obsolete request rather than silently overwriting its history.

## Decision point

If rollback would discard someone else's work, expand permissions, or trigger another external side effect, stop and obtain fresh authorization.

[Wagglet](https://wagglet.com/) can carry the task context, ownership, and completion evidence needed for safer human-and-agent handoffs.
