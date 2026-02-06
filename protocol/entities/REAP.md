# REAP ENTITY (Tier-0 Canonical)

## Definition
Single verification session proving human attention.

## Required Fields
```yaml
id: uuid
seeker_id: uuid
start_time: timestamp
end_time: timestamp
duration: int
status: enum
## Optional fields
score: float
behaviors: array[uuid]
Constraints
duration == end_time - start_timescore ∈ [0.0,1.0]status ∈ ["pending","verified","rejected"]
