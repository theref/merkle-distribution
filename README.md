# T Merkle Distributor

Solidity contract for Threshold rewards' distribution.

In Cumulative Merkle Drop contract each new token distribution replaces previous one and should
contain cumulative balances of all the participants. Cumulative claimed amount is used as
invalidation for every participant.

## Structure

This is a Hardhat project:

- `contracts`: Source code for contract
- `test`: Contract tests
- `scripts`: Hardhat scripts:
  - `gen_merkle_dist.js`: generate new Merkle distribution
  - `verify_proof.js`: verify Merkle proof
  - `example_run_claim.js`: example about how to claim tokens using the contract

## Examples

- `example_stake_list_<n>.json`: List of stakes and its data. This JSON is the input of
  `gen_merkle_dist.js`, which will return the Merkle Distribution for provided stakes.
- `example_dist_generated_<n>.json`: All the data of the generated Merkle distribution. Includes the
  total amount of tokens to be claimed by stakers, the Merkle root, and the info of each stake. It's
  the output of `gen_merkle_dist.js`.
- `example_proof_generated_<n>.json`: This is an example of the data that will be provided to each
  staker. Includes the Merkle root, the token's amount to be claimed and the Merkle proof. It's the
  output of `gen_merkle_dist.js`.

## Installation

```bash
npm install
```

## Run scripts

```bash
npx hardhat run scripts/<script.js>
```

## Run tests

```bash
npx hardhat test
```
