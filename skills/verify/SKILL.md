---
name: verify
description: "Use when about to report task complete, say something works, or claim a fix succeeded"
---

Before claiming done, collect evidence — don't assert.

**Checklist:**
- [ ] Run the code / test / command — don't trust mental models
- [ ] Output matches expected behavior (not just "no errors")
- [ ] Edge cases tested: empty input, boundary values, error paths
- [ ] No regressions: existing tests still pass
- [ ] Claim matches scope: only say "done" for what was asked

**Never say:**
- "This should work" without running it
- "Tests pass" without running them
- "Fixed" without reproducing the original failure first

If evidence incomplete → state what's missing, don't claim success.
