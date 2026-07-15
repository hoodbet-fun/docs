# Contract addresses

Robinhood Chain mainnet — chain ID **4663**.

Explorer: [robinhoodchain.blockscout.com](https://robinhoodchain.blockscout.com)

## Policy: real tokens only

All production configs use **verified mainnet contracts** on Robinhood Chain (4663):

- **USDG** `0x5fc5360D0400a0Fd4f2af552ADD042D716F1d168` — deposit asset, prize token, stake-to-win asset
- **Morpho vault** `0xDF06045aBAE69d6e73a7F0197FED917032d22194` — HoodPot yield vault
- **$HOOD** `0x3b4b9E8982449aa6712F0d13162252A4a871D43e` — HoodBet agent token (Virtuals)

Do **not** use `0x000…000` or mock tokens.

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
| **HoodPot PrizeVault** | `0x11da9bE66d20328c6eA16d52079890322fA90f24` |
| HoodRngBlockhash | `0x8B6EdfeCe14210eCb2A8D28F333D81621103Dd19` |
| HoodFeeHarvester | `0x3632Dd39B2717602fB4d7f79D001c3a51625159d` |
| Claimer | `0x71ec0971e8f8e35568a4bbe0fc118e6ca0ebe707` |
| **$HOOD token** | `0x3b4b9E8982449aa6712F0d13162252A4a871D43e` |
| **HoodPointsRegistry** | `0x7EBb6063C98e2D9faAD4C67A99d6A259f7810901` |

### Live protocol params

| Parameter | Value |
|-----------|-------|
| Prize pool balance | **$10 USDG** (Safe seed; grows from yield + fees) |
| `firstDrawOpensAt` | **20 July 2026** |
| Draw period | 24 hours |
| PrizeVault `yieldBuffer` | 0.5 USDG |
| Completed draws | `0` |

### Deprecated

| Contract | Address | Note |
|----------|---------|------|
| HoodPot PrizeVault (old) | `0x318b89c2b407f091adcbc02854dd3f96e3470e17` | `yieldBuffer = 0` — do not use |
| HoodFeeHarvester (old) | `0x7FB9C432e78101a6bB59e681458888acaA3db532` | Broken PT V5 contribute path — do not use |

### Subgraph (Goldsky)

Public GraphQL endpoint:

```
https://api.goldsky.com/api/public/project_cmmaz8bs32rjv01u29b8y8vuf/subgraphs/hoodbet/1.0.0/gn
```

Indexes from block `8664950`. Dashboard: [app.goldsky.com](https://app.goldsky.com).

### Links

- [HoodPot PrizeVault](https://robinhoodchain.blockscout.com/address/0x11da9bE66d20328c6eA16d52079890322fA90f24)
- [PrizePool](https://robinhoodchain.blockscout.com/address/0x14e5004a757a85439fc379c8acd5b3b3cdf47344)
- [$HOOD token](https://robinhoodchain.blockscout.com/token/0x3b4b9E8982449aa6712F0d13162252A4a871D43e)
- [HoodPointsRegistry](https://robinhoodchain.blockscout.com/address/0x7EBb6063C98e2D9faAD4C67A99d6A259f7810901)
- [Morpho vault](https://robinhoodchain.blockscout.com/address/0xDF06045aBAE69d6e73a7F0197FED917032d22194)
- [Safe on Safe UI](https://app.safe.global/home?safe=robinhood:0x5FF989aCB81e612fb54d2BDE9C6334B4C9a8f117)

## Network

| Parameter | Value |
|-----------|-------|
| RPC | `https://rpc.mainnet.chain.robinhood.com` |
| Chain ID | `4663` |
| Deploy start block | `8664950` |
| HoodPointsRegistry deploy | `8787024` |

## Config source

Canonical JSON config: [contracts/config/robinhood.json](https://github.com/hoodbet-fun/contracts/blob/main/config/robinhood.json)

This page is updated after each mainnet deployment.
