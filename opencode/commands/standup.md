---
description: Summarize recent git activity for a standup update
subtask: true
---

Here is the recent git activity:
!`git log --oneline --since="2 days ago" --author="$(git config user.email)" 2>/dev/null || git log --oneline -10`

Here are any uncommitted changes:
!`git status --short`

Write a brief standup update covering:
- What was completed (from commits)
- What is in progress (from uncommitted changes or WIP commits)

Keep it to 3-5 sentences max. Write in first person. Skip filler phrases like "I worked on" — just state what happened.
