# Majarrah Nexus — Marketplace

[![skills.sh installs](https://skills.sh/b/MuhammadBahaa/majarrah-marketplace)](https://skills.sh/MuhammadBahaa/majarrah-marketplace)

Free, open AI-agent skills from **Majarrah Nexus**. Works with Claude Code and
every agent that supports the Agent Skills open standard, including Codex,
Cursor, GitHub Copilot, and Gemini CLI.

> This repository is **generated** from the private `MajarrahCore` monorepo.
> Do not edit here — changes are overwritten on the next release.

## Plugins

| Plugin | What it does |
|--------|--------------|
| [`skill-craft`](plugins/skill-craft) | Technical review and guided walkthroughs for agent skills, slash commands, and plugins. |

## Install

### Codex

Add the GitHub marketplace:

```bash
codex plugin marketplace add MuhammadBahaa/majarrah-marketplace
```

Confirm that Codex can see the marketplace:

```bash
codex plugin marketplace list
```

List its available plugins:

```bash
codex plugin list
```

Install Skill Craft:

```bash
codex plugin add skill-craft@majarrah-marketplace
```

Run `codex plugin list` again and confirm that
`skill-craft@majarrah-marketplace` is `installed, enabled`. Start a
new Codex task to load `skill-craft-review` and `skill-walkthrough`.

### Any agent — [skills.sh](https://skills.sh/MuhammadBahaa/majarrah-marketplace)

Claude Code, Codex, Cursor, GitHub Copilot, Gemini CLI, and other compatible
agents:

```bash
npx skills add MuhammadBahaa/majarrah-marketplace
```

### Claude Code

```bash
claude plugin marketplace add MuhammadBahaa/majarrah-marketplace
# then, inside Claude Code:
/plugin install skill-craft@majarrah-marketplace
```

### Manual Agent Skills installation

Agents that read `~/.agents/skills` or a project `.agents/skills` directory can
copy the skill folders directly:

```bash
git clone https://github.com/MuhammadBahaa/majarrah-marketplace
mkdir -p ~/.agents/skills
cp -r majarrah-marketplace/plugins/skill-craft/skills/* ~/.agents/skills/
```

Restart the agent or use its skills-reload command after a manual installation.

## License

[MIT](LICENSE) © Majarrah Nexus
