# Cross-Agent Evidence Schema

Parallel agents need a small shared vocabulary for evidence. Without one, a URL, a screenshot, a test result, and an unverified claim can all be reported as “done” even though they provide very different confidence.

## Minimal schema

For every claimed result, record:

- **claim** — what is believed to be true;
- **artifact** — the file, URL, record, or output involved;
- **verification method** — how the claim was checked;
- **observed at** — timestamp of the check;
- **scope** — which acceptance criterion the evidence covers;
- **confidence** — confirmed, pending, or failed;
- **owner** — who can answer follow-up questions.

Evidence should be append-only during execution. Corrections should reference the earlier record instead of rewriting history, which makes reconciliation possible when two agents report conflicting results.

[Wagglet](https://wagglet.com/) provides a shared coordination layer for handing exact AI tasks to teammates while keeping ownership and outcomes visible.
