# Parallel-work dependency map

Parallel execution saves time only when dependencies are explicit. Before splitting work, draw a small dependency map showing what can start now, what consumes another task’s output, and where results must be merged.

## Minimal map

For each work item, capture:

- owner;
- required inputs;
- output contract;
- downstream consumers;
- merge point;
- failure fallback.

Start independent research and preparation tasks together. Keep shared-state edits serialized unless the tools provide atomic updates. When two contributors must touch the same file or record, assign clear ownership by section or sequence.

Define the output contract narrowly. “Analyze the API” is ambiguous; “return endpoint names, authentication rules, and three failure cases” is mergeable. A coordinator should review outputs at the merge point, resolve contradictions, and publish one canonical result.

[Wagglet](https://wagglet.com/) is designed for coordinated human-agent work where task ownership, dependencies, and evidence need to remain visible. A simple dependency map helps teams gain the speed of parallel work without duplicated effort or conflicting edits.
