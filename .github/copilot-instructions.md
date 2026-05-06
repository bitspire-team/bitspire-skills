# Bitspire Skills - Copilot Instructions

## Repository Overview

This repository contains curated AI agent skills and plugins (such as the `self-learning` plugin) by Bitspire. These plugins define AI workflows, automations, and continuous learning loops for AI-assisted development. Skills are defined using Markdown (`SKILL.md`) and structured via `plugin.json`.

## Tech Stack

- **Agent Instructions:** Markdown (`SKILL.md`, `.instructions.md`) and YAML/JSON.
- **Skill Metadata:** JSON (`plugin.json`).
- **Prompt Evaluation & Testing:** **Promptfoo** (used to evaluate `SKILL.md` instructions, enforce specific LLM behaviors, and prevent prompt drift).
- **Primary Environments:** VS Code, GitHub Copilot, Claude Code.

## Development Guidelines

- **Testing Skills:** When modifying or creating new skills, always write Promptfoo evaluation test cases to ensure the LLM respects the constraints and doesn't drift.
- **Skill Structure:** Each skill must live in `plugins/<plugin-name>/skills/<skill-name>/` and contain a `SKILL.md` file. Templates should be placed in an `assets/` subdirectory.
- **Tone & Style:** Maintain concise, imperative instructions in `SKILL.md` files so the agent clearly understands its boundaries.
- **Team Preference:** All team members use 4-space indents. Strictly avoid using tools with less than 10k downloads.
