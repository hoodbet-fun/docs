# $HOOD token

**$HOOD** is the HoodBet agent token launched via [Virtuals Protocol](https://www.virtuals.io/) on Robinhood Chain.

## Contract (live)

| Field | Value |
|-------|-------|
| **Address** | `0x3b4b9E8982449aa6712F0d13162252A4a871D43e` |
| **Name** | HoodBet.fun by Virtuals |
| **Symbol** | HOOD |
| **Decimals** | 18 |
| **Chain** | Robinhood Chain (4663) |

Explorer: [Blockscout](https://robinhoodchain.blockscout.com/token/0x3b4b9E8982449aa6712F0d13162252A4a871D43e)

Always verify this address on [Contract addresses](contract-addresses.md) or [hoodbet.fun](https://hoodbet.fun) before buying.

## What it does

Holding $HOOD unlocks **HoodPoints tiers** — on-chain tier status based on your wallet balance (read by `HoodPointsRegistry`).

Perks include:

- Profile **tier badge** in the dApp
- **Referral multiplier** on HoodCrew (coming soon)
- **Early access** to HoodPredict and other products

## How tiers work

`HoodPointsRegistry` (`0x7EBb…0901`) reads your $HOOD balance and assigns a tier:

| Tier | Min $HOOD |
|------|-----------|
| Scout | 0 |
| Hood | 10,000 |
| Legend | 100,000 |
| OG | 1,000,000 |

See [Tiers & perks](tiers-and-perks.md) for full details.

## How to get $HOOD

1. **Switch your wallet to Robinhood Chain** (chain ID `4663`).
2. **Acquire $HOOD** on Robinhood Chain — swap from ETH or USDG using a wallet/DEX that supports chain 4663.
3. **Verify the contract address** above before any swap.

Useful links:

- [Token on Blockscout](https://robinhoodchain.blockscout.com/token/0x3b4b9E8982449aa6712F0d13162252A4a871D43e) — holders, transfers, contract verification
- [Virtuals Protocol](https://www.virtuals.io/) — agent token platform

If no DEX route is listed yet, check [Telegram](https://t.me/+8KdjgSVzZr5hZjc0) for the latest swap links.

## Not required for HoodPot

You can use HoodPot **without** holding $HOOD. Scout tier (0 $HOOD) has full base access. $HOOD is for boosts and future products.

## Developer reference

Token launch steps: [Virtuals $HOOD launch](../developers/virtuals.md)
