---
description: Find and run a prompt from `prompts/` that matches the input.
---

The user wants to run one of the prompts in the `prompts/` directory of this vault.

User input: $ARGUMENTS

Steps:
1. List the files in `prompts/` (ignore `README.md`).
2. Pick the single prompt file whose name most closely matches the user's input. Match on filename without extension, case-insensitive, substring or fuzzy. If two are close, prefer the shorter name.
3. If nothing reasonably matches, list the available prompts and ask which one — don't guess wildly.
4. If the input is empty, list the available prompts and ask which one.
5. Read the chosen prompt file.
6. Follow its instructions, treating the prompt body as the active task. Before doing anything destructive or structural, honor the propose-before-edit rules in `CLAUDE.md`.

If the user passed extra words after the prompt name (e.g. `/prompt inbox quick`), treat the trailing words as parameters/modifiers and apply them per the matched prompt's own conventions (e.g. `inbox-triage.md`'s quick vs full mode).

Briefly tell the user which prompt you matched before you start executing it, so they can correct you if the match was wrong.
