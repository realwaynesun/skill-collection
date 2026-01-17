# Skill Collection

A curated collection of Claude Code skills for extending Claude's capabilities.

## What are Skills?

Skills are markdown files that provide Claude Code with specialized knowledge, workflows, or tool integrations. They follow the standard Claude Code skill format with YAML frontmatter.

## Structure

```
skill-collection/
└── skills/
    ├── vibe-coding/
    │   └── SKILL.md      # Vibe coding workflow
    ├── ui-skills/
    │   └── SKILL.md      # UI development constraints
    └── skill-template/
        └── SKILL.md      # Template for creating new skills
```

## Installation

Copy any skill folder to your Claude Code skills directory:

```bash
# Global installation (all projects)
cp -r skills/vibe-coding ~/.claude/skills/

# Project-specific installation
cp -r skills/ui-skills /path/to/project/.claude/skills/
```

**Then invoke in Claude Code:**
```
/vibe-coding
/ui-skills
```

## Skills

### vibe-coding

A structured workflow for building products from scratch with Claude Code. Covers:
- Phase 1: Initial Planning (`/plan` mode)
- Phase 2: MVP Execution
- Phase 3: MVP Validation
- Phase 4: UI/UX Polish
- Phase 5: Deployment

*By waynesun, inspired by [@turingou](https://x.com/turingou)*

### ui-skills

Opinionated constraints for building better interfaces with agents. Covers:
- Stack choices (Tailwind, motion/react, etc.)
- Component primitives (Base UI, React Aria, Radix)
- Interaction patterns
- Animation guidelines
- Typography & Layout
- Performance & Design rules

*From [ui-skills.com](https://www.ui-skills.com/)*

## Creating a New Skill

1. Create a folder: `skills/<skill-name>/`
2. Add a `SKILL.md` file with YAML frontmatter:

```yaml
---
name: skill-name
description: Brief description of what this skill does
author: your-name
---

# Skill Title

Your skill instructions here...
```

See [skills/skill-template/SKILL.md](skills/skill-template/SKILL.md) for a full template.

## YAML Frontmatter Fields

| Field | Required | Description |
|-------|----------|-------------|
| `name` | Yes | Skill identifier (lowercase-kebab-case) |
| `description` | Yes | Brief description for Claude |
| `author` | No | Creator's name |
| `source` | No | Original source URL if adapted |
| `inspired_by` | No | Credit for inspiration |

## Contributing

Feel free to submit PRs with new skills or improvements to existing ones.

## License

MIT
