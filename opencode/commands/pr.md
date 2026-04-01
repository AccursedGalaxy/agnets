---
description: Draft a pull request description from recent commits
subtask: true
---

Here is the git log for this branch compared to the base branch:
!`git log --oneline $(git merge-base HEAD $(git rev-parse --abbrev-ref --symbolic-full-name @{u} 2>/dev/null || echo main))..HEAD 2>/dev/null || (echo "WARNING: could not resolve upstream branch, falling back to last 10 commits" && git log --oneline -10)`

Here is the full diff:
!`git diff $(git merge-base HEAD $(git rev-parse --abbrev-ref --symbolic-full-name @{u} 2>/dev/null || echo main))..HEAD 2>/dev/null || (echo "WARNING: could not resolve upstream branch, falling back to HEAD~5..HEAD" && git diff HEAD~5..HEAD)`

Write a pull request description with:
- A concise title (one line, imperative mood)
- A short summary paragraph explaining *why* this change exists, not just what changed
- A bullet list of the notable changes
- Any follow-up work or known limitations, if relevant

Do not include sections that are empty or not applicable. Output plain markdown.
