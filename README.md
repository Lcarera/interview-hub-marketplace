# Interview Hub Marketplace

A proof-of-concept Claude Code marketplace that provides plugins with domain-specific skills for the [Interview Hub](https://github.com/lcarera/interview_hub) project.

## Available plugins

| Plugin | Description |
|--------|-------------|
| [`interview-hub-common-skills`](plugins/interview-hub-common-skills/) | Domain skills for adding email types, creating Supabase migrations, running pre-PR checks, and debugging production issues on Cloud Run |

## Installation

### Claude Code CLI

```bash
# Add this marketplace
claude plugin marketplace add lcarera/interview-hub-marketplace

# Install a plugin
claude plugin install interview-hub-common-skills
```

### Claude Desktop

1. Open **Customize** (bottom-left menu)
2. Click **Add plugins**
3. Select **Create plugin**
4. Choose **Add marketplace**
5. Paste the repository URL: `https://github.com/lcarera/interview-hub-marketplace`
6. Go back to **Add plugins** — a new **Personal** tab will appear with the plugins from the marketplace
7. Install the desired plugins from there

## Creating your own plugin

If you want to create your own Claude Code plugin, install the [plugin-dev](https://github.com/anthropics/claude-plugins-official) plugin. It includes skills and agents for scaffolding plugins, writing skills, creating hooks, and validating your plugin structure:

```bash
claude plugin marketplace add anthropics/claude-plugins-official
claude plugin install plugin-dev
```

## Repository structure

```
interview-hub-marketplace/
├── .claude-plugin/
│   └── marketplace.json                        # Marketplace index
├── plugins/
│   └── interview-hub-common-skills/
│       ├── .claude-plugin/
│       │   └── plugin.json                     # Plugin manifest
│       ├── skills/
│       │   ├── add-email-type/SKILL.md
│       │   ├── create-migration/SKILL.md
│       │   ├── pr-check/SKILL.md
│       │   └── prod-debug/SKILL.md
│       └── README.md
└── README.md
```
