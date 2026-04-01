---
description: Refactor a file — usage: /refactor <file> [instructions]
---

Arguments: $ARGUMENTS

Parse the arguments as follows: the first token is the file path to refactor; everything after it is additional instructions. If only one token is provided, there are no additional instructions.

Rules:
- Read the file in full before making any changes.
- Do not change behavior — only improve structure, clarity, or maintainability.
- Match the conventions already present in the codebase.
- Remove dead code. Do not comment it out.
- Do not add comments that just restate what the code does.
- If no additional instructions are provided, use your judgment on what most needs improving.

After refactoring, briefly state what you changed and why.
