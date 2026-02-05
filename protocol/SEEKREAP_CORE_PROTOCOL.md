# SEEKREAP CORE PROTOCOL v1.0.0 (FROZEN - Feb 5, 2026)

## DOMAIN MODELSEEKER → [0-to-many REAP] → [0-to-many BEHAVIOR] → VERIFIED HUMAN SIGNAL
## CORE INVARIANTS
1. `reap.duration == end_time - start_time`
2. `reap.score >= 0.70 → status = "verified"`  
3. `behavior.intensity ∈ [0.0, 1.0]`

## SCORING FORMULAscore = 0.5×playback + 0.2×viewport + 0.1×volume + 0.1×mouse_entropy + 0.05×timing + 0.05×hover
