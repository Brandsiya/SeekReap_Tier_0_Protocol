# TAXONOMY (Tier-0 Canonical)

## Definition
Fixed weights for Behavior types → Reap score calculation.

## Behavior Type Weights
| Type            | Weight | Metric          |
|-----------------|--------|-----------------|
| playback        | 50%    | video watched   |
| viewport        | 20%    | screen focus    |
| volume          | 10%    | audio           |
| mouse_entropy   | 10%    | human           |
| timing          | 5%     | pace            |
| hover           | 5%     | CTA             |

## Constraints
- Weights MUST sum to 100%
- Types MUST match BEHAVIOR.md enum
- Weights are IMMUTABLE (Tier-0 fixed)

## Formula Reference
Reap Score = Σ(behavior_intensity × type_weight)

## Examples
playback (0.85 intensity) × 50% = 0.425 score contribution

## Reference
BEHAVIOR.md
SCORING_FORMULA.md
invariants/MATHEMATICAL.md
