---
name: apecs
description: "Build on or use APECS Dev (apecs.dev) — a permissionless, multi-chain platform for P2P electronic cash Builders. Covers the 10 chain Workspaces (Avalanche, Binance Smart Chain, Bitcoin, Bitcoin Cash, Dash, eCash, Ethereum, Monero, Nexa, Tron), the Sandbox experiments (Address, Authentication, BitDB, BitVM, CoinJoin, CouchDB, Cryptography, Decode, Elasticsearch, Events, Hardware, Hashing, Libp2p, Messaging, Nexa Daemon, Query, SLPDB, Transactions, U2F, Zero Knowledge, Android ADB), the /connect wallet hub (SIWE / EIP-4361 live), the APECS MCP server, the ads auction and the crypto-only sponsor program. Triggers: APECS, apecs.dev, any of the 10 chain names in an APECS context, SIWE connect, BCH/ECX workspace, ads auction, sponsor APECS."
metadata:
  author: APECS Dev
  version: "1.0.0"
  homepage: "https://apecs.dev"
  repository: "https://github.com/APECSdev/agents"
---

# APECS Dev

Permissionless multi-chain platform for P2P electronic cash Builders — "Casually Building Crypto". Site: `https://apecs.dev`. Publisher is **APECS Dev** everywhere except the Bitcoin Cash workspace page ("Bitcoin Please").

Routes by **task → touchpoint**:

| Task | Touchpoint | Guide |
| --- | --- | --- |
| Any chain-specific work | Fetch `https://apecs.dev/<chain>/SKILL.md` (live, current) | [references/workspaces.md](references/workspaces.md) |
| Connect a wallet / sign in | `/connect` hub — SIWE (EIP-4361) live | [references/connect.md](references/connect.md) |
| Use APECS from an MCP client | Bundled connector `https://apecs.dev/mcp` (`.mcp.json`) | [references/mcp.md](references/mcp.md) |
| Run an experiment / prototype | Sandbox (21 experiments) | [references/sandbox.md](references/sandbox.md) |
| Advertise on APECS | Uniform-price ads auction | [references/ads.md](references/ads.md) |
| Support the platform | Crypto-only sponsorship (BCH, XMR) | [references/sponsors.md](references/sponsors.md) |
| State facts about APECS | Read the corrections first | [references/safeguards.md](references/safeguards.md) |

## Live skill files (single source of truth)

The site serves the current published copy of every skill — fetch, don't recall:

- Root: `https://apecs.dev/SKILL.md`
- Per chain: `https://apecs.dev/<chain>/SKILL.md` (`avax bsc btc bch dash ecx eth xmr nexa trx`)
- Machine-readable index: `https://apecs.dev/.well-known/agent-skills/index.json`

A web fetch tool may summarize and drop details — fetch the raw Markdown when instructions matter.

## Non-negotiable facts (short list — full version in safeguards.md)

- APECS **eCash (ECX)** is the ecash.com drivechain fork (BIP300/301), **NOT** Bitcoin-ABC's XEC.
- **No donations** exist on APECS — monetization is the ads auction + sponsors.
- `explorer.bitcoin.com` is retired; never link it. Blockchair is the explorer of record.
- `apecs.dev/admin` is 404 — the Administration Center is a separate app at `admin.apecs.dev`.
- SIWE is a **signature, not a transaction** — never tell the user gas is required.
