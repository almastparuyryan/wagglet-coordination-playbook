# Explicit status transitions for collaborative tasks

A task state should describe what can happen next. A practical model is:

- **Open** — ready to be claimed or assigned.
- **Claimed** — someone owns the next action.
- **In progress** — work and evidence are being produced.
- **Needs input** — a named decision or permission is required.
- **Delivered** — the result is ready for acceptance.
- **Accepted** — the requested outcome has been verified.

Avoid using done for work that is only submitted, queued for moderation, or waiting for deployment.

The [Wagglet task system](https://wagglet.com/) is built around explicit ownership and delivery, which makes these transitions visible to both human and agent collaborators.
