# Contract addresses

Robinhood Chain mainnet — chain ID **4663**.

Explorer: [robinhoodchain.blockscout.com](https://robinhoodchain.blockscout.com)

## Policy: real tokens only

All production configs use **verified mainnet contracts** on Robinhood Chain (4663):

- **USDG** `0x5fc5360D0400a0Fd4f2af552ADD042D716F1d168` — deposit asset, prize token, stake-to-win asset
- **Morpho vault** `0xDF06045aBAE69d6e73a7F0197FED917032d22194` — HoodPot yield vault

Do **not** use `0x000…000` or mock tokens. `$HOOD` is added only after the real Virtuals launch — HoodPointsRegistry deploys with `HOOD_TOKEN=<real address>` only.

| Contract | Address | Status |
|----------|---------|--------|
| USDG | `0x5fc5360D0400a0Fd4f2af552ADD042D716F1d168` | Live |
| Morpho vault `hoodbet.fun` | `0xDF06045aBAE69d6e73a7F0197FED917032d22194` | Live (~$1 TVL) |
| Safe (owner + fees) | `0x5FF989aCB81e612fb54d2BDE9C6334B4C9a8f117` | Live |

### Links

- [Morpho vault on Blockscout](https://robinhoodchain.blockscout.com/address/0xDF06045aBAE69d6e73a7F0197FED917032d22194)
- [Safe on Safe UI](https://app.safe.global/home?safe=robinhood:0x5FF989aCB81e612fb54d2BDE9C6334B4C9a8f117)

## Pending deployment

| Contract | Address | Status |
|----------|---------|--------|
| TwabController | — | Pending |
| PrizePool | — | Pending |
| DrawManager | — | Pending |
| PrizeVault | — | Pending |
| HoodRngBlockhash | `0x8B6EdfeCe14210eCb2A8D28F333D81621103Dd19` | Live |
| HoodFeeHarvester | — | Pending PrizePool |
| HoodPointsRegistry | — | Pending $HOOD token |
| $HOOD token | — | Pending Virtuals launch |

Track deploy progress: [Deployment checklist](../developers/deployment.md)

## Network

| Parameter | Value |
|-----------|-------|
| RPC | `https://rpc.mainnet.chain.robinhood.com` |
| Chain ID | `4663` |

## Config source

Canonical JSON config: [contracts/config/robinhood.json](https://github.com/hoodbet-fun/contracts/blob/main/config/robinhood.json)

This page is updated after each mainnet deployment.
