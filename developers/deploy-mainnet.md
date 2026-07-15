# HoodBet mainnet deploy runbook

**Status:** Core deploy complete on Robinhood Chain (4663). This page is the operator reference for what was deployed and how to extend it.

Safe owner: `0x5FF989aCB81e612fb54d2BDE9C6334B4C9a8f117`

## Live addresses

See [Contract addresses](../user/contract-addresses.md) for the canonical list.

| Contract | Address |
|----------|---------|
| HoodPot PrizeVault | `0x11da9bE66d20328c6eA16d52079890322fA90f24` |
| PrizePool | `0x14e5004a757a85439fc379c8acd5b3b3cdf47344` |
| HoodFeeHarvester | `0x3632Dd39B2717602fB4d7f79D001c3a51625159d` |
| $HOOD token | `0x3b4b9E8982449aa6712F0d13162252A4a871D43e` |
| HoodPointsRegistry | `0x7EBb6063C98e2D9faAD4C67A99d6A259f7810901` |

## HoodPointsRegistry (deployed)

```bash
cd contracts
export HOOD_TOKEN=0x3b4b9E8982449aa6712F0d13162252A4a871D43e
export SAFE_OWNER=0x5FF989aCB81e612fb54d2BDE9C6334B4C9a8f117
forge script script/DeployHoodPointsRegistry.s.sol \
  --rpc-url https://rpc.mainnet.chain.robinhood.com \
  --broadcast
```

Deploy tx block: `8787024`.

## Prize pool seed (optional)

Safe batches in [pt-deploy/safe](https://github.com/hoodbet-fun/hoodbet/tree/main/pt-deploy/safe):

| Batch | Amount |
|-------|--------|
| `hoodpot-seed-10-usdg.batch.json` | $10 USDG |
| `hoodpot-seed-100-usdg.batch.json` | $100 USDG |

Import in Safe Transaction Builder → sign → execute. Credits `PrizePool.contributePrizeTokens` for the HoodPot vault.

## Verify on Blockscout

https://robinhoodchain.blockscout.com

## Related

- [Deployment checklist](deployment.md)
- [Safe + Morpho wiring](safe-morpho-wiring.md)
- [Virtuals $HOOD](virtuals.md)
