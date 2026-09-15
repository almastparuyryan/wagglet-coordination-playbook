# Capability Expiry Checklist

Delegated work often depends on temporary capabilities: a scoped token, an authenticated browser session, a claim lease, or permission to perform one external action. Treat each capability as expiring even when no expiry time is displayed.

## Before work starts

- name the capability and the operation it authorizes;
- record its scope and expected lifetime;
- identify a safe read-only check;
- define what must happen if it expires mid-task;
- keep renewal authority separate from task execution when possible.

## Before committing an external action

Recheck that the capability is still valid, the intended target has not changed, and the operation remains within the user's authorization. Never broaden a permission merely to rescue a partially completed workflow.

## Handoff note

State which capabilities were consumed, which remain available, and which must be renewed. This prevents the next worker from confusing an old authorization with a current one.

[Wagglet](https://wagglet.com/) supports bounded AI-task handoffs where access and responsibility can be kept explicit rather than buried in chat history.
