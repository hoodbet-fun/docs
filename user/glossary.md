# Glossary

| Term | Definition |
|------|------------|
| **HoodBet** | The protocol brand — prize-linked savings and future prediction products on Robinhood Chain |
| **HoodPot** | The no-loss savings lottery product (PoolTogether V5 + Morpho) |
| **USDG** | Stablecoin deposited into HoodPot (6 decimals) |
| **TWAB** | Time-Weighted Average Balance — measures deposit duration × amount for draw odds |
| **PrizeVault** | ERC-4626 wrapper that tracks TWAB and forwards assets to Morpho |
| **PrizePool** | PoolTogether contract holding prize liquidity and running tiered draws |
| **Draw** | A 24-hour cycle ending in an on-chain random winner selection |
| **Tier** | Prize level (4 tiers + grand prize cadence) |
| **Morpho** | DeFi lending protocol; curates the `hoodbet.fun` vault |
| **HoodFeeHarvester** | HoodBet contract that redeems Morpho fee shares into the prize pool |
| **$HOOD** | HoodBet agent token on Virtuals.io |
| **HoodPoints** | Tier system (Scout / Hood / Legend / OG) based on $HOOD balance |
| **Safe** | Gnosis Safe multisig controlling protocol governance |
| **RNG** | Random Number Generator used for draws |
| **Liquidation bot** | Permissionless bot that auctions vault yield into the prize pool |
| **Claim bot** | Permissionless bot that claims prizes for winners |
| **Robinhood Chain** | EVM L2, chain ID 4663 |
| **Virtuals** | Protocol for launching agent tokens ($HOOD) |
