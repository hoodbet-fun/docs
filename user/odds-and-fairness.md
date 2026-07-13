# Odds & fairness

## How odds work (simplified)

Your chance of winning scales with:

1. **Your TWAB** — time-weighted average USDG balance in HoodPot
2. **Vault contribution** — how much yield your vault contributed to the prize pool
3. **Tier** — each prize tier has different odds and amounts

```
winning chance ∝ your TWAB × tier odds × vault portion
```

More deposit + longer duration = better odds. There is **no guarantee** of winning.

## TWAB explained

**TWAB (Time-Weighted Average Balance)** snapshots your balance over the draw period.

| Behavior | Effect on odds |
|----------|----------------|
| Deposit early in the period | Higher TWAB |
| Deposit right before draw ends | Lower TWAB |
| Withdraw mid-period | TWAB drops for remaining time |
| Hold steady | Maximum TWAB for your deposit size |

## Before the first draw (20 July 2026)

The dApp may show **Your odds —** until the draw period is active and TWAB is recorded on-chain. This is expected.

If you already deposited, your **position** (vault balance) is tracked. Once draws begin, TWAB will reflect how long you've been in the pool. A large share of total TVL → very high odds in early draws.

## Randomness

Draws use on-chain randomness via the protocol's RNG adapter.

| Phase | RNG | Notes |
|-------|-----|-------|
| MVP launch | Blockhash adapter | Acceptable for low TVL test phase |
| Production | Witnet / Chainlink VRF | Required before high TVL |

See [RNG decision](../developers/rng.md) for the full technical plan.

## Governance & trust

| Control | Holder |
|---------|--------|
| Protocol owner | Safe `0x5FF9…f117` (public multisig) |
| Morpho vault curator | Same Safe |
| Core prize params | Immutable after deploy |
| Draw & claim bots | Permissionless |

No single operator can pick winners — outcomes are determined by smart contracts and the RNG.

## Verifiability

Anyone can verify:

- Deposit balances via `TwabController`
- Draw results via `PrizePool` events
- Random number via `DrawManager` + RNG contract
- Fee routing via `HoodFeeHarvester` and Morpho vault events

## Open source

All HoodBet contracts are on [GitHub](https://github.com/hoodbet-fun/contracts). Audit checklist: [Security](../developers/security.md).

## Related

- [Risks & disclaimer](risks.md)
- [Glossary](glossary.md)
