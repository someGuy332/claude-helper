# claude-helper

Lean workflow plugin for Claude Code. Superpowers-equivalent, ~50% fewer tokens. No hooks, no startup overhead.

## Skills

| Skill | Purpose | Token target |
|-------|---------|-------------|
| `use` | Meta-dispatcher — which skill to invoke | 80w |
| `orient` | Session startup — load memory + git state | 100w |
| `compress` | Context hygiene — when/how to /compact | 120w |
| `plan` | Write implementation plans before coding | 180w |
| `exec` | Execute plans step by step | 180w |
| `debug` | Systematic 4-phase debugging | 220w |
| `tdd` | Test-driven development discipline | 320w |
| `review` | Code review — pre-request + receiving | 140w |
| `parallel` | Dispatch parallel agents | 150w |
| `verify` | Verify before claiming done | 120w |

## vs Superpowers

- No session hooks (zero startup token cost)
- Caveman-style prose (~40% shorter per skill)
- Rationalization tables trimmed to top 3
- No "Real-World Impact" sections
- `orient` + `compress` are new — not in superpowers

## Installation

### Option 1: Local (manual)

1. Add to `~/.claude/settings.json`:
```json
{
  "enabledPlugins": {
    "claude-helper@local": true
  }
}
```

2. Register in `~/.claude/plugins/installed_plugins.json`:
```json
{
  "claude-helper": {
    "marketplace": "local",
    "version": "1.0.0",
    "path": "/path/to/claude_helper"
  }
}
```

### Option 2: GitHub

Push to GitHub, then install via:
```
/plugin install claude-helper@your-marketplace
```

## Usage

Skills auto-invoke based on CSO descriptions. To invoke manually:
```
/use          — pick right skill for task
/orient       — orient at session start
/compress     — manage long context
/plan         — write a plan
/exec         — execute a plan
/debug        — systematic debugging
/tdd          — TDD discipline
/review       — code review workflow
/parallel     — parallel agent dispatch
/verify       — verify before claiming done
```
