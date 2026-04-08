# Interview Hub Marketplace

A Claude Code marketplace that provides plugins with domain-specific skills for the [Interview Hub](https://github.com/lcarera/interview_hub) project.

## Available plugins

| Plugin | Description |
|--------|-------------|
| [`interview-hub-common-skills`](plugins/interview-hub-common-skills/) | Domain skills for adding email types, creating Supabase migrations, running pre-PR checks, and debugging production issues on Cloud Run |

## Installation

```bash
# Add this marketplace
claude plugin marketplace add lcarera/interview-hub-marketplace

# Install a plugin
claude plugin install interview-hub-common-skills
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
