# Draw history

Public log of HoodPot draws on Robinhood Chain mainnet.

## Launch status

| Field | Value |
|-------|-------|
| Prize pool | **Shut down** — `isShutdown()` is `true` |
| `shutdownAt` | `1789682400` (17 September 2026, 22:00 UTC) |
| Prize pool seeded | $10 USDG (Safe contribution) |
| `getLastAwardedDrawId` | `0` (no draw was ever awarded) |
| `drawTimeout` | `60` draws |
| First draw opened | **20 July 2026** (`firstDrawOpensAt` = `1784498400`, 19 July 2026, 22:00 UTC) |
| Draw period | 24 hours |

PT V5 shuts a prize pool down when `drawTimeout` draws pass without an award: `shutdownAt` is `drawClosesAt(lastAwardedDrawId + drawTimeout)`, which is `drawClosesAt(60)` here. `awardDraw` reverts once the pool is shut down, and because the last awarded draw can then never advance, the shutdown is permanent. `HoodRngBlockhash.nextRequestId()` is still `1`, so no randomness was ever requested for a draw.

### HoodPot PrizeVault after the shutdown

| Field | Value (block `96055611`) |
|-------|-------|
| `totalDebt` (owed to depositors) | 227.680515 USDG |
| `totalAssets` | 226.126366 USDG |
| `maxDeposit` | `0` — deposits are closed |
| `previewRedeem(1 hpUSDG)` | 0.993173 USDG |

`totalAssets` is below `totalDebt`, so the PrizeVault pays redemptions pro rata: each hpUSDG currently redeems for about 0.9932 USDG.

## Template (use after each draw)

### Draw #N — YYYY-MM-DD

| Field | Value |
|-------|-------|
| Draw ID | |
| Block | |
| Random number | |
| Prize pool balance | |
| Winners | |
| Explorer | |

---

*No draw was awarded before the prize pool shut down on 17 September 2026.*
