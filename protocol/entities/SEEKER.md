# SEEKER ENTITY (Tier-0 Canonical)

## Definition
End-user proving attention to content.

## Fields
```yaml
<<<<<<< HEAD
id: uuid
created_at: timestamp
status: enum
```
## Optional Fields
```yaml
reaps: array[uuid]

metadata: object
=======
id: uuid                   # unique identifier for the Seeker
created_at: timestamp       # ISO 8601 timestamp of account creation
status: enum                # one of ["active","paused","terminated"]
reaps: array[uuid]          # optional, list of Reap IDs
metadata: object            # optional, implementation-specific
>>>>>>> 87ddceb (Tier-0 formatting complete: 100% clean)
```
## Constraints
id MUST be globally unique
status MUST be one of ["active","paused","terminated"]
created_at MUST follow ISO 8601
State transitions MUST follow STATE_MACHINES.md

## Relationships
ONE Seeker → MANY Reaps

## State Machine
Initial: active
Transitions:
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
  "status": "active",
  "reaps": []
}
```
## Reference
<<<<<<< HEAD
REAP.md
BEHAVIOR.md
STATE_MACHINES.md
TAXONOMY.md
=======
STATE_MACHINES.md
entities/REAP.md
invariants/BUSINESS.md
>>>>>>> 87ddceb (Tier-0 formatting complete: 100% clean)
