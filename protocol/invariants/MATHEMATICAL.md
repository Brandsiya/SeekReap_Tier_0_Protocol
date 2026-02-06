# MATHEMATICAL INVARIANTS (Tier-0 Canonical)

## Core Equations

1. **Duration invariant:**reap.duration == end_time - start_time
2. **Intensity bounds:**behavior.intensity ∈ [0.0, 1.0]
3. **Score aggregation:**reap.score == Σ(behavior.intensity × weight)

## Implications
- Duration computed, not stored
- All intensities normalized [0,1]
- Score mathematically determined by TAXONOMY.md weights

## Reference
REAP.md
BEHAVIOR.md
TAXONOMY.md
SCORING_FORMULA.md
