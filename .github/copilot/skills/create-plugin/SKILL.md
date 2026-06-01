---
name: create-plugin
description: "Procedure and guidelines for creating a new Bitspire plugin in the repository."
---

# Create Plugin Procedure

1. **Create Directory:** Create the directory `plugins/<plugin-name>/`. Plugin names must be lowercase, hyphen-separated, and contain only alphanumeric characters and hyphens (e.g. `my-plugin`).
2. **Create Manifest:** Add `plugin.json` with metadata (`name`, `description`, `version`). Include `"agents": "agents/"` if the plugin contains agents, `"skills": "skills/"` if it contains skills, or both if it contains both.
3. **Structure Components:** Structure Agents in `agents/<name>.agent.md` and Skills in `skills/<name>/SKILL.md`.
4. **Register in Marketplace:** Register the plugin by appending it to the `.github/plugin/marketplace.json` manifest. Append an object with `{"name": "<plugin-name>", "path": "plugins/<plugin-name>/", "version": "<version>"}` to the array in marketplace.json.
