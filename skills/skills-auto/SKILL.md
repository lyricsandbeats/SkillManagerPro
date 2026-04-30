---
name: skills-auto
description: Toggle automatic skill restoration on/off, or set mode. Usage: /skills-auto off | /skills-auto mode session|ask
user-invocable: true
---

# Skills Auto

Manages automatic skill restoration behavior for this session.

## Commands

- `/skills-auto off` — disable proactive skill suggestions for this session
- `/skills-auto mode session` — restore skills automatically at session start
- `/skills-auto mode ask` — prompt before restoring each skill

## Behavior

When auto mode is active, Claude checks the session's initial prompt against `~/.claude/plugins/skill-manager-pro/index.json` keyword categories. If a category matches, suggest restoring the primary skill for that domain.

To manually restore skills: use `/restore-skill`.
