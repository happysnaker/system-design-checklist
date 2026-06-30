# System Design Answer Sheet

Use this as a compact prompt sheet during:

- system design interviews
- architecture reviews
- lightweight design docs
- backend service proposal discussions

The goal is not to memorize fancy components. The goal is to stay structured, explicit, and practical.

## 1. Start with the problem

- Who is the user or caller?
- What is the primary request or workflow?
- What is in scope for this discussion?
- What is explicitly out of scope?
- What matters most here: latency, throughput, durability, correctness, or cost?

## 2. Size the system quickly

- Expected DAU / MAU?
- Peak QPS / RPS?
- Read / write ratio?
- Storage growth over 6–12 months?
- Hot-key, tenant skew, or burst traffic risks?
- Latency target (for example, p95 / p99)?

## 3. Draw the high-level architecture

Use a simple first pass:

`client -> API / gateway -> service -> cache / queue / database`

Then explain:

- service boundaries
- sync vs async parts
- where state lives
- which parts are on the critical path

## 4. Define the API and contracts

- Main endpoints or RPCs
- Request / response shape
- Idempotency expectations
- Error model
- Pagination / filtering / retries

## 5. Model the data

- Core entities
- Main access patterns
- Primary storage choice and why
- Required indexes
- Partition / shard key if needed
- Schema evolution risk

## 6. Explain the read path

- Normal request flow
- Cache location and eviction strategy
- Cache miss behavior
- Hot-key handling
- Fallback / degraded read behavior

## 7. Explain the write path

- Validation and persistence flow
- Sync confirmation vs async work
- Queue / stream usage
- Retry behavior
- Deduplication / idempotency strategy
- Partial failure handling

## 8. Call out consistency and correctness

- Where do you need strong consistency?
- Where is eventual consistency acceptable?
- Which invariants must never break?
- What can race?
- How do you prevent duplicate effects?

## 9. Talk about failure and reliability

- Dependency timeout behavior
- Retries / backoff / circuit breaking
- Queue backlog or consumer failure handling
- Blast radius of a bad deploy
- Graceful degradation path
- Recovery plan after backlog or outage

## 10. Add observability and operations

- Logs needed for debugging
- Key metrics
- Useful traces / spans
- Core alerts and dashboards
- Runbooks or operational notes

## 11. Cover security and abuse

- Authn / authz model
- Sensitive data handling
- Rate limiting / abuse control
- Auditability requirements
- Retention / deletion obligations

## 12. Finish with rollout and tradeoffs

- Safe deployment plan
- Backward compatibility concerns
- Rollback plan
- What would you defer to v2?
- Which assumption is most likely to fail first?

## Good sentence starters

- “I’ll start with the simplest design that satisfies the current scale and reliability target.”
- “I’d keep the first version single-region unless multi-region is a hard requirement.”
- “The main tradeoff here is correctness versus latency.”
- “I’d make the write path idempotent before optimizing it.”
- “I want to be explicit about the failure mode and the degraded behavior.”

## Common interview closing line

> I’d ship the simple version first, instrument it well, and only add more complexity when scale or correctness requirements force it.
