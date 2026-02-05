# SeekReap Protocol Specification v1.0.0 FROZEN

## 1. DOMAIN MODELSEEKER → [0-N] REAP → [0-N] BEHAVIOR → VERIFICATION EVENT
## 2. CORE INVARIANTS (8 total)
1. reap.duration == end_time - start_time  
2. behavior.intensity ∈ [0.0,1.0]
3. reap.score = Σ(behavior.intensity × weight)
4. seeker.id = reap.seeker_id
5. verified → COUNT(behavior) ≥ 3
6. playback.weight = 0.50 IMMUTABLE
7. verification_threshold = 0.70
8. minimum_behaviors = 3

## 3. SCORING FORMULAscore = 0.5×playback + 0.2×viewport + 0.1×volume +
0.1×mouse_entropy + 0.05×timing + 0.05×hover
THRESHOLD: ≥ 0.70 = VERIFIED
## 4. CANONICAL OPERATIONScreate_seeker() → Seeker{id,created_at,status}create_reap(seeker_id) → Reap{id,seeker_id,duration}record_behavior(reap_id,{type,intensity})verify_reap(reap_id) → score ≥ 0.70 && behaviors ≥ 3emit_verification_event(reap_id) → VerificationEvent
## 5. ENTITY REFERENCES
See entities/{SEEKER,REAP,BEHAVIOR}.md
Invariants: invariants/{MATH,BUSINESS,RELATIONAL}.md
Taxonomy: TAXONOMY.md
