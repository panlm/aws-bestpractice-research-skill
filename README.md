# panlm/skills

A collection of agent skills for AWS operations, best practices research, and cloud infrastructure management.

## Install

```bash
# Install all skills
npx skills add panlm/skills --skill '*'

# Install a specific skill
npx skills add panlm/skills --skill aws-bestpractice-research

# List available skills
npx skills add panlm/skills --list
```

## Available Skills

| Skill | Description |
|-------|-------------|
| [aws-bestpractice-research](./skills/aws-bestpractice-research/) | Research and compile comprehensive best-practice checklists for any AWS service. Produces categorized HA/DR/security checklist tables with source annotations. Optionally audits live AWS resources against the compiled checklist. |

## Prerequisites

Skills in this repo may depend on the following MCP servers and tools:

- [**aws-knowledge-mcp-server**](https://github.com/awslabs/mcp/tree/main/src/aws-knowledge-mcp-server) -- AWS documentation search and retrieval
- **AWS CLI** -- for optional live resource auditing

## Contributing

To add a new skill, create a directory under `skills/` with a `SKILL.md` file:

```
skills/
└── your-new-skill/
    ├── SKILL.md          # Required: skill definition with YAML frontmatter
    └── references/       # Optional: supporting templates and docs
```

The `SKILL.md` must include YAML frontmatter with `name` and `description`:

```yaml
---
name: your-new-skill
description: What this skill does and when to use it
---
```

## License

MIT
