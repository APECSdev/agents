# APECS MCP server

Endpoint: `https://apecs.dev/mcp` — Model Context Protocol over streamable
HTTP (POST JSON-RPC 2.0, `application/json` responses; no batching, no SSE).
One URL, both audiences: POST speaks JSON-RPC; GET serves the human landing
page (`pages/mcp.vue` in the apecs.dev repo).

Source: `server/routes/mcp.post.ts` in the `APECSdev/apecs.dev` repo (Nitro
server route, ships with the SSR deployment). This repo bundles it for MCP
clients via the root [`.mcp.json`](../../../.mcp.json). (History: began as a
Cloudflare Worker at `mcp.apecs.dev` in `APECSdev/mcp`; the subdomain was
decommissioned 2026-10-23.)

## Client registration

Claude Code / Cowork and Cursor pick the server up automatically from this
plugin's `.mcp.json`. Manual/generic clients:

```json
{
  "mcpServers": {
    "apecs": { "type": "http", "url": "https://apecs.dev/mcp" }
  }
}
```

## Tools exposed

| Tool | Purpose |
| --- | --- |
| `list_skills` | List every published APECS skill (proxies the site's live index). |
| `get_skill` | Fetch one skill's Markdown by name (`apecs`, `apecs-bch`, …). |
| `get_connection_guide` | The `/connect` hub explained (SIWE live; WizardConnect / DashConnect coming soon). |
| `get_ads_info` | Ads auction + sponsor program facts. |

## Smoke test

```bash
curl -s -X POST https://apecs.dev/mcp \
  -H 'content-type: application/json' \
  -d '{"jsonrpc":"2.0","id":1,"method":"initialize","params":{}}'
# expect: result.serverInfo.name == "apecs-mcp"
```

No authentication is required today. The endpoint is read-only against the
public site; it holds no keys and cannot write to any chain or account.
