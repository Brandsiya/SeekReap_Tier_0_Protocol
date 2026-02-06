# RELATIONAL CONSTRAINTS (Tier-0 Canonical)

1. **Foreign Key:** seeker.id = reap.seeker_id
2. **Cardinality:** reap.status="verified" → COUNT(behavior) >= 3  
3. **Reference Integrity:** behavior.reap_id → valid reap

## Implications
- No orphan behaviors (all link to existing Reaps)
- Verified Reaps require minimum 3 Behaviors
- Seeker → Reap → Behavior referential chain enforced
