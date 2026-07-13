# hoodbet.fun deployment checklist

## Current on-chain state (mainnet)

| Item | Status |
|------|--------|
| Morpho vault `hoodbet.fun` | Live |
| USDG asset | Live |
| Safe as owner + fee recipient | Live |
| HoodPot PrizeVault | Live — `0x318b89…0e17` |
| Prize pool + DrawManager | Live |
| HoodFeeHarvester | Live — wired to PrizeVault |
| HoodRngBlockhash | Live (MVP — upgrade before high TVL) |
| Morpho fees → HoodFeeHarvester | **Pending Safe action** |
| HoodPointsRegistry | Pending $HOOD token |
| Subgraph Goldsky | Scaffold ready |
| Bots | Scaffold ready |
| Formal security audit | **Not completed** |

## Deploy flow (completed + remaining)

1. ~~Prize pool core~~ — done
2. ~~HoodPot PrizeVault + HoodFeeHarvester~~ — done
3. [Safe + Morpho wiring](safe-morpho-wiring.md) — **next**
4. [Virtuals $HOOD](virtuals.md) — $HOOD token
5. [Subgraph README](https://github.com/hoodbet-fun/subgraph) — Goldsky
6. [Security checklist](security.md) — audit + RNG upgrade before scale

## HoodBet custom deploy

```bash
cd contracts
export SAFE_OWNER=0x5FF989aCB81e612fb54d2BDE9C6334B4C9a8f117
export PRIZE_POOL=0x14e5004a757a85439fc379c8acd5b3b3cdf47344
# forge script or cast send --create (chain 4663)
```

## Frontend deploy

| URL | Directory |
|-----|-------------|
| hoodbet.fun | `landing/` |
| app.hoodbet.fun | `app/` |
