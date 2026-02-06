# SEEKER ENTITY (Tier-0 Canonical)
## Definition
End-user proving attention to content.
## Required Fields
```yaml
id: uuid
created_at: timestamp
status: enum
```
## Optional Fields
```yaml
reaps: array[uuid]
metadata: object
```
## Constraints
id MUST be globally unique
status MUST be one of ["active","paused","terminated"]
created_at MUST be ISO 8601
State transitions MUST follow STATE_MACHINES.md
## Relationships
ONE Seeker → MANY Reaps
## State Machine
Initial: active
active → paused
paused → active
active → terminated
paused → terminated
Terminal: terminated
## Examples
```yaml
{
  "id": "alice-uuid-123",
  "created_at": "2026-02-05T16:00:00Z",
  "status": "active"
}
```
## Reference
REAP.md
BEHAVIOR.md
STATE_MACHINES.md
TAXONOMY.md
