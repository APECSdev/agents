# Sandbox — https://apecs.dev/sandbox

The playground for chain developers: 21 experiment cards on a data-driven
grid. Experiment routes are client-only (interactive; not prerendered).

Experiments (verified against `pages/sandbox.vue` in the apecs.dev repo):

| Experiment | Path | One-liner |
| --- | --- | --- |
| Address | `/sandbox/address` | Create addresses from user-defined scripts. |
| Android | `/android` | Live dashboard for a physically attached Android device, driven by the ADB workspace API. |
| Authentication | `/sandbox/auth` | User / identity verification using one or more protocols. |
| BitDB | `/sandbox/bitdb` | "Bitcoin is the most secure hard disk that will ever exist" — BitDB is its memory. |
| BitVM | `/sandbox/bitvm` | TBD. |
| CoinJoin | `/sandbox/coinjoin` | Coin-anonymity experiments (CashFusion and CashShuffle protocols). |
| CouchDB | `/sandbox/couchdb` | Various CouchDB functions. |
| Cryptography | `/sandbox/crypto` | Various cryptographic functions. |
| Decode | `/sandbox/decode` | Various decoding functions. |
| Elasticsearch | `/sandbox/elasticsearch` | Various Elasticsearch functions. |
| Events | `/sandbox/events` | Connect with events, server-side and beyond. |
| Hardware | `/sandbox/hardware` | Experiment with blockchain hardware devices. |
| Hashing | `/sandbox/hashing` | Calculate a hash (message digest) of data. |
| Libp2p | `/sandbox/libp2p` | libp2p, the open-source project from the IPFS community. |
| Messaging | `/sandbox/messaging` | Send/receive messages over on-chain protocols. |
| Nexa Daemon | `/sandbox/nexad` | Command a local `nexad` instance over JSON-RPC. |
| Query | `/sandbox/query` | Perform queries to the Bitcoin blockchain. |
| SLPDB | `/sandbox/slpdb` | SLP token system on Bitcoin Cash. |
| Transactions | `/sandbox/txs` | Experiments on Bitcoin Cash transactions. |
| Universal 2-Factor Authentication | `/sandbox/u2f` | Build and experiment with U2F. |
| Zero Knowledge | `/sandbox/zk` | Build and experiment with Zero Knowledge technologies. |

Caveats:

- `/android` data comes from the `apecs.dev/v1/*` Worker, which currently
  answers **401** to browsers (it expects an `x-apecs-key`; SIWE-based auth
  is the planned fix). The dashboard showing its error notice is expected.
- If a blurb above disagrees with the live card, the live card wins — the
  grid is generated from `pages/sandbox.vue` in the apecs.dev repo.
