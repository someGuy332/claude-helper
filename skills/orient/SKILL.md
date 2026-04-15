---
name: orient
description: "Use at session start before exploring files, asking questions, or touching code"
---

Orient before acting. Prevents re-exploring known territory.

**Steps:**
1. Read `~/.claude/projects/[project]/memory/MEMORY.md` — load user preferences, prior context
2. `git status` + `git log --oneline -5` — current branch state
3. Summarize in ≤3 bullets: what project does, branch state, relevant memory
4. Proceed with task

**Skip if:**
- Already mid-session with context loaded
- User provided full context in message

Memory beats re-discovery. Don't re-read files already summarized in memory.
