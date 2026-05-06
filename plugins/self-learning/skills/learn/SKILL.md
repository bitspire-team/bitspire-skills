---
name: learn
description: "Extracts insights from the current conversation and stores them in either User Memory (local/opinionated) or Workspace Files (project/shared) to make the agent smarter over time."
---

# Learn from Conversation

This skill extracts learnable content from the current conversation and persists it in the correct location based on its category. This creates a self-learning loop where the agent retains knowledge across sessions.

## Categorization & Routing Rules

1. **Local / Opinionated (User Memory)**
   - _Scope:_ Personal coding preferences, local environment quirks, and opinions on how the agent should behave.
   - _Destination:_ `User Memory`
   - _Action:_ Use the `memory` tool to create or update files in `/memories/` (e.g., `/memories/preferences.md`).

2. **Project / Shared (Workspace Context)**
   - _Scope:_ Project architecture, product requirements, documentation, team coding standards, and domain facts. 
   - _Destination:_ `Workspace Files`
   - _Action:_ Use `replace_string_in_file` tool to append/update team rules in `.github/copilot-instructions.md`, or the `create_file` tool to document requirements/designs in the `docs/` directory.

## Procedure

1. **Analyze:** Review the recent conversation to identify the core facts, decisions, preferences, or context that should be remembered.
2. **Categorize:** Classify each specified piece of knowledge as either "Local / Opinionated" or "Project / Shared".
3. **Persist:** Execute the corresponding tool action to save the knowledge.
4. **Report:** Output a brief summary to the user detailing what was learned and where it was saved.
