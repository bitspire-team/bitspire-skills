# Bitspire Skills

Curated agent skills by Bitspire — workflows, automations, and best practices for AI-assisted development.

## Available Plugins

| Plugin | Description | Version |
|--------|-------------|---------|
| [self-learning](plugins/self-learning/) | A draft-and-compact documentation learning loop that teaches your AI agent to capture decisions and maintain living documentation. | 1.0.0 |

## Installation

### VS Code (Agent Plugin)

1. Open Command Palette → `Chat: Install Plugin From Source`
2. Paste: `https://github.com/bitspire-team/bitspire-skills`

Or add to your VS Code settings to browse all plugins:
```json
"chat.plugins.marketplaces": ["bitspire-team/bitspire-skills"]
```

### Copilot CLI

Install a specific plugin:
```shell
copilot plugin install bitspire-team/bitspire-skills:plugins/self-learning
```

Or register the marketplace and browse:
```shell
copilot plugin marketplace add bitspire-team/bitspire-skills
copilot plugin install self-learning@bitspire-skills
```

### Claude Code

```shell
claude plugin add bitspire-team/bitspire-skills
```

### Manual (any system)

Clone this repo and point your tool at the plugin folder:
```shell
git clone https://github.com/bitspire-team/bitspire-skills.git
```

## Plugin Structure

Each plugin lives in `plugins/<name>/` and contains:
- `plugin.json` — metadata and component paths
- `skills/` — one or more agent skills with `SKILL.md` instructions and `assets/`

## Contributing

Open an issue or PR to suggest new skills or improvements to existing ones.

## License

MIT
