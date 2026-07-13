# Risks & disclaimer

{% hint style="warning" %}
**HoodBet is experimental DeFi.** This is not financial advice. Only deposit what you can afford to lose considering smart contract and market risks.
{% endhint %}

## No-loss ≠ no risk

PoolTogether's "no-loss" model means your **principal is not intentionally spent on prizes**. It does **not** eliminate all risk.

## Smart contract risk

- Bugs in HoodBet, PoolTogether, Morpho, or dependency contracts could cause loss
- Immutable misconfiguration at deploy cannot be reversed
- Contracts are open source but **not formally audited** for mainnet launch

## Market & vault risk

- Morpho vaults lend USDG to markets — **bad debt** or illiquidity could affect withdrawals
- Curated vaults reduce but do not eliminate this risk

## RNG risk (MVP)

The initial RNG may use a **blockhash adapter** suitable only for **low TVL**. Production requires upgrade to Witnet or Chainlink VRF before significant deposits.

## Regulatory risk

Prize-linked savings and prediction products may be regulated differently in your jurisdiction. You are responsible for compliance.

## Token risk ($HOOD)

$HOOD is a speculative agent token. Price can go to zero. Tier perks do not guarantee returns.

## Operational risk

- Bots must run draws, liquidations, and claims — downtime delays prizes
- Subgraph or frontend outages do not stop the protocol but affect UX

## No guarantees

- Past draws do not predict future wins
- Odds do not guarantee winnings
- Roadmap dates are targets, not commitments

## Experimental notice

HoodBet.fun is an experimental protocol. The team makes no warranties. Use at your own risk.

## Security resources

- [Security checklist](../developers/security.md)
- [Architecture](../developers/architecture.md)
- Report issues: [github.com/hoodbet-fun](https://github.com/hoodbet-fun)
