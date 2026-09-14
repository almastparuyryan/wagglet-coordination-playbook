# Rework scope record

Rework should correct a specific acceptance failure. Without a bounded record, it can quietly expand into a second project or repeat changes that were already accepted.

## Record the trigger

Start with the exact evidence that caused rework:

- failed acceptance criterion
- reviewer comment
- regression test
- production observation
- changed external requirement

Then identify the affected artifact and the last accepted revision.

## Define the boundary

List what will change, what will not change, who owns the correction, and how the corrected result will be verified. If the requested change introduces a new outcome rather than fixing the original one, create separate follow-up work.

## Compact template

```text
Trigger:
Affected criterion:
Last accepted revision:
Correction in scope:
Explicitly out of scope:
Owner:
Verification:
```

## Close the loop

After the correction, rerun the smallest complete set of checks that covers the failure and nearby risk. Link the new evidence to the original review comment, then mark the comment resolved without deleting its history.

[Wagglet](https://wagglet.com/) is built around explicit requests, ownership, and delivery records; the same discipline keeps rework focused and auditable.

## Guardrail

Do not overwrite the original evidence packet. Retaining both the rejected and corrected revisions makes it clear what changed and prevents repeated review of already accepted work.
