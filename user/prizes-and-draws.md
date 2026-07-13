# Prizes & daily draws

## Draw schedule

| Parameter | Value |
|-----------|-------|
| Draw period | 24 hours |
| Prize tiers | 4 |
| Grand prize frequency | ~every 91 draws |
| Prize token | USDG |
| First draw opens | **20 July 2026** |
| Current prize pool | **$10 USDG** (Safe seed + grows from yield) |

## How a draw works

1. **Draw period ends** after 24 hours
2. A **draw bot** starts the draw via `DrawManager`
3. An **RNG** produces a verifiable random number
4. **Winners are determined** per tier using TWAB-weighted odds
5. Winners **claim** USDG prizes (manually or via claim bot)

All steps are on-chain and auditable on [Blockscout](https://robinhoodchain.blockscout.com).

## How the prize pool grows

| Source | Mechanism |
|--------|-----------|
| **Vault yield** | Yield above the 0.5 USDG buffer → TPDA liquidation → prize pool |
| **Morpho fees** | 50% performance + 5% management → `HoodFeeHarvester` → prize pool |
| **Governance seed** | Optional Safe `contributePrizeTokens` (e.g. $10 launch seed) |

With low TVL, organic growth is slow. More deposits → more yield → faster jackpot growth.

## Claiming prizes

1. Open [app.hoodbet.fun](https://app.hoodbet.fun) → **Prizes** tab
2. If you won, click **Claim prize**
3. Confirm the transaction — USDG is sent to your wallet

The dApp shows **To claim** with your unclaimed total. Permissionless **claim bots** can also claim on your behalf.

## Prize history

Public draw records: [Draws log](../developers/draws.md)

## Multiple tiers

HoodPot uses **tiered prizes**:

- Smaller tiers pay out more frequently
- The grand tier pays larger prizes less often

Your odds apply independently per tier based on your TWAB and the vault's contribution to the prize pool.

## I didn't win — did I lose money?

**No.** If you don't win a draw, your USDG deposit remains in HoodPot. Only yield and fees funded the prize — not your principal.

## Related

- [Odds & fairness](odds-and-fairness.md)
- [How HoodPot works](hoodpot-overview.md)
