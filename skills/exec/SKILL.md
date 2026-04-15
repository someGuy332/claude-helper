---
name: exec
description: "Use when executing an implementation plan step by step in the current session"
---

Execute plan sequentially. One step at a time.

**Process:**
1. Read full plan — confirm steps are clear
2. Execute step N
3. Verify step N worked (run test/command/check output)
4. Mark complete, proceed to N+1
5. After all steps: invoke `verify` skill

**Stop and confirm if:**
- Step fails unexpectedly
- Step requires destructive action (delete, overwrite, force push)
- Scope expands beyond original plan
- Two consecutive steps fail

**Don't:**
- Skip steps "because obviously fine"
- Execute multiple steps before verifying each
- Continue past a failed step without diagnosis

**If blocked:** state what step failed, exact error, what was tried. Ask for guidance. Don't invent workarounds that change plan scope.
