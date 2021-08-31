# Developer Documention

## Adding New Reward Pools

### Creating the Staking Rewards contract
1. Submit a multisig transaction to call AddWhiteListedPool on the LiquidityManagerV2 contract (0x912b5D41656048Ef681eFa9D32488a3fFE397994) with the token pair (PGL) address as the input parameter and weight
2. After the function is called, a staking rewards contract will be created. Find the staking rewards contract address using the read function "stakes" on the LiquidityManagerV2 contract (0x912b5D41656048Ef681eFa9D32488a3fFE397994) with the token pair (PGL) address as the input parameter

### Updating the pangolin_api repo
1. Add the staking rewards contract address (check-summed) to the array in the src/constants.ts file
Example: https://github.com/pangolindex/pangolin-api/pull/35/files

### Updating the interface repo
1. Add the token information to the src/constants/index.ts file
2. Add the staking rewards contract information to the src/state/stake/hooks.ts file
Example: https://github.com/pangolindex/interface/pull/126/files

### Updating the tokenlists repo
1. Ensure that the new token is available in the defi.tokenlist.json file
Example: https://github.com/pangolindex/tokenlists/pull/91/files
