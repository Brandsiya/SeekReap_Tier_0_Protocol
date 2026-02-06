# STATE MACHINES (Tier-0 Canonical)

## Seeker
active → paused → terminated

## Reap  
pending → verified | rejected

## Valid States
**Seeker:** ["active","paused","terminated"]
**Reap:** ["pending","verified","rejected"]

## Constraints
- Terminal states irreversible
- Reap: score ≥ 0.70 = verified (SCORING_FORMULA.md)
