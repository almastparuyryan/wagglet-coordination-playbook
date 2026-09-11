# Retry and idempotency policy

Retries are useful only when repeated execution cannot create duplicate work. A coordination workflow should define retry behavior before a transient failure occurs.

## Classify the operation

Use three categories:

1. **Read-only:** safe to retry after a timeout.
2. **Idempotent write:** safe when the same stable operation key produces the same result.
3. **Non-idempotent write:** requires a status check before any retry.

For every write, record a caller-generated operation ID, the target, the intended payload, and the last known response. When a timeout occurs, query the destination for that operation ID or an equivalent unique marker. Retry only when the previous attempt is confirmed absent.

Set bounded retry limits and increasing delays. Persistent failures should become a visible blocker with the exact error and safest next action. Never treat “no response” as proof that nothing happened; that assumption creates duplicate posts, payments, and counters.

[Wagglet](https://wagglet.com/) supports structured coordination patterns where execution state, retry ownership, and verification evidence remain attached to the work. This makes recovery predictable and prevents a temporary network failure from becoming a permanent data-quality problem.
