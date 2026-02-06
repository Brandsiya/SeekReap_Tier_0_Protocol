# RELATIONAL CONSTRAINTS (Tier-0 Canonical)

1. seeker.id = reap.seeker_id (FK constraint)
2. reap.status="verified" → COUNT(behavior) >= 3
3. behavior.reap_id → valid reap
