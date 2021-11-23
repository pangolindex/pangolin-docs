---
description: This will guide you through adding new pools onto Pangolin
---

# 🎱 Adding new pools

## Adding New Reward Pools

### Creating the Staking Rewards contract

1. Submit a multisig transaction (0xA4cB6e1971Ed8A1F76d9e8d50A5FC56DFA5cc1e6) to call AddWhiteListedPool on the LiquidityManagerV2 contract (0x912b5D41656048Ef681eFa9D32488a3fFE397994) with the token pair (PGL) address as the input parameter and weight. To do this you'll need to log onto the[ Multisig wallet UI](https://multisig.pangolin.exchange).
2. After the function is called, a staking rewards contract will be created. Find the staking rewards contract address using the read function "stakes" on the LiquidityManagerV2 contract (0x912b5D41656048Ef681eFa9D32488a3fFE397994) with the token pair (PGL) address as the input parameter

### Updating the [pangolin\_api repo](https://github.com/pangolindex/pangolin-api)

1.  Add the staking rewards contract address (check-summed) to the array in the src/constants.ts file

    Example: [https://github.com/pangolindex/pangolin-api/pull/35/files](https://github.com/pangolindex/pangolin-api/pull/35/files)

### Updating the[ interface repo](https://github.com/pangolindex/interface)

1. Add the token information to the src/constants/index.ts file
2.  Add the staking rewards contract information to the src/state/stake/hooks.ts file

    Example: [https://github.com/pangolindex/interface/pull/126/files](https://github.com/pangolindex/interface/pull/126/files)

### Updating the [tokenlists repo](https://github.com/pangolindex/tokenlists)

1.  Ensure that the new token is available in the defi.tokenlist.json file

    Example: [https://github.com/pangolindex/tokenlists/pull/91/files](https://github.com/pangolindex/tokenlists/pull/91/files)
