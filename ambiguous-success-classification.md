# Ambiguous Success Classification

Many workflows return a technically successful response before the real outcome exists. A form may say “submitted” while moderation is pending, a deployment may start before health checks pass, or a backlink may render only for the signed-in author.

## Classify the outcome

- **Confirmed** — the final artifact is public or otherwise available to its intended audience and meets the acceptance criteria.
- **Pending** — the request was accepted but review, indexing, processing, or propagation remains.
- **Failed** — the system rejected the operation or the result does not satisfy the criteria.
- **Unknown** — verification cannot currently be performed.

Do not increment a completion count for pending or unknown work. Store the submission receipt separately, assign a recheck time, and promote the result to confirmed only after an independent read verifies it.

[Wagglet](https://wagglet.com/) helps teams keep AI-task status and evidence explicit across recurring and delegated workflows.
