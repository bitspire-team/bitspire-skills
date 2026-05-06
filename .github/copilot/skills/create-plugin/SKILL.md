---
name: create-plugin
description: "Procedure and guidelines for creating a new Bitspire plugin in the repository."
---

# Create Plugin Procedure

1. **Create Directory:** Create the directory `plugins/<plugin-name>/`
2. **Create Manifest:** Add `plugin.json` with metadata (`name`, `description`, `version`) and map paths for `"agents": "agents/"` or `"skills": "skills/"` as applicable.
3. **Structure Components:** Structure Agents in `agents/<name>.agent.md` and Skills in `skills/<name>/SKILL.md`.
4. **Register in Marketplace:** Register the plugin by appending it to the `.github/plugin/marketplace.json` manifest.
