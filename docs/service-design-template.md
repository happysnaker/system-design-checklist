# Service design template

Use this when writing a lightweight design doc.

## 1. Problem

- What problem are we solving?
- Who is affected?
- What happens if we do nothing?

## 2. Scope

### In scope

- 

### Out of scope

- 

## 3. Requirements

### Functional

- 

### Non-functional

- Latency:
- Throughput:
- Availability:
- Durability:
- Consistency:

## 4. Traffic / scale assumptions

- Expected QPS:
- Peak QPS:
- Read/write ratio:
- Storage growth:
- Hotspot risks:

## 5. Proposed design

- High-level architecture
- Request flow
- Write flow
- Read flow
- Failure handling

## 6. Data model

- Entities
- Indexes
- Partitioning / sharding
- Retention / deletion

## 7. Tradeoffs

- Why this design?
- What alternatives were rejected?
- What risks remain?

## 8. Operations

- Metrics
- Logs
- Traces
- Alerts
- Runbooks

## 9. Rollout

- Migration plan
- Backward compatibility
- Rollback plan
- Validation plan
