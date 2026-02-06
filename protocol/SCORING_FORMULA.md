# SCORING FORMULA (Tier-0 Canonical)

## Definition
Mathematical aggregation of Behavior signals → Reap score.

## Formulascore = 0.5×playback + 0.2×viewport + 0.1×volume +
0.1×mouse_entropy + 0.05×timing + 0.05×hover
## Verification Threshold
score ≥ 0.70 = "verified"
score < 0.70 = "rejected"

## Detailed Calculation
Each behavior contributes: intensity × TAXONOMY weight

| Behavior | Weight | Example (intensity=0.85) |
|----------|--------|-------------------------|
| playback | 0.5    | 0.85 × 0.5 = 0.425     |
| viewport | 0.2    | 0.85 × 0.2 = 0.170     |
| volume   | 0.1    | 0.85 × 0.1 = 0.085     |
| **Total** | **1.0** | **≥0.70 = verified**    |

## Constraints
- Weights from TAXONOMY.md (immutable)
- Intensity ∈ [0.0, 1.0] per BEHAVIOR.md
- Threshold 0.70 fixed (Tier-0)

## Reference
TAXONOMY.md
BEHAVIOR.md
REAP.md
