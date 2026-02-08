# On-Chain Staking Rewards

This repository provides a robust and gas-optimized staking mechanism. Users can stake their tokens into the pool and accumulate rewards dynamically. It is designed for projects looking to incentivize long-term token holding and liquidity.

### Features
* **Time-Based Rewards:** Accrue rewards every second based on the staking duration.
* **Emergency Withdraw:** A safety function for users to pull their principal in case of contract migration (optional/configurable).
* **Owner Management:** Tools for the project owner to fund the reward pool and adjust parameters.

### Logic Flow
1. **Stake:** User approves the contract and calls `stake(amount)`.
2. **Earn:** The contract calculates rewards based on `(amount * rate * time)`.
3. **Claim:** User calls `getReward()` to mint or transfer accumulated earnings.
4. **Withdraw:** User removes their original principal and any remaining rewards.
