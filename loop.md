---
configured: true
interval: 1
timeout: 30
description: "Watch .squad/inbox/ for new work items and process them"
---

# Inbox Watcher Loop

Each cycle, you will:

1. List all markdown files in `.squad/inbox/`
2. If no files exist, report "Inbox empty" and end this cycle
3. For each file found:
   - Read its contents (the work request)
   - Route the work to the appropriate agent based on `.squad/routing.md`
   - Execute the work described in the file
   - Once completed, move the file to `.squad/inbox/done/` (create the directory if it does not exist)
4. Report what was processed

Rules:
- Process files in alphabetical order
- Only process `.md` files
- Never delete inbox files and always move to `done/`
- If a file instruction is unclear, move it to `.squad/inbox/blocked/` with a note