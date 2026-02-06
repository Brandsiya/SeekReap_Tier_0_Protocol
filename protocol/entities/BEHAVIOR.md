# BEHAVIOR ENTITY (Tier-0 Canonical)

## Definition
Single proof signal captured during a Reap session.

## Fields
```yaml
<<<<<<< HEAD
id: uuid
reap_id: uuid
type: enum
intensity: float
timestamp: timestamp
```
## Optional Fields
```yaml
metadata: object
=======
id: uuid                   # unique identifier for th>
reap_id: uuid              # references the Reap this>
type: enum                 # one of ["playback","view>
intensity: float           # 0.0 to 1.0
timestamp: timestamp       # when this behavior occur>
metadata: object           # optional, implementation>
>>>>>>> 87ddceb (Tier-0 formatting complete: 100% clean)
```
## Constraints
reap_id MUST reference a valid Reap
type MUST be one of ["playback","viewport","volume",">
intensity MUST be in range [0.0, 1.0]
timestamp MUST be within Reap start/end time
Each type has a fixed weight (see TAXONOMY.md)

## Relationships
<<<<<<< HEAD
ONE Behavior -> ONE Reap
=======
ONE Behavior → ONE Reap
>>>>>>> 87ddceb (Tier-0 formatting complete: 100% clean)
Behaviors aggregate into Reap score

## Examples
```yaml
{
  "id": "b1",
  "reap_id": "reap-456",
  "type": "playback",
  "intensity": 0.85,
  "timestamp": "2026-02-05T16:00:02Z",
  "metadata": {}
}
```
## Reference
TAXONOMY.md
SCORING_FORMULA.md
invariants/MATHEMATICAL.md
