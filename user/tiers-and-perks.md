# Tiers & perks

HoodPoints tiers are based on your **$HOOD token balance** on Robinhood Chain.

## Tier table

| Tier | Min $HOOD | Referral multiplier | Perks |
|------|-----------|---------------------|-------|
| **Scout** | 0 | 1.00× | Base HoodPot access |
| **Hood** | 10,000 | 1.25× | Tier badge + referral boost |
| **Legend** | 100,000 | 1.50× | HoodPredict beta access |
| **OG** | 1,000,000 | 2.00× | Governance + max referral boost |

Multipliers apply to **HoodCrew** referral rewards (roadmap Q4 2026).

## Badge in the dApp

When connected, [app.hoodbet.fun](https://app.hoodbet.fun) shows your tier badge next to your wallet address (e.g. `Hood`, `Legend`).

## How tier is calculated

- Read from `HoodPointsRegistry.getTierName(yourAddress)`
- Based on **current** $HOOD balance — not staked or locked
- Tier updates when your balance crosses a threshold

## Thresholds (on-chain)

Configured on-chain in `HoodPointsRegistry` (`0x7EBb6063C98e2D9faAD4C67A99d6A259f7810901`):

```
Scout:  0
Hood:   10,000 × 10^18
Legend: 100,000 × 10^18
OG:     1,000,000 × 10^18
```

## Future perks

| Product | Tier benefit |
|---------|--------------|
| HoodCrew | Referral XP multiplier |
| HoodPredict | Legend+ beta access |
| HoodArena | OG creator fee discounts |
| Governance | OG voting weight (planned) |

## Related

- [$HOOD token](hood-token.md)
- [Product roadmap](roadmap.md)
