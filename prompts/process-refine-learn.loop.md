---
configured: true
interval: 1
timeout: 30
description: "Process a prompt defined in this Markdown file"
---

# Prompt File Processing

Use this file as the source prompt for the cycle.

Task:
1. Read the request in `.squad/inbox/refine-learn-skill.md`.
2. Refine the skill at `plugins/self-learning/skills/learn/SKILL.md`.
3. Keep instructions concise and imperative.
4. Respect token and prompt constraints already defined in the skill.
5. Run Promptfoo evaluation after changes.
6. Report a brief summary of what changed and test results.

Execution constraints:
- Do not create unrelated files.
- Do not modify plugins outside `plugins/self-learning/skills/learn/` unless required by tests.
- If tests fail, report the failure clearly and stop.