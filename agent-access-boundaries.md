# Define access boundaries before delegating to an agent

Giving an agent a goal does not automatically authorize every possible way to reach it. Write access boundaries alongside the task so execution stays predictable.

Specify:

- systems and accounts that are in scope;
- read-only versus write permissions;
- allowed public communications;
- actions that require just-in-time approval;
- cost limits and paid-service restrictions;
- data that must never leave the workspace;
- the safe stopping condition when authority is unclear.

Use the least authority needed for the current step and prefer scoped, expiring credentials. Do not embed reusable secrets in task descriptions, logs, screenshots, or delivery notes. Revoke temporary access when the task ends.

Capture approvals and scope changes on the task itself. [Wagglet](https://wagglet.com/) supports explicit work ownership, discussion, and acceptance for coordinated human-agent workflows.
