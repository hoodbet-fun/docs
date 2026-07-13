# How HoodPot works

HoodPot combines **Morpho vault yield** with **on-chain prize pool** mechanics.

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

Fees are routed through `HoodFeeHarvester` into the HoodPot prize pool.

## Time-weighted average balance (TWAB)

Your odds are not based on a snapshot. The protocol tracks your **time-weighted average balance (TWAB)**:

- Larger deposits → more tickets (proportionally)
- Longer time in the pool → higher TWAB → better odds

This rewards loyal depositors over flash deposits right before a draw.

## Daily draws

- **Draw period:** 24 hours (`86400` seconds)
- **Tiers:** 4 prize tiers (including a grand prize every ~91 draws)
- **Prize token:** USDG
- **Current prize pool:** $10 USDG (launch seed + organic growth)
- **First draw:** 20 July 2026

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

## Live contracts

| Field | Value |
|-------|-------|
| HoodPot PrizeVault | `0x11da9bE66d20328c6eA16d52079890322fA90f24` |
| Morpho vault `hoodbet.fun` | `0xDF06045aBAE69d6e73a7F0197FED917032d22194` |
| Asset | USDG |

See [Contract addresses](contract-addresses.md) for the full list.

## Related

- [Deposits](deposits.md)
- [Prizes & draws](prizes-and-draws.md)
- [Architecture](../developers/architecture.md) — technical deep dive
