---
name: plan
description: "Use when breaking down a feature, bug fix, or refactor before writing any code"
---

Write plan before touching code.

**Structure:**
```
## Goal
[One sentence: problem this solves]

## Approach
[2-3 sentences: chosen solution + why]

## Steps
1. [File + what changes — specific]
2. ...

## Risks
- [What could break, edge cases]
```

**Rules:**
- Steps name specific files, not vague actions (`Edit auth.ts:45` not "fix auth")
- Search for existing utilities before planning new code
- 5–15 steps max — split plan if larger
- Read critical files before writing plan
- Ask one clarifying question if scope unclear — then plan

Write plan to file if task spans multiple sessions. Stop at plan, don't execute.
