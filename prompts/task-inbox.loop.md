---
configured: true
interval: 5
timeout: 20
description: "Process local task files from .squad/inbox"
---

# Local Task Inbox Loop

Each cycle:

1. Read the Markdown files in `.squad/inbox/`.
2. If the inbox is empty, report that no task is ready and stop the cycle.
3. Pick one task file. Prefer the oldest ready task.
4. Complete only that task. Keep the scope bounded to the task file.
5. Run the narrowest validation that matches the files you changed.
6. Write a short result note to `.squad/outbox/<task-file-name>`.
7. If the task is complete, move it to `.squad/archive/`. If it is blocked, leave it in place and record the blocker in the outbox note.

Execution constraints:
- Do not take a second task in the same cycle.
- Do not create unrelated files.
- Keep changes small and verifiable.
- If the task is ambiguous, record the blocker and stop the cycle.