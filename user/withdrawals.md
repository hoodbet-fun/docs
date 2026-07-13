# Withdraw anytime

HoodPot is **no-loss** — your USDG principal remains in the vault until you withdraw.

## Steps

1. Open [app.hoodbet.fun](https://app.hoodbet.fun)
2. Connect the wallet that deposited
3. Go to the **Withdraw** tab
4. Enter an amount or use the suggested instant max
5. Confirm the transaction

## What you receive

You receive **USDG** back, proportional to your vault shares at the current share price (principal + any accrued yield not yet liquidated to the prize pool).

## Morpho instant liquidity (important)

HoodPot deposits into a **Morpho lending vault**. Most USDG is deployed to borrowers — only a small **idle** slice is available for instant withdrawal.

| What you see | Meaning |
|--------------|---------|
| **Your position** | Full vault balance (always yours on paper) |
| **Instant max** | What Morpho can pay out right now |
| `maxWithdraw = 0` on-chain | Common — Morpho-backed vaults often report 0 even when small withdrawals work |

If a larger withdraw fails with `TransferReverted`:

1. Try a **smaller amount** (e.g. $0.001)
2. Wait for borrowers to repay and free liquidity
3. Your full position is not lost — it unlocks over time

This is normal ERC-4626 + lending market behaviour, not a HoodPot bug.

## Impact on odds

Withdrawing reduces your balance immediately. Your **TWAB** for the current draw period reflects the lower balance for the remaining time.

If you plan to stay for multiple draws, avoid withdrawing and re-depositing frequently — it lowers your average balance.

## Unclaimed prizes

Withdrawing does **not** forfeit prizes you already won. Claim prizes separately on the **Prizes** tab before or after withdrawal.

## Related

- [Deposits](deposits.md)
- [Prizes & draws](prizes-and-draws.md)
- [FAQ](faq.md)
