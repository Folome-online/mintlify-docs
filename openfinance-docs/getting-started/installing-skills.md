# Installing Skills

Skills are SKILL.md-format playbooks that auto-load into your editor when relevant. They work across Claude Code, Cursor, Codex CLI, Gemini CLI, Windsurf, and most modern coding agents.

## One command (auto-detects your editor)

```bash
npx skills add openfinance-tech/skills -y
```

The `skills` CLI detects which editors you have installed and places the SKILL.md files in the right config directories (`.claude/skills/`, `.cursor/`, etc.). The `-y` flag skips the interactive prompt.

## Project-scoped install

Run the command from inside a project to install into that project only:

```bash
cd ~/code/my-trading-bot
npx skills add openfinance-tech/skills -y
```

This creates `.claude/skills/openfinance-tech/` (and equivalents for other agents) inside the project. Commit the folder to git so your team gets the same playbooks.

## Global install

```bash
npx skills add openfinance-tech/skills -y --global
```

Installs to `~/.claude/skills/` so the skills are available in every project.

## Verify

```bash
npx skills list
```

You should see `openfinance-tech` in the output. In Claude Code, type `/` and the skill commands will appear in the slash-command menu.

{% hint style="info" %}
Skills installed via `npx skills add` only apply to local editors. They do not apply to Claude.ai web or ChatGPT.
{% endhint %}
