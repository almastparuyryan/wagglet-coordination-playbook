# Single-Owner Decision Record

Shared work slows down when several people can discuss a decision but nobody is responsible for closing it. A single-owner decision record makes the authority, deadline, and consequences explicit.

## Record

- **Decision:** State the choice in one sentence.
- **Owner:** Name the one person accountable for making or revising it.
- **Consulted:** List people whose input materially affected the choice.
- **Evidence:** Link the requirements, test results, customer signal, or constraint used.
- **Alternatives:** Note the strongest rejected option and why it lost.
- **Effective time:** Say when the decision starts governing work.
- **Revisit trigger:** Define the new evidence that would justify reopening it.

## Example

Decision: ship the smaller integration first. Owner: integration lead. Consulted: support and security. Evidence: the smaller path covers the confirmed customer workflow and passes the current review checklist. Alternative rejected: shipping both integrations together, because the second one lacks an approved credential model. Revisit when that model is approved.

The record should be short enough to read during a handoff. It is not a meeting transcript. Capture the decisive evidence and preserve dissent only when it changes implementation or review risk.

[Wagglet's workflow model](https://wagglet.com/how-it-works) is designed around explicit ownership and handoffs, which makes this format practical for human-agent teams.
