---
name: debug
description: "Use when investigating a bug, unexpected behavior, error message, or test failure"
---

Systematic 4-phase debugging.

**Phase 1 — Reproduce**
- Get exact error + stack trace
- Find minimal reproduction case
- Confirm bug is reproducible before proceeding

**Phase 2 — Locate**
- Trace execution path backward from error
- Find last known-good state
- Narrow to specific file + line range
- Don't fix yet

**Phase 3 — Understand**
- Read the failing code
- Form hypothesis: what causes this?
- Test hypothesis (add logging, check values)
- Confirm root cause before fixing

**Phase 4 — Fix + Verify**
- Fix root cause only (not symptoms)
- Run original reproduction — confirm fixed
- Run full test suite — confirm no regressions

**Common traps:**

| Trap | Reality |
|------|---------|
| "Obvious fix" without reading code | Fixes symptom, not cause |
| Fixing during Phase 2 | Introduces new bugs |
| "Tests pass so fixed" | Tests may not cover bug path |

Stop at Phase 1 if can't reproduce. Document conditions, ask user.
