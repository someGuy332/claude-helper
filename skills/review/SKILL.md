---
name: review
description: "Use before requesting a code review or when receiving and addressing review feedback"
---

**Before requesting review:**
- [ ] All tests pass locally
- [ ] No debug logs / commented-out code left
- [ ] Reviewed your own diff — no accidental includes
- [ ] PR description states: what changed + why (not just what)
- [ ] Breaking changes explicitly flagged

**When receiving feedback:**
1. Read all comments before responding to any
2. Separate: objective issues (fix) vs style preferences (discuss)
3. Every comment gets one of: fix, decline with reason, ask for clarification — never ignore
4. Don't defend first-draft code — evaluate feedback on merit
5. After addressing: re-run tests, confirm nothing broke

**Don't:**
- Mark resolved without actually fixing
- Push back on all style feedback reflexively
- Merge with unresolved comments without explicit agreement
