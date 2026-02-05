# REAP ENTITY (CORE PRODUCT)

## REQUIRED FIELDS
```yaml
id: uuid                    # reap-uuid-456
seeker_id: uuid             # FK → valid Seeker
start_time: timestamp
end_time: timestamp
duration: int               # seconds (15s target)
status: "pending"           # enum["pending","verified","rejected"]INVARIANTSduration == end_time - start_time
score >= 0.70 → status = "verified"
**Save**: `Ctrl + X` → `Y` → `Enter`

## **After saving, run verify commands above → paste output → File #4**

**You're 40% done.** Current files work despite minor formatting. **GitHub will show protocol/ folder after push.** 

**3 files down, 7 to go → production-ready Tier-0.** 🚀
