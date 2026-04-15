---
name: tdd
description: "Use when writing new functionality, fixing bugs that need coverage, or modifying code in a tested codebase"
---

**IRON LAW: No production code without a failing test first.**

Write code before the test? Delete it. Start over. No exceptions.

**Red-Green-Refactor:**
1. **RED** — Write failing test for one behavior. Run it. Confirm it fails (right reason).
2. **GREEN** — Write minimal code to pass. Nothing extra.
3. **REFACTOR** — Clean up. Tests still green? Commit.
4. Repeat for next behavior.

**Minimal means minimal:**
- One `if` when one `if` suffices
- No "I'll need this later" code
- No error handling not yet tested

**Top 3 rationalizations — all wrong:**

| Excuse | Reality |
|--------|---------|
| "I know what the code needs, tests slow me down" | You don't. Tests reveal design flaws before they compound. |
| "Simple fix, no test needed" | Simple bugs recur. Test costs 2 min. Re-debug costs 30. |
| "I'll write tests after, just want to see it work first" | "After" never comes. Untested code ships. |

**Test anatomy:**
```
// Arrange — set up state
// Act — call the thing
// Assert — one behavior
```

**Never:**
- Write tests that pass immediately (means code came first)
- Test implementation details — test behavior
- Delete a test because it's inconvenient

**Brownfield (no existing tests):**
Write characterization tests for code you must change. Test it, then change it.

**No test framework exists:**
Add one before writing feature code.
