# Connect — wallet sign-in on APECS Dev

Hub: `https://apecs.dev/connect` (also reached by the "Get Connected" header
button and the projects panel when signed out).

## Options

| Option | Chain | Status |
| --- | --- | --- |
| SIWE — Sign-In with Ethereum | Ethereum (EIP-4361) | **LIVE** |
| WizardConnect | Bitcoin Cash | Coming Soon (disabled card) |
| DashConnect | DashPay | Coming Soon (disabled card) |

## SIWE flow (what actually happens)

1. The site builds an EIP-4361 message (domain, address, statement, URI,
   version, chain ID, nonce, issued-at).
2. The wallet **signs** it. This is a message signature — **no transaction,
   no gas**. Never tell the user otherwise.
3. The signature is verified client-side (`ethers.verifyMessage`); the
   session lives in shared client state, so the header avatar, `/connect`
   and the projects panel update without a reload.
4. Sign-out is available from the header, the hub, or the projects panel.

No passwords, no email, no cookies-for-login.

## Language for humans

Say: "Connect your wallet" · "Sign the message — it's free, no transaction" ·
"You're connected as 0x1234…abcd".

Never say: session token, cookie, "approve the transaction", middleware,
composable.
