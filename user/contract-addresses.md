# Contract addresses

Robinhood Chain mainnet — chain ID **4663**.

Explorer: [robinhoodchain.blockscout.com](https://robinhoodchain.blockscout.com)

## Policy: real tokens only

All production configs use **verified mainnet contracts** on Robinhood Chain (4663):

- **USDG** `0x5fc5360D0400a0Fd4f2af552ADD042D716F1d168` — deposit asset, prize token, stake-to-win asset
- **Morpho vault** `0xDF06045aBAE69d6e73a7F0197FED917032d22194` — HoodPot yield vault

Do **not** use `0x000…000` or mock tokens. `$HOOD` is added only after the real Virtuals launch — HoodPointsRegistry deploys with `HOOD_TOKEN=<real address>` only.

## Live contracts

| Contract | Address |
|----------|---------|
| USDG | `0x5fc5360D0400a0Fd4f2af552ADD042D716F1d168` |
| Morpho vault `hoodbet.fun` | `0xDF06045aBAE69d6e73a7F0197FED917032d22194` |
| Safe (owner + fees) | `0x5FF989aCB81e612fb54d2BDE9C6334B4C9a8f117` |
| TwabController | `0x534eb000af980efe5dc8f7b1b579c3c4baf87942` |
| PrizePool | `0x14e5004a757a85439fc379c8acd5b3b3cdf47344` |
| DrawManager | `0xd1c3d3b690c9a2033b0bea03ba0771847fd983eb` |
| PrizeVaultFactory | `0xa81b8281586115a228763a584734325beb71e5c2` |
| **HoodPot PrizeVault** | `0x318b89c2b407f091adcbc02854dd3f96e3470e17` |
| HoodRngBlockhash | `0x8B6EdfeCe14210eCb2A8D28F333D81621103Dd19` |
| HoodFeeHarvester | `0x7FB9C432e78101a6bB59e681458888acaA3db532` |
| Claimer | `0x71ec0971e8f8e35568a4bbe0fc118e6ca0ebe707` |

### Links

- [HoodPot PrizeVault](https://robinhoodchain.blockscout.com/address/0x318b89c2b407f091adcbc02854dd3f96e3470e17)
- [PrizePool](https://robinhoodchain.blockscout.com/address/0x14e5004a757a85439fc379c8acd5b3b3cdf47344)
- [Morpho vault](https://robinhoodchain.blockscout.com/address/0xDF06045aBAE69d6e73a7F0197FED917032d22194)
- [Safe on Safe UI](https://app.safe.global/home?safe=robinhood:0x5FF989aCB81e612fb54d2BDE9C6334B4C9a8f117)

## Pending

| Contract | Status |
|----------|--------|
| HoodPointsRegistry | Pending $HOOD token (Virtuals) |
| $HOOD token | Pending Virtuals launch |

## Network

| Parameter | Value |
|-----------|-------|
| RPC | `https://rpc.mainnet.chain.robinhood.com` |
| Chain ID | `4663` |
| Deploy start block | `8664950` |

## Config source

Canonical JSON config: [contracts/config/robinhood.json](https://github.com/hoodbet-fun/contracts/blob/main/config/robinhood.json)

This page is updated after each mainnet deployment.
