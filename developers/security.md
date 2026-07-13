# HoodBet — Security & Launch Checklist

## HoodFeeHarvester audit notes

| Item | Status |
|------|--------|
| Only owner sets `prizeVault` | OK — `onlyOwner` |
| Asset must match prize token | OK — constructor check |
| `harvest()` permissionless | By design — anyone can trigger |
| Morpho share redemption | Trust Morpho vault — use curated vault |
| Reentrancy | Uses OZ SafeERC20 + standard ERC4626 redeem |

## HoodRngBlockhash

- **MVP only** — not production-grade randomness
- Upgrade to Witnet / Chainlink VRF before high TVL ([RNG](rng.md))

## HoodPointsRegistry

- Tier thresholds owner-adjustable (Safe)
- Reads `$HOOD` balance — trust token contract at `0x3b4b…D43e`

## Pre-launch checklist

- [x] PrizePool deployed with intended params (24h draws, 4 tiers, USDG)
- [x] Integration tests pass (`forge test`)
- [x] Contracts verified on Blockscout
- [x] Safe Morpho fee wiring complete
- [x] Subgraph deployed on Goldsky
- [x] Bots deployed (draw / claim / liquidation)
- [x] Disclaimer on landing
- [ ] RNG tested with 10+ consecutive draws on testnet
- [ ] Bot dry-run 7 days at scale
- [ ] Formal third-party audit
- [ ] First public draw documented ([draws.md](draws.md))

## Launch sequence (completed)

1. Deploy PT core + verify
2. Deploy PrizeVault + liquidation pair
3. Deploy HoodFeeHarvester
4. Safe wiring + Morpho fees + collateral caps
5. Subgraph + bots live
6. Virtuals `$HOOD` + HoodPointsRegistry
7. Landing + app live
8. Prize pool seed ($10 USDG)
9. **First draw** — scheduled 20 July 2026

## First draw documentation

Record in [draws.md](draws.md):

- Draw ID, block, random number hash
- Winners, prize amounts
- Explorer links
