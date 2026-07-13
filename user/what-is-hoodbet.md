# What is HoodBet?

HoodBet is an open protocol on **Robinhood Chain** that turns DeFi yield into a shared jackpot — without asking depositors to risk their principal.

## The idea

Traditional finance keeps most of the yield. Casinos are built so the house wins. HoodBet flips the model:

1. You **deposit USDG** into HoodPot.
2. Your **capital stays withdrawable** at any time.
3. **Yield and protocol fees** feed a prize pool.
4. **Daily draws** pick winners proportional to your time-weighted balance.

You don't bet against the house. You save together and win together.

## Built on proven primitives

| Layer | Role |
|-------|------|
| [Morpho](https://morpho.org/) | Curated ERC-4626 vault (`hoodbet.fun`) earns yield on USDG |
| [PoolTogether V5](https://dev.pooltogether.com/protocol/design/) | No-loss prize pool, TWAB odds, tiered draws |
| [Robinhood Chain](https://docs.robinhood.com/chain/) | EVM L2 (chain ID `4663`) |
| Safe multisig | Protocol governance and fee routing |

## HoodPot — the first product

**HoodPot** is HoodBet's launch product: a no-loss savings lottery.

- **Asset:** USDG (6 decimals)
- **Draw period:** every 24 hours
- **Prize funding:** Morpho curator fees (50% performance + ~5% APR management) + vault yield
- **Odds:** scale with deposit size and how long you stay (TWAB)

## $HOOD & HoodPoints

The **$HOOD** agent token (via [Virtuals.io](https://www.virtuals.io/)) unlocks tier perks — referral multipliers, badges, and early access to future products like HoodPredict.

## Transparency

- All deposits, draws, and claims are **on-chain**
- Contracts are **open source** on [GitHub](https://github.com/hoodbet-fun)
- Governance uses a **public Safe** — no hidden admin keys

## Next steps

- [Quick start](quick-start.md) — connect wallet and deposit
- [How HoodPot works](hoodpot-overview.md) — mechanics in detail
- [Risks & disclaimer](risks.md) — read before depositing
