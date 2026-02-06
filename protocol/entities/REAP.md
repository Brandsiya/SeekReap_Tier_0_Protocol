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
```
## Optional Fields
```yaml
score: float
behaviors: array[uuid]
```
## Constraints
duration == end_time - start_time
score ∈ [0.0,1.0]
status ∈ ["pending","verified","rejected"]
## Relationships
ONE Reap -> ONE Seeker
MANY Behaviors -> ONE Reap
## Examples
```yaml
{
  "id": "reap-456",
  "seeker_id": "alice-uuid-123",
  "start_time": "2026-02-05T16:00:00Z",
  "end_time": "2026-02-05T16:05:00Z",
  "duration": 300,
  "status": "verified"
}
```
## Reference
SEEKER.md
BEHAVIOR.md
TAXONOMY.md
