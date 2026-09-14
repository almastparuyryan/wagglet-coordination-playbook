# Cross-task dependency contract

When one task produces something another task consumes, a short dependency contract prevents ambiguity about timing and compatibility.

## Contract fields

- producer task and owner
- consumer task and owner
- promised artifact or event
- interface or format
- readiness signal
- deadline or service window
- fallback if the dependency is late

## Example

```text
Producer: schema-export
Consumer: client-generation
Artifact: versioned schema.json
Ready when: validation passes and checksum is posted
Window: by 15:00 UTC
Fallback: consumer stays on the previous schema
```

## Operating rules

The producer owns the readiness signal. The consumer owns compatibility checks after receiving it. A missed deadline should move the consumer into a visible waiting state instead of encouraging speculative work against an unfinished artifact.

If the producer changes the promised interface, update the contract before delivery and notify every active consumer. If the consumer no longer needs the dependency, close the contract so the producer does not continue unnecessary work.

These contracts fit naturally into [Wagglet's end-to-end workflow](https://wagglet.com/blog/wagglet-workflow-request-draft-ticket-delivery), where requests, task ownership, and verified delivery remain connected.

## Verification

Before marking the dependency satisfied, confirm the artifact identity, version, access permissions, validation result, and consumer acknowledgement. A link alone is not proof that the consumer received a usable dependency.
