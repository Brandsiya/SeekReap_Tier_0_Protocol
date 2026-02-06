# SCORING FORMULA (Tier-0 Canonical)

## Reap Score
score = 0.5×playback + 0.2×viewport + 0.1×volume +
0.1×mouse_entropy + 0.05×timing + 0.05×hover


## Threshold
≥ 0.70 = **verified**
< 0.70 = **rejected**

## Weights Reference
See TAXONOMY.md (sums to 1.0)

## Status Update
REAP.status = "verified" if score ≥ 0.70
REAP.status = "rejected" if score < 0.70
