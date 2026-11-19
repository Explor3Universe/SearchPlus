---
description: Explaining a shell command, no external facts
tags: [trigger]
runs: 3
max_turns: 3
timeout_seconds: 300
allowed_tools: [Skill, Read]
---

Explain what this command does, piece by piece: find . -name '*.log' -mtime +7 -delete
