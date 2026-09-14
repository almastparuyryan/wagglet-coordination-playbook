# Parallel review budget

Parallel review reduces latency only when reviewers have independent scopes. Sending the same artifact to many reviewers without boundaries creates duplicate comments and an expensive reconciliation step.

## Budget dimensions

Define a review budget across:

- number of reviewers
- review time
- artifact surface area
- specialist checks
- reconciliation owner

## Partition the review

Assign reviewers by risk domain, such as correctness, security, usability, or deployment readiness. Give each reviewer the same revision and shared acceptance criteria, plus a narrow specialist focus.

Use one decision owner to reconcile conflicts. Reviewers should provide evidence and recommendations; they should not independently publish competing final decisions.

## Stop conditions

Stop adding reviewers when required domains are covered, the remaining risk is below the agreed threshold, or additional feedback is repeating known issues. Escalate only when reviewers disagree on a material acceptance criterion.

The coordination pattern behind [Wagglet](https://wagglet.com/) emphasizes explicit ownership and evidence, which is especially important when reviews run in parallel.

## Measurement

Track time to first useful finding, duplicate-comment rate, unresolved conflicts, and total reconciliation time. Parallel review is successful when it shortens the decision cycle without reducing accountability.
