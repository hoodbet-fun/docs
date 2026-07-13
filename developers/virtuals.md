# Virtuals.io — $HOOD token launch

## Overview

HoodBet agent token launches via [Virtuals Protocol](https://www.virtuals.io/) on Robinhood Chain.

## Steps

1. ~~Create HoodBet agent on Virtuals~~ — done
2. ~~Tokenize on chain 4663~~ — `0x3b4b9E8982449aa6712F0d13162252A4a871D43e`
3. ~~Record token address~~ — `contracts/config/robinhood.json`
4. ~~Deploy `HoodPointsRegistry`~~ — `0x7EBb6063C98e2D9faAD4C67A99d6A259f7810901`

Deploy script (reference):

```bash
export HOOD_TOKEN=0x3b4b9E8982449aa6712F0d13162252A4a871D43e
forge script script/DeployHoodPointsRegistry.s.sol --rpc-url $RH_RPC --broadcast
```

## Post-launch

- Subgraph indexes `$HOOD` transfers (see `services/subgraph/schema-hood.graphql`)
- App shows tier badge from `HoodPointsRegistry.getTier()`
- Optional: route agent trading fees to `VaultBooster` for jackpot

## References

- [Virtuals agent token docs](https://os.virtuals.io/agent-identity/token/overview)
- [Robinhood Chain × Virtuals](https://morpho.org/blog/robinhood-chooses-morpho-to-power-new-earn-product/)
