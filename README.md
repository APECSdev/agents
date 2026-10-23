# APECS Dev Agent Skills

The agent skill for [APECS Dev](https://apecs.dev) — a permissionless, multi-chain platform for P2P electronic cash Builders. Enables AI agents to discover and work with the 10 chain Workspaces (Avalanche, Binance Smart Chain, Bitcoin, Bitcoin Cash, Dash, eCash, Ethereum, Monero, Nexa, Tron), the Sandbox experiments, the `/connect` SIWE wallet hub, the APECS MCP server, the ads auction and the crypto-only sponsor program. Agent Skills spec compliant. Works with Claude Code, Cursor, `npx skills`.

## Status

| Item | Status |
|------|--------|
| Repo | `APECSdev/agents` on GitHub |
| Skill | `apecs` v1.0 — task → touchpoint routing with live skill files served by the site |
| Plugin | `.claude-plugin/marketplace.json` + manifest; includes the APECS MCP server via root [`.mcp.json`](.mcp.json) (Claude Code / Cowork / Cursor) |
| Spec | [Agent Skills](https://agentskills.io/specification) compliant |
| Live skills | Site serves the current copy: [`/SKILL.md`](https://apecs.dev/SKILL.md), per-chain `/<chain>/SKILL.md`, index at [`/.well-known/agent-skills/index.json`](https://apecs.dev/.well-known/agent-skills/index.json) |

## Installation

### Claude Code / Cowork (plugin: skill + MCP)

```bash
/plugin marketplace add APECSdev/agents
/plugin install apecs@apecs-skills
/reload-plugins
```

Registers the **apecs** skill and the APECS MCP connector ([`.mcp.json`](.mcp.json)). Pin: `APECSdev/agents@v1.0.0`.

Update:

```bash
/plugin marketplace update apecs-skills
/plugin update apecs@apecs-skills
/reload-plugins
```

### Cursor (plugin: skill + MCP)

**Customize** → add `APECSdev/agents` → install **apecs**. Gets the skill and the MCP connector in [`.mcp.json`](.mcp.json).

### skills CLI

```bash
npx skills add APECSdev/agents
```

### Direct MCP (any client)

```json
{
  "mcpServers": {
    "apecs": { "type": "http", "url": "https://mcp.apecs.dev/mcp" }
  }
}
```

Human setup guide: [https://apecs.dev/mcp](https://apecs.dev/mcp).

## What's inside

| Path | Purpose |
| --- | --- |
| `skills/apecs/SKILL.md` | Main skill — routing table + non-negotiable facts |
| `skills/apecs/references/workspaces.md` | The 10 chain Workspaces and their live skill URLs |
| `skills/apecs/references/connect.md` | The `/connect` hub and the SIWE (EIP-4361) flow |
| `skills/apecs/references/mcp.md` | MCP endpoint, tools, client registration, smoke test |
| `skills/apecs/references/sandbox.md` | The 21 Sandbox experiments |
| `skills/apecs/references/ads.md` | The uniform-price ads auction |
| `skills/apecs/references/sponsors.md` | The crypto-only sponsor program (no donations) |
| `skills/apecs/references/safeguards.md` | Facts training data gets wrong (ECX ≠ XEC, retired explorers, ...) |

## License

MIT — see [LICENSE](LICENSE).
