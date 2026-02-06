# Agent Skills Repository

This is a skills repository. Skills are reusable capabilities for AI agents — install them with a single command to enhance your agents with access to procedural knowledge. Distributed via [skills.sh](https://skills.sh).

## Repository structure

```
<skill-name>/
  SKILL.md            # Skill definition (frontmatter + instructions)
  README.md           # Installation & usage guide
  references/         # Reference documentation files
  scripts/            # Automation scripts (e.g., doc updaters)
README.md             # Repo-level overview
CLAUDE.md             # This file
```

Each skill is a self-contained directory. The `SKILL.md` file is the entry point — it uses YAML frontmatter (`name`, `description`) and markdown body to define when and how the skill should be used.

## Current skills

- **vercel-sandbox** — Work with Vercel Sandbox ephemeral Linux microVMs

## Conventions

- No build system, no tests, no linting — this is a documentation-driven repo.
- Reference docs in `references/` are fetched from upstream sources and should not be hand-edited.
- Use the `scripts/update_docs.py` pattern to keep reference docs in sync with upstream.
- Generated/temporary files (`.fetched.md`, `_update_meta.json`) are gitignored.

## Updating documentation

Each skill may include an `update_docs.py` script. Run it to refresh reference files:

```bash
python3 vercel-sandbox/scripts/update_docs.py vercel-sandbox/references
```

The script fetches upstream docs, computes diffs, and overwrites local reference files.

## Installing a skill

```bash
npx skills add https://github.com/cesarecaoduro/agent-skills --skill <skill-name>
```

## Adding a new skill

1. Create a new directory: `<skill-name>/`
2. Add a `SKILL.md` with frontmatter (`name`, `description`) and usage instructions
3. Add a `README.md` with installation instructions (`npx skills add ... --skill <skill-name>`)
4. Add `references/` for any reference documentation
5. Optionally add `scripts/` for automation
6. Update the root `README.md` to list the new skill
