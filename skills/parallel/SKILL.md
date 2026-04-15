---
name: parallel
description: "Use when a task has multiple independent subtasks that don't share state or depend on each other's output"
---

Dispatch agents for truly independent work. Sequential otherwise.

**Parallelize if ALL true:**
- Tasks don't share mutable state
- Task B doesn't need Task A's output
- Tasks can be reviewed independently

**Keep sequential if ANY true:**
- Task B reads files Task A writes
- Order matters for correctness
- Tasks share a DB/service/config

**Dispatch pattern:**
- Write clear isolated brief per agent: specific files, exact goal, constraints, what NOT to change
- Collect all results before integrating
- Integrate, then invoke `verify`

**Model selection:**
- Complex reasoning (architecture, debugging): Opus
- Implementation (code to spec): Sonnet
- Simple transforms (rename, reformat): Haiku

**Never parallelize:** git operations, DB migrations, tasks that "might" overlap.
