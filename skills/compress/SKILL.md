---
name: compress
description: "Use when conversation is long, context feels cluttered, or before starting a large multi-step task"
---

Manage context window before quality degrades.

**When to compress:**
- Messages exceed ~50 turns
- About to start task requiring many tool calls
- Key decisions buried deep in history

**Before /compact:**
1. Write critical state to a file (e.g. `_session.md`):
   - Current task + progress
   - Decisions made this session (not in code/CLAUDE.md)
   - Files modified
   - Next steps
   - Unresolved questions
2. Run `/compact`
3. Read `_session.md` first thing after compaction

**Preserve:** explicit user decisions, error patterns discovered, stated constraints.
**Skip:** code content (re-read files), git history (re-run `git log`), anything already in CLAUDE.md or memory.
