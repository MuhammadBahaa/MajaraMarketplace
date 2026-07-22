# Majara Nexus — Marketplace

[![skills.sh installs](https://skills.sh/b/MuhammadBahaa/majara-marketplace)](https://skills.sh/MuhammadBahaa/majara-marketplace)

Free, open AI-agent skills from **Majara Nexus**. Works with Claude Code and
every agent that supports the Agent Skills open standard (Codex, Cursor,
GitHub Copilot, Gemini CLI).

> This repository is **generated** from the private `MajaraCore` monorepo.
> Do not edit here — changes are overwritten on the next release.

## Plugins

| Plugin | What it does |
|--------|--------------|
| [`skill-craft`](plugins/skill-craft) | Review and authoring craft for agent skills, custom agents, and plugins — SkillCraft technical dimension-walk review with severity-mapped verdicts, and a guided walkthrough for reading and approving a skill in clear, organized parts. |

## Install

### Any agent — [skills.sh](https://skills.sh/MuhammadBahaa/majara-marketplace)
Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, and 70+ others:
```bash
npx skills add MuhammadBahaa/majara-marketplace
```

### Claude Code
```bash
claude plugin marketplace add MuhammadBahaa/majara-marketplace
# then, inside Claude Code:
/plugin install skill-craft@majara-marketplace
```

### Codex · Cursor · GitHub Copilot · Gemini CLI
These agents read skills from `~/.agents/skills` (user-wide) or
`<project>/.agents/skills` (per project). Copy the skill folders in:
```bash
git clone https://github.com/MuhammadBahaa/majara-marketplace
mkdir -p ~/.agents/skills
cp -r majara-marketplace/plugins/skill-craft/skills/* ~/.agents/skills/
```
- **Cursor / Copilot** also read `~/.claude/skills`, so a Claude install covers them too.
- **Gemini CLI** alternative: `gemini skills install <path-to-a-skill-folder>`.

Restart the agent (or run its skills-reload command) and the skills auto-activate by description.

## License

[MIT](LICENSE) © Majara Nexus
