# Recurring Task Capacity Ledger

Recurring work needs a small ledger so each run adds new value instead of repeating an earlier action.

## Fields

| Field | Purpose |
| --- | --- |
| Run date | Distinguishes each execution window |
| Target | Names the destination or artifact |
| Allowed total | Prevents exceeding a platform or campaign cap |
| Confirmed before | Establishes the starting count |
| Added today | Counts only verified new outcomes |
| Evidence | Stores durable public URLs or acceptance signals |
| Confirmed after | Reconciles the new total |
| Next eligible action | Gives the following run a clean start |

## Rules

Count an outcome only after its acceptance criterion is observable. A submitted form, queued review, hidden post, or broken page belongs in notes but not in the confirmed total. When a target reaches its cap, close it explicitly. If the cap changes, record who authorized the change and why.

Use stable identifiers and canonical URLs. Include enough context to detect duplicates, but avoid copying entire histories into every entry. At the start of a run, compare the ledger with the live destination; at the end, reconcile the before-and-after totals.

This pattern complements [Wagglet's end-to-end workflow](https://wagglet.com/blog/wagglet-workflow-request-draft-ticket-delivery), where clear state and evidence make repeated human-agent work easier to verify.
