# Workspaces — the 10 supported chains

Sorted alphabetically. Every Workspace ships a landing page plus live block and
transaction viewers — except RISCy, which is in development (landing only).
Routes are lowercase; capitalized URLs also resolve in SSR.

| Chain | Symbol | Path | Pages | Live skill |
| --- | --- | --- | --- | --- |
| Akash | AKT | `/akt` | landing · blocks · txs | `https://apecs.dev/akt/SKILL.md` |
| Avalanche | AVAX | `/avax` | landing · blocks · txs | `https://apecs.dev/avax/SKILL.md` |
| Bitcoin | BTC | `/btc` | landing · blocks · txs | `https://apecs.dev/btc/SKILL.md` |
| Bitcoin Cash | BCH | `/bch` | landing · blocks · txs | `https://apecs.dev/bch/SKILL.md` |
| Dash | DASH | `/dash` | landing · blocks · txs | `https://apecs.dev/dash/SKILL.md` |
| eCash | ECX | `/ecx` | landing · blocks · txs | `https://apecs.dev/ecx/SKILL.md` |
| Flux | FLUX | `/flux` | landing · blocks · txs | `https://apecs.dev/flux/SKILL.md` |
| Monero | XMR | `/xmr` | landing · blocks · txs | `https://apecs.dev/xmr/SKILL.md` |
| Nexa | NEXA | `/nexa` | landing · blocks · txs | `https://apecs.dev/nexa/SKILL.md` |
| RISCy | — | `/riscy` | landing only (in development) | `https://apecs.dev/riscy/SKILL.md` |

Index page for humans: `https://apecs.dev/workspaces`.

The platform focuses on **UTXO-based networks** (Avalanche is included for its
Primary Network / P-Chain). **RISCy** (https://riscy.network) is a UTXO-based
network in development by APECS Dev — verified facts only, no preview stats.

Chains REMOVED from the registry (pages may still exist on disk but are not
advertised): Binance Smart Chain, Ethereum, Tron (2026-10-23 UTXO-focus
removal); Filecoin, Polygon, Smart Bitcoin, THORChain (earlier). Do not present
them as supported Workspaces.

For chain-specific work, always fetch the live per-chain skill — it carries
the corrections (e.g. `eCash (ECX) ≠ XEC` on `/ecx/SKILL.md`).
