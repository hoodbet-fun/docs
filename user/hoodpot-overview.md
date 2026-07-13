# How HoodPot works

HoodPot combines **Morpho vault yield** with **PoolTogether V5** prize mechanics.

## No-loss savings

In a normal lottery you pay for tickets and lose your stake. In HoodPot:

- Your **USDG principal is always yours**
- You can **withdraw anytime** (subject to vault liquidity)
- Only **yield and fees** fund prizes

If you never win, you still have your deposit. If you win, you keep your deposit **and** receive a prize.

## Where prizes come from

Two funding streams feed the jackpot:

| Source | Description |
|--------|-------------|
| **Morpho curator fees** | 50% performance fee + ~5% APR management fee on the `hoodbet.fun` vault |
| **Vault yield** | Residual share-price growth liquidated into the prize pool |

Fees are routed through `HoodFeeHarvester` into the PoolTogether prize pool after deployment.

## Time-weighted average balance (TWAB)

Your odds are not based on a snapshot. The protocol tracks your **time-weighted average balance (TWAB)**:

- Larger deposits → more tickets (proportionally)
- Longer time in the pool → higher TWAB → better odds

This rewards loyal depositors over flash deposits right before a draw.

## Daily draws

- **Draw period:** 24 hours (`86400` seconds)
- **Tiers:** 4 prize tiers (including a grand prize every ~91 draws)
- **Prize token:** USDG

A permissionless draw bot triggers each draw after the period ends. Randomness is provided by an on-chain RNG (see [Odds & fairness](odds-and-fairness.md)).

## The flow

```
Deposit USDG → PrizeVault → Morpho vault (yield)
                    ↓
              TWAB tracked
                    ↓
         Yield + fees → Prize pool
                    ↓
            Daily draw → Winners claim
```

## Morpho vault (live today)

The underlying Morpho vault is already deployed:

| Field | Value |
|-------|-------|
| Name | `hoodbet.fun` |
| Address | `0xDF06045aBAE69d6e73a7F0197FED917032d22194` |
| Asset | USDG |

The full HoodPot experience (PrizeVault wrapper + draws) activates once PoolTogether V5 core contracts are deployed. See [Contract addresses](contract-addresses.md).

## Related

- [Deposits](deposits.md)
- [Prizes & draws](prizes-and-draws.md)
- [Architecture](../developers/architecture.md) — technical deep dive
