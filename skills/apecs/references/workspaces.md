# Workspaces — the 10 supported chains

Sorted alphabetically. Every Workspace ships a landing page plus live block and
transaction viewers. Routes are lowercase; capitalized URLs also resolve in SSR.

| Chain | Symbol | Path | Pages | Live skill |
| --- | --- | --- | --- | --- |
| Avalanche | AVAX | `/avax` | landing · blocks · txs | `https://apecs.dev/avax/SKILL.md` |
| Binance Smart Chain | BSC | `/bsc` | landing · blocks · txs | `https://apecs.dev/bsc/SKILL.md` |
| Bitcoin | BTC | `/btc` | landing · blocks · txs | `https://apecs.dev/btc/SKILL.md` |
| Bitcoin Cash | BCH | `/bch` | landing · blocks · txs | `https://apecs.dev/bch/SKILL.md` |
| Dash | DASH | `/dash` | landing · blocks · txs | `https://apecs.dev/dash/SKILL.md` |
| eCash | ECX | `/ecx` | landing · blocks · txs | `https://apecs.dev/ecx/SKILL.md` |
| Ethereum | ETH | `/eth` | landing · blocks · txs | `https://apecs.dev/eth/SKILL.md` |
| Monero | XMR | `/xmr` | landing · blocks · txs | `https://apecs.dev/xmr/SKILL.md` |
| Nexa | NEXA | `/nexa` | landing · blocks · txs | `https://apecs.dev/nexa/SKILL.md` |
| Tron | TRX | `/trx` | landing · blocks · txs | `https://apecs.dev/trx/SKILL.md` |

Index page for humans: `https://apecs.dev/workspaces`.

Chains REMOVED from the registry (pages may still exist on disk but are not
advertised): Filecoin, Polygon, Smart Bitcoin, THORChain. Do not present them
as supported Workspaces.

For chain-specific work, always fetch the live per-chain skill — it carries
the corrections (e.g. `eCash (ECX) ≠ XEC` on `/ecx/SKILL.md`).
