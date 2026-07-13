# FAQ

## General

### Is HoodBet a casino?

No. HoodPot is **prize-linked savings** — you don't buy losing tickets. Your USDG principal stays withdrawable. Only yield and protocol fees fund prizes.

### Can I lose my deposit?

Under normal operation, **no** — that's the HoodPot no-loss model. Smart contract, market, and vault risks still apply. Read [Risks & disclaimer](risks.md).

### What chain is HoodBet on?

**Robinhood Chain mainnet** — chain ID `4663`.

### Is HoodBet affiliated with Robinhood the brokerage?

HoodBet is an independent open-source protocol built on Robinhood Chain. It is not an official Robinhood product.

## HoodPot

### What token do I deposit?

**USDG** — 6 decimal stablecoin on Robinhood Chain.

### How often are draws?

Every **24 hours**. The first draw window opens **20 July 2026**.

### Why does the app show "—" for my odds?

Before the first draw period is active, TWAB may not be available yet. Your **vault position** is still tracked — odds will appear once draws begin. See [Odds & fairness](odds-and-fairness.md).

### Why is the prize pool only $10?

The pool was **seeded with $10 USDG** from governance at launch. It grows organically from Morpho yield and curator fees as TVL increases. More deposits → faster jackpot growth.

### Why can't I withdraw my full balance?

HoodPot uses a Morpho lending vault. Most USDG is lent out — only a small **instant** amount may be withdrawable immediately. Your full position remains yours. See [Withdrawals](withdrawals.md).

### Do I need to claim manually?

You can claim on the dApp **Prizes** tab, or a permissionless claim bot may claim for you.

### Why can't I deposit?

Check that your wallet is on Robinhood Chain (4663), you have USDG and ETH for gas, and you're using [app.hoodbet.fun](https://app.hoodbet.fun). See [Contract addresses](contract-addresses.md) if you need to verify HoodPot is live.

## $HOOD

### Do I need $HOOD to use HoodPot?

No. Scout tier (0 $HOOD) works for HoodPot.

### Where can I buy $HOOD?

On **Robinhood Chain (4663)**. Official contract:

`0x3b4b9E8982449aa6712F0d13162252A4a871D43e`

Swap from ETH or USDG using a wallet that supports chain 4663. Verify the address on [Contract addresses](contract-addresses.md) or [Blockscout](https://robinhoodchain.blockscout.com/token/0x3b4b9E8982449aa6712F0d13162252A4a871D43e) before buying.

You do **not** need $HOOD to deposit in HoodPot — tiers are optional boosts.

### How do I see my tier?

Connect on [app.hoodbet.fun](https://app.hoodbet.fun). The dApp reads `HoodPointsRegistry` and shows your tier badge (Scout / Hood / Legend / OG) from your wallet $HOOD balance.

## Technical

### Where are the contracts?

[Contract addresses](contract-addresses.md) and [GitHub](https://github.com/hoodbet-fun/contracts).

### Is the code open source?

Yes — [github.com/hoodbet-fun](https://github.com/hoodbet-fun).

### Who controls the protocol?

A public **Safe multisig** (`0x5FF9…f117`) for governance and fee routing. Core prize parameters are immutable after deploy.

## Support

Community: [HoodBet.fun Official on Telegram](https://t.me/+8KdjgSVzZr5hZjc0).

For bugs, open an issue on the relevant [GitHub repo](https://github.com/hoodbet-fun).
