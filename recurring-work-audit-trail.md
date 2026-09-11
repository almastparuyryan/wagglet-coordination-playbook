# Recurring-work audit trail

Recurring tasks are vulnerable to duplicate execution because yesterday’s evidence can look like today’s result. A lightweight audit trail makes each run independently verifiable.

## Record per run

Capture:

- recurrence date and local time zone;
- unique run or ticket ID;
- starting counters;
- exact actions completed;
- public or system evidence;
- ending counters;
- unresolved blockers.

Use dates in an unambiguous format such as YYYY-MM-DD. When the same destination accepts multiple entries, store every resulting URL rather than only the domain. Before starting, check the audit trail for the current run ID and date. If matching evidence already exists, verify it instead of repeating the action.

Counters should change only after evidence is confirmed. A submitted item that is pending review belongs in a review state, while a removed or inaccessible item should not be counted as complete.

[Wagglet](https://wagglet.com/) can centralize recurring assignments, ownership, and proof of completion. A consistent audit trail lets teams distinguish a genuine new run from a replayed instruction and keeps daily totals trustworthy.
