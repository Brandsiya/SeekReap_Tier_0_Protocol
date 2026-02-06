# CANONICAL OPERATIONS (Tier-0 Protocol)

## create_seeker()
Creates a new Seeker.
- Output: id: uuid, created_at: timestamp, status: active
- Invariants: id unique, status=active

## create_reap(seeker_id)
Creates a new Reap session.
- Input: seeker_id exists
- Output: id: uuid, status: pending, start_time set

## record_behavior(reap_id, behavior)
Records a Behavior.
- Invariants: reap exists, intensity ∈ [0,1], timestamp in reap window

## verify_reap(reap_id)
Calculates score and assigns status.
- verified: score ≥ 0.70 AND behaviors ≥ 3
- else: rejected

## emit_verification_event(reap_id)
Emits final verification signal.
- Constraints: reap verified, emit once only
