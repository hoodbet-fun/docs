# Deposit USDG

## Before you deposit

1. Wallet on **Robinhood Chain** (4663) — [setup guide](wallet-setup.md)
2. **USDG** balance in your wallet
3. **ETH** for gas
4. Open [app.hoodbet.fun](https://app.hoodbet.fun)

## Steps

1. **Connect wallet** in the top-right of the dApp
2. Go to the **Deposit** tab
3. Enter the USDG amount
4. **Approve** USDG spending (first time only)
5. **Confirm deposit** — this mints PrizeVault shares tracked by TWAB

## What happens on-chain

```
Your wallet ──USDG──► PrizeVault ──USDG──► Morpho vault (hoodbet.fun)
                           │
                           └── TWAB balance recorded for draws
```

Your HoodPot position is represented as vault shares. Share price increases as yield accrues.

## No lock-up

There is **no minimum lock period**. You can withdraw at any time. However, withdrawing before a draw reduces your TWAB and therefore your odds for that period.

## Tips

- Deposit earlier in the draw period to maximize TWAB for the next draw
- Larger deposits increase your proportional chance (not a guarantee)
- Verify the transaction on [Blockscout](https://robinhoodchain.blockscout.com)

## Deployment status

If the dApp shows **"PrizeVault pending deploy"**, the PoolTogether PrizeVault wrapper is not yet live. The Morpho vault accepts curator configuration but the full no-loss lottery path requires core PT deployment. Track progress in [Contract addresses](contract-addresses.md).

## Related

- [Withdrawals](withdrawals.md)
- [Odds & fairness](odds-and-fairness.md)
