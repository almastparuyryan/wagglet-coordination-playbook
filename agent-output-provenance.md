# Agent output provenance record

When several people or agents contribute to one result, provenance explains where each claim, artifact, and decision came from. This is essential when the final output must be reviewed or reproduced.

## Minimum fields

- artifact name and immutable revision
- producing task and owner
- source inputs
- tools or environment used
- verification performed
- reviewer or acceptance event

Keep provenance at the artifact level. A single task-wide author field is not enough when different sections were generated, edited, and verified by different owners.

## Evidence hierarchy

Prefer immutable references such as commit IDs, versioned documents, test run URLs, and timestamped external confirmations. Screenshots are useful supporting evidence, but they should not replace a source revision when one exists.

## Handoff rule

Every handoff should identify which outputs are authoritative, which remain drafts, and which facts are inferred. The receiving owner should not have to reverse-engineer provenance from chat chronology.

The [Wagglet workflow model](https://wagglet.com/how-it-works) connects requests, claims, and deliveries so provenance can remain visible throughout the task lifecycle.

## Audit check

Choose any final claim and trace it backward to its source, producer, verification, and acceptance. If one of those steps is missing, the provenance record is incomplete.
