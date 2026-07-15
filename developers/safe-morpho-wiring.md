# Safe + Morpho vault wiring

**Status:** HoodFeeHarvester v2 deployed — **Safe batch pending** (`hoodpot-harvester-v2.batch.json`).

Safe: https://app.safe.global/home?safe=robinhood:0x5FF989aCB81e612fb54d2BDE9C6334B4C9a8f117

Morpho vault: `0xDF06045aBAE69d6e73a7F0197FED917032d22194`  
HoodPot PrizeVault: `0x11da9bE66d20328c6eA16d52079890322fA90f24`  
HoodFeeHarvester (v2): `0x3632Dd39B2717602fB4d7f79D001c3a51625159d`  
HoodFeeHarvester (deprecated): `0x7FB9C432e78101a6bB59e681458888acaA3db532`

## Batches used

Import JSON from [pt-deploy/safe](https://github.com/hoodbet-fun/hoodbet/tree/main/pt-deploy/safe):

| Batch | Purpose |
|-------|---------|
| `hoodpot-harvester-v2.batch.json` | **Pending** — wire v2 harvester + Morpho fee recipients |
| `hoodpot-wiring.batch.json` | Liquidation pair + `harvester.setPrizeVault` (v1) |
| `hoodpot-morpho-fees.batch.json` | Morpho `submit` + execute fee recipients (v1) |
| `morpho-collateral-caps.batch.json` | Collateral caps (syrupUSDG, USDe, spUSDG) |
| `hoodpot-seed-10-usdg.batch.json` | Optional prize pool seed |

### Why `submit` + `execute`?

Morpho Vault V2 curator functions require `submit(bytes)` before execution. Direct calls revert with `DataNotTimelocked()` (Safe shows **GS013**). Timelock is **0** on this vault, so submit and execute can run in the same batch.

## Checklist

- [x] Liquidation pair wired to PrizeVault
- [x] Collateral caps set for syrupUSDG, USDe, spUSDG
- [ ] `hoodpot-harvester-v2.batch.json` executed on Safe
- [ ] `performanceFeeRecipient` = HoodFeeHarvester v2
- [ ] `managementFeeRecipient` = HoodFeeHarvester v2
- [ ] `harvester.prizeVault()` = HoodPot PrizeVault (v2)

## Ongoing

- `harvester.harvest()` — permissionless; liquidation-bot calls it every 30s
- TPDA liquidation — runs when `maxAmountOut > 0` (needs vault yield above buffer + bot USDG for swap)
