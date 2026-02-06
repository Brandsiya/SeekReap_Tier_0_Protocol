# BEHAVIOR ENTITY (Tier-0 Canonical)

## Definition
Single proof signal captured during a Reap session.

## Required Fields
```yaml
id: uuid
reap_id: uuid
type: enum
intensity: float
timestamp: timestamp
```
## Optional Fields
```yaml
metadata: object
```
## Constraints
reap_id MUST reference a valid Reap
type MUST be one of ["playback","viewport","volume","mouse_entropy","timing","hover"]
intensity MUST be in range [0.0, 1.0]
timestamp MUST be within Reap start/end time
Each type has a fixed weight (see TAXONOMY.md)

## Relationships
ONE Behavior -> ONE Reap
Behaviors aggregate into Reap score

## Examples
```yaml
{
  "id": "b1",
  "reap_id": "reap-456",
  "type": "playback",
  "intensity": 0.85,
  "timestamp": "2026-02-05T16:00:02Z"
}
```
## Reference
TAXONOMY.md
SCORING_FORMULA.md
invariants/MATHEMATICAL.md
