# interview-hub-common-skills

A Claude Code plugin that packages domain-specific skills for the [Interview Hub](https://github.com/lcarera/interview_hub) project.

Gives Claude contextual knowledge about the Interview Hub codebase so it can guide you through common workflows without you having to explain the project's conventions each time.

## Skills

| Skill | Trigger | What it does |
|-------|---------|--------------|
| `add-email-type` | Auto + `/add-email-type` | Walks through adding a new email notification type to the async email system |
| `create-migration` | `/create-migration` only | Generates a sequentially-numbered Supabase migration file |
| `pr-check` | `/pr-check` only | Runs backend + frontend tests locally before creating a PR |
| `prod-debug` | Auto + `/prod-debug` | Guides production debugging on Cloud Run (logs, secrets, common errors) |

**Auto** means Claude will invoke the skill automatically when it detects a relevant request. Skills marked with **only** require an explicit slash command.

## Installation

```bash
claude plugin marketplace add lcarera/interview-hub-marketplace
claude plugin install interview-hub-common-skills
```
