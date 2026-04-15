---
name: use
description: "Use at start of any non-trivial task to identify which skill applies"
---

Match task to skill before responding:

| Task | Invoke |
|------|--------|
| New session, unfamiliar state | `orient` |
| Context window large / long session | `compress` |
| Feature/fix needs planning | `plan` |
| Executing a plan step-by-step | `exec` |
| Bug, error, unexpected behavior | `debug` |
| Writing or modifying tested code | `tdd` |
| Preparing or receiving code review | `review` |
| Multiple independent subtasks | `parallel` |
| About to say "done" or "works" | `verify` |

If multiple apply: invoke most relevant first.
No skill matches: proceed normally.
