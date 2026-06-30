# Common tradeoffs

## Simplicity vs flexibility

Prefer a design that is easy to operate unless flexibility is a real near-term requirement.

## Strong consistency vs availability / latency

Be explicit about where correctness is mandatory and where eventual consistency is acceptable.

## Synchronous vs asynchronous work

Sync paths reduce coordination complexity for users but can amplify latency and failure coupling.

## Cache hit rate vs freshness

A cache that makes stale or incorrect data hard to reason about can create more pain than it saves.

## Centralization vs team autonomy

Shared platforms can reduce duplicated effort, but they also create coordination and ownership bottlenecks.

## Rich abstractions vs operational clarity

Do not hide critical failure behavior behind abstractions nobody can debug during incidents.
