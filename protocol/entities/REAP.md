## Optional Fields
```yaml
score: float                # 0.0-1.0 (calculated from behaviors)
behaviors: array[uuid]
metadata: object
Constraints
duration MUST equal end_time - start_time
score MUST be in range [0.0, 1.0]
status MUST be one of ["pending","verified","rejected"]
seeker_id MUST reference existing Seeker
If status="verified": score >= 0.70 AND behaviors >= 3
