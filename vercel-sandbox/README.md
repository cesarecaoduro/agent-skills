# Vercel Sandbox Skill

Work with [Vercel Sandbox](https://vercel.com/docs/vercel-sandbox) — ephemeral Linux microVMs for running untrusted code, AI agent output, and developer experimentation on Vercel.

## Install

```bash
npx skills add https://github.com/cesarecaoduro/agent-skills --skill vercel-sandbox
```

Or install globally with auto-confirm:

```bash
npx skills add https://github.com/cesarecaoduro/agent-skills --skill vercel-sandbox -g -y
```

## What this skill provides

Once installed, Claude Code will know how to:

- **Create and manage sandboxes** — spin up isolated microVMs via the TypeScript/Python SDK or Vercel CLI
- **Run commands** — execute code in `node24`, `node22`, or `python3.13` runtimes
- **Snapshot and restore** — save sandbox state for fast restarts
- **Authenticate** — set up OIDC tokens or access tokens for sandbox access
- **Navigate pricing and limits** — understand plan-specific resource limits and timeouts

## When it triggers

The skill activates when you mention:

- Vercel Sandbox, `@vercel/sandbox`, sandbox microVMs
- Running code in isolated environments on Vercel
- Creating, managing, or snapshotting sandboxes
- Sandbox pricing, resource limits, or authentication
- `vercel sandbox` CLI commands
- Updating sandbox documentation

## Reference documentation

| File | Covers |
|------|--------|
| [quickstart.md](references/quickstart.md) | Getting started, prerequisites, authentication |
| [sdk-reference.md](references/sdk-reference.md) | TypeScript/Python SDK classes and methods |
| [cli-reference.md](references/cli-reference.md) | `vercel sandbox` CLI commands |
| [pricing-and-specs.md](references/pricing-and-specs.md) | Plans, limits, system specs |

## Updating docs

Refresh reference files from Vercel's official documentation:

```bash
python3 vercel-sandbox/scripts/update_docs.py vercel-sandbox/references
```

## Links

- [Vercel Sandbox docs](https://vercel.com/docs/vercel-sandbox)
- [Skills.sh](https://skills.sh)
