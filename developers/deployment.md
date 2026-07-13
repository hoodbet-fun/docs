# hoodbet.fun deployment checklist

Last updated after mainnet launch (July 2026).

## Current on-chain state (mainnet)

| Item | Status |
|------|--------|
| Morpho vault `hoodbet.fun` | Live |
| USDG asset | Live |
| Safe as owner + fee recipient | Live |
| HoodPot PrizeVault | Live — `0x11da9b…0f24` (yield buffer 0.5 USDG) |
| Prize pool + DrawManager | Live |
| Prize pool balance | **$10 USDG** (Safe seed) |
| HoodFeeHarvester | Live — wired to PrizeVault |
| Liquidation pair + router | Live |
| Morpho fee recipients | Done (harvester) |
| Morpho collateral caps | Done (syrupUSDG, USDe, spUSDG) |
| HoodRngBlockhash | Live (MVP — upgrade before high TVL) |
| $HOOD token (Virtuals) | Live — `0x3b4b…D43e` |
| HoodPointsRegistry | Live — `0x7EBb…0901` |
| Subgraph (Goldsky) | Live |
| Bots (draw / claim / liquidation) | Deployed — Oracle VPS |
| Formal security audit | **Not completed** |

Deprecated vault `0x318b…0e17` (`yieldBuffer = 0`) — do not use.

## Deploy flow

| Step | Status |
|------|--------|
| Prize pool core (PT V5) | Done |
| HoodPot PrizeVault + HoodFeeHarvester | Done |
| Safe wiring (liquidation + harvester) | Done |
| Morpho fee recipients | Done |
| Morpho collateral caps | Done |
| Virtuals $HOOD | Done |
| HoodPointsRegistry | Done |
| Prize pool seed ($10) | Done |
| Subgraph Goldsky | Done |
| Bots on VPS | Done |
| RNG upgrade (VRF) | Before high TVL |
| Formal audit | Before scale |

## Operations

| Bot | Role | Notes |
|-----|------|-------|
| `hoodbet-draw` | Hourly cron — start/finish draws | Active after 20 Jul 2026 |
| `hoodbet-claim` | Scan winners, `claimPrizes` | Idle until first draw |
| `hoodbet-liquidation` | Harvest Morpho fees + TPDA swaps | Harvest runs always; swap needs USDG in bot wallet |

Repo: [github.com/hoodbet-fun/bots](https://github.com/hoodbet-fun/bots)

## Frontend deploy

| URL | Repo |
|-----|------|
| [hoodbet.fun](https://hoodbet.fun) | `landing/` |
| [app.hoodbet.fun](https://app.hoodbet.fun) | `app/` |

## Related

- [Safe + Morpho wiring](safe-morpho-wiring.md)
- [Virtuals $HOOD](virtuals.md)
- [Security checklist](security.md)
- [Draw log](draws.md)
