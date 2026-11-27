# Minimal Soroban Follow-ups

## Soroban/Proxy: Implementation Contract Interface Validation

- [x] Define the required implementation entry point or interface contract.
- [x] Validate the candidate implementation before storing it during initialization and upgrade.
- [x] Keep the current implementation unchanged when validation fails.
- [x] Add one test covering rejection of an incompatible implementation.

## Soroban/YieldFarming: Auto-Compounding Strategy Vaults

- [x] Add vault share supply and per-user share state.
- [x] Add deposit, withdraw, and compound operations with authorization and accounting checks.
- [x] Reinvest harvested rewards into the configured AMM and mint/burn vault shares proportionally.
- [x] Add one test covering a deposit, compound, and withdrawal round trip.

## Soroban/Batch: Operation Gas Usage Estimation

- [x] Define a read-only estimator input and result for the existing batch operation types.
- [x] Return a deterministic estimate for each operation and the complete batch without executing calls.
- [x] Reject unsupported operations or arithmetic overflow explicitly.
- [x] Add one test proving estimates do not mutate the nonce or execute a target call.

## Soroban/Utils: Standardize Storage TTL Extension

- [x] Provide shared helpers for instance, persistent, and temporary storage TTL extension.
- [x] Use one documented threshold and extension policy for all three storage classes.
- [x] Replace direct contract-level `extend_ttl` calls with the shared helpers.
- [x] Add focused tests for each helper and preserve key-specific TTL behavior.
