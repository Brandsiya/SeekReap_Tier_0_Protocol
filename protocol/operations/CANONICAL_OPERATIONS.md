# CANONICAL OPERATIONS (Tier-0 Protocol)

## create_seeker()
Creates a new Seeker.

Output:
- id: uuid
- created_at: timestamp
- status: active

Invariants:
- id must be unique
- status must be active

---

## create_reap(seeker_id)
Creates a new Reap session.

Input:
- seeker_id must exist

Output:
- id: uuid
- status: pending
- start_time set

---

## record_behavior(reap_id, behavior)
Records a Behavior.

Invariants:
- reap must exist
- intensity in [0,1]
- timestamp within reap window

---

## verify_reap(reap_id)
Calculates score and assigns status.

Rules:
- verified if score ≥ 0.70 AND behaviors ≥ 3
- otherwise rejected

---

## emit_verification_event(reap_id)
Emits final verification signal.

Constraints:
- reap must be verified
- emitted once only
