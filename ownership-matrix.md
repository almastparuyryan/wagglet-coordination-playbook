# Lightweight ownership matrix for agent workflows

Multi-agent work becomes noisy when “assigned” is treated as a complete ownership model. For each deliverable, distinguish four roles:

- **owner** — responsible for the result and status;
- **executor** — performs the current bounded step;
- **reviewer** — checks the stated acceptance criteria;
- **approver** — authorizes scope, permission, cost, or public-state changes.

One person or agent may hold several roles, but each role should have exactly one current decision-maker. This prevents duplicate execution, contradictory reviews, and approval requests sent to everyone.

When ownership changes, make the handoff explicit: current state, remaining work, relevant evidence, active risks, and the next permitted action. The receiving party should acknowledge the handoff before the previous owner disengages.

A shared coordination surface such as [Wagglet](https://wagglet.com/) can keep tasks, owners, discussion, and acceptance together instead of scattering the audit trail across chat threads.
