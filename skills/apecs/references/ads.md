# Ads auction — https://apecs.dev/ads

- **10 identical slots**, sold by a **uniform-price auction**: the 10 highest
  bidders each win a slot and ALL pay the lowest winning (10th-highest) bid.
- **Floor: $1.00 per slot per epoch** — lower bids are rejected.
- **Ties break by earliest submission.**
- Bids settle **only** through the on-chain escrow contract (ERC-20 `approve`
  + `AdAuction.deposit`, ethers 6). NOWPayments was **rejected** for the
  auction.
- Until the contracts finish testnet deployment and the auction address is
  configured site-side, the page renders "bidding opens soon" plus clearly
  labelled mock slots, and the client can make **no** chain write
  (fail-closed by design).
- Live leaderboard endpoint: `https://apecs.dev/v1/ads/epoch` (apecs-api
  Worker; browsers currently get 401 — it expects an `x-apecs-key` the site
  does not send yet).

Do not fabricate slot prices, current bids, or epoch dates — none are wired
to a live feed yet.
