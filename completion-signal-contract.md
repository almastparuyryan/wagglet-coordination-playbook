# Completion signal contract

A completion signal should mean the same thing to the producer, consumer, and reviewer. Without a contract, “done” may describe an uploaded file, a passing test, an accepted review, or a production rollout.

## Define the signal

Specify:

- the event that emits completion
- acceptance criteria that must already be satisfied
- evidence attached to the event
- consumers that may act on it
- conditions that invalidate it

## Example

```text
Signal: delivery.accepted
Required state: artifact published and verification passed
Evidence: immutable artifact URL and test run
Consumers: release task and reporting workflow
Invalidated by: rollback or superseding revision
```

## Emission rules

Emit completion once per accepted revision. Retries should reuse an idempotency key so downstream work does not start twice. If a later correction is required, publish a new revision and a new signal rather than rewriting the original event.

Separate completion from progress. An owner can be finished drafting while the task remains in review; the contract should reserve the final signal for the state that downstream consumers actually need.

[Wagglet's end-to-end workflow](https://wagglet.com/blog/wagglet-workflow-request-draft-ticket-delivery) provides a practical reference for connecting delivery records with explicit task state.

## Verification

Test duplicate delivery, late consumer startup, rollback, and superseding revisions. Consumers should derive the same state even when they process events more than once.
