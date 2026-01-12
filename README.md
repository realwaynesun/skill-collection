# Skill Collection

A curated collection of Claude Code skills for extending Claude's capabilities.

## What are Skills?

Skills are markdown files that provide Claude Code with specialized knowledge, workflows, or tool integrations. They can be invoked using `/skill-name` in Claude Code.

## Structure

```
skill-collection/
├── skills/
│   ├── coding/          # Development and programming skills
│   ├── productivity/    # Workflow and automation skills
│   ├── documentation/   # Writing and docs skills
│   ├── data/            # Data analysis and processing skills
│   └── ui/              # UI and frontend development skills
└── examples/            # Example skills and templates
```

## Installation

Claude Code requires skills to be placed in a specific structure: a folder named after the skill containing a `SKILL.md` file. Skills in this repo use descriptive filenames for readability, so you'll need to rename them when installing.

**To install a skill:**

```bash
# 1. Create a folder with your desired skill name
mkdir -p ~/.claude/skills/vibe-coding

# 2. Copy the skill file and rename to SKILL.md
cp skills/coding/vibe-coding-workflow.md ~/.claude/skills/vibe-coding/SKILL.md
```

**Then invoke in Claude Code:**
```
/vibe-coding
```

> **Note:** The folder name becomes the command name. You can name it whatever you prefer.

## Adding a Skill

Each skill should be a `.md` file with:
- Clear description of what it does
- Instructions for Claude to follow
- Any required context or examples

## Skills

### Coding

- **[vibe-coding-workflow](skills/coding/vibe-coding-workflow.md)** - A structured workflow for building products from scratch with Claude Code. Covers planning, MVP execution, validation, UI polish, and deployment. *By waynesun, inspired by [@turingou](https://x.com/turingou)*

### Productivity
<!-- Add your productivity skills here -->

### Documentation
<!-- Add your documentation skills here -->

### Data
<!-- Add your data skills here -->

### UI

- **[ui-skills](skills/ui/ui-skills.md)** - Opinionated constraints for building better interfaces with agents. Covers stack choices, components, interaction patterns, animation, typography, layout, performance, and design guidelines. *From [ui-skills.com](https://www.ui-skills.com/)*

## Contributing

Feel free to submit PRs with new skills or improvements to existing ones.

## License

MIT
