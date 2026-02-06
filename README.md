# Agent Skills

Skills are reusable capabilities for AI agents. Install them with a single command to enhance your agents with access to procedural knowledge. Distributed via [skills.sh](https://skills.sh).

## Available skills

| Skill | Description | Install |
|-------|-------------|---------|
| [vercel-sandbox](./vercel-sandbox) | Work with Vercel Sandbox ephemeral Linux microVMs | `npx skills add https://github.com/cesarecaoduro/agent-skills --skill vercel-sandbox` |

## Repository structure

```
<skill-name>/
  SKILL.md        # Skill definition (frontmatter + instructions)
  README.md       # Installation & usage guide
  references/     # Reference documentation
  scripts/        # Automation (e.g., doc updaters)
```

## Installing a skill

```bash
npx skills add https://github.com/cesarecaoduro/agent-skills --skill <skill-name>
```

## Adding a new skill

1. Create a directory for the skill
2. Add a `SKILL.md` with YAML frontmatter (`name`, `description`) and markdown instructions
3. Add a `README.md` with installation instructions
4. Add reference docs in `references/` and optional scripts in `scripts/`
5. Update this README to list the new skill

## Updating documentation

Each skill may include an update script to refresh reference files from upstream sources:

```bash
python3 <skill-name>/scripts/update_docs.py <skill-name>/references
```

## License

MIT
