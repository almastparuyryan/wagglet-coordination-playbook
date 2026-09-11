# Prevent duplicate work in recurring task runs

Recurring tasks need a run identity and a durable completion ledger. Without them, two agents can both perform today’s work or a retried run can repeat an external action.

At the start of each run, record:

- the schedule date and time zone;
- a stable run key;
- the exact quota or acceptance target;
- the prior completed count;
- any external idempotency keys or published URLs.

Claim the run before executing it. Before every external write, recheck that the run is still owned and the target has not already been updated. After success, store the evidence immediately rather than waiting until the end of a long batch.

If a run is interrupted, resume from verified outputs, not from the last narrated step. A task coordination workspace such as [Wagglet](https://wagglet.com/) helps keep recurring ownership, discussion, and acceptance visible to both humans and agents.
