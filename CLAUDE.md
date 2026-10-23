# APECS Skills — Agent Guide

Instructions:

- Be semantically dense and token efficient. Prefer concise, information-rich responses; avoid filler, repetition, and unnecessary elaboration.
- When editing, never mention the previous version or the changes you made. All contents must be authoritative and up to date.
- Never guess a fact about APECS. The site is the source of truth — fetch `https://apecs.dev/SKILL.md` (root), `https://apecs.dev/<chain>/SKILL.md` (per chain) or `https://apecs.dev/.well-known/agent-skills/index.json` (index) before stating anything that could have changed.
- Avoid creating new sections; update existing knowledge instead.

This repository is a monorepo of agent skills for APECS Dev, packaged as a **Claude Code / Cowork plugin marketplace**. Skills live in `skills/` and are distributed through the plugin system shared by Claude Code, Cowork and Cursor.

## Installing the Plugin

### Claude Code

```shell
/plugin marketplace add APECSdev/agents
/plugin install apecs@apecs-skills
/reload-plugins
```

Bundled **APECS MCP** ([`.mcp.json`](.mcp.json), `https://apecs.dev/mcp`). Pin: `APECSdev/agents@v1.0.0`.

### Claude Cowork / Cursor

Customize → Plugins → add `APECSdev/agents` → install **apecs**.

### Local Testing

```shell
claude --plugin-dir ./
```

`/reload-plugins` after edits. `claude plugin validate .` before publish.

## Repository Structure

```
.claude-plugin/
  plugin.json          # Plugin manifest (name, version, author)
  marketplace.json     # Marketplace catalog listing the plugin
.cursor-plugin/
  plugin.json          # Cursor manifest (skills + .mcp.json)
.mcp.json              # MCP server definition (APECS HTTP MCP)
assets/                # (reserved)
skills/
  apecs/
    SKILL.md           # Main skill (routing + safeguards)
    references/        # Deep-dive docs per touchpoint
```

## Hard rules for edits

1. **Pin every version exactly** — GitHub Actions by commit SHA, npm deps without `^`/`~`.
2. Keep `skills/apecs/references/*` in sync with the live site. When the
   apecs.dev repo changes a fact (chains, auction rules, connect options),
   update the reference file in the same change.
3. The **site** serves the canonical published copy of the skills; this repo
   is the installable package. Never let them contradict.
4. Facts live in `references/safeguards.md` — extend that list rather than
   scattering corrections across files.
