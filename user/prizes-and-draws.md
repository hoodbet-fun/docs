# Prizes & daily draws

## Draw schedule

| Parameter | Value |
|-----------|-------|
| Draw period | 24 hours |
| Prize tiers | 4 |
| Grand prize frequency | ~every 91 draws |
| Prize token | USDG |

## How a draw works

1. **Draw period ends** after 24 hours
2. A **draw bot** starts the draw via `DrawManager`
3. An **RNG** produces a verifiable random number
4. **Winners are determined** per tier using TWAB-weighted odds
5. Winners **claim** USDG prizes (manually or via claim bot)

All steps are on-chain and auditable on [Blockscout](https://robinhoodchain.blockscout.com).

## Claiming prizes

1. Open [app.hoodbet.fun](https://app.hoodbet.fun) → **Prizes** tab
2. If you won, click **Claim prize**
3. Confirm the transaction — USDG is sent to your wallet

Permissionless **claim bots** can also claim on your behalf (incentivized by the protocol).

## Prize history

Public draw records are published in the [Draws log](../developers/draws.md) after launch.

A **HoodStats** dashboard (roadmap Q4 2026) will show live winners, odds, and jackpot history.

## Multiple tiers

PoolTogether V5 uses **tiered prizes**:

- Smaller tiers pay out more frequently
- The grand tier pays larger prizes less often

Your odds apply independently per tier based on your TWAB and the vault's contribution to the prize pool.

## I didn't win — did I lose money?

**No.** If you don't win a draw, your USDG deposit remains in HoodPot. Only yield and fees funded the prize — not your principal.

## Related

- [Odds & fairness](odds-and-fairness.md)
- [How HoodPot works](hoodpot-overview.md)
