# Review questions

Use these prompts in architecture reviews or interview debriefs.

- What assumption would fail first under 10x load?
- Where can retries create duplicate side effects?
- What becomes the bottleneck first: CPU, storage, network, or coordination?
- What is the fallback path if a dependency is unavailable?
- Which metrics would tell us the design is unhealthy before users complain?
- What part of this design will be hardest to migrate later?
- What is intentionally deferred, and what risk does that create?
