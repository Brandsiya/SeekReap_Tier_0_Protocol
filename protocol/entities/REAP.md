# REAP ENTITY (Tier-0 Canonical)

## Definition
Single verification session proving human attention.

## Required Fields
```yaml
id: uuid                    # reap-uuid-123
seeker_id: uuid             # references seeker.id
start_time: timestamp       # 2026-02-05T16:00Z  
end_time: timestamp         # 2026-02-05T16:05Z
duration: seconds           # 300 (5 minutes)
status: enum                # pending|verified|rejected
score: float                # 0.0-1.0 [0.72]Constraintsduration == end_time - start_timescore ∈ [0.0,1.0]status ∈ ["pending","verified","rejected"]seeker_id MUST exist
