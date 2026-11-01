# DELIRO — AuxPoW Merged Mining Design

Version: 0.1
Status: Draft — Not Implemented

## 1. Purpose

Deliro plans to support SHA-256d Auxiliary Proof of Work (AuxPoW).

The goal is to allow compatible mining pools to mine Deliro alongside another SHA-256d blockchain, such as Bitcoin, without requiring a separate full mining operation.

## 2. Important Security Principle

Merged mining does not automatically give Deliro the security or hash rate of Bitcoin.

A mining pool must explicitly support Deliro, construct valid auxiliary mining data, and submit valid AuxPoW proofs to Deliro nodes.

## 3. Mining Algorithm

Proposed algorithm:

- SHA-256d
- Auxiliary Proof of Work
- Parent-chain proof verification
- Independent Deliro block validation

## 4. Parent Chain

The parent chain is expected to use SHA-256d Proof of Work.

The exact parent-chain compatibility rules must be specified before implementation.

## 5. Auxiliary Block Commitment

The parent block's coinbase transaction must contain a valid commitment to the Deliro auxiliary block.

The commitment format, chain identifier, tree structure, and proof rules must be formally specified.

## 6. AuxPoW Validation

Every Deliro full node must independently verify:

- The parent block header
- The parent-chain Proof of Work
- The coinbase transaction
- The auxiliary commitment
- The Merkle branch
- The auxiliary block hash
- The required difficulty target
- The absence of invalid or reused proofs

Invalid AuxPoW data must cause the block to be rejected.

## 7. Chain Identifier

Deliro must use a unique chain identifier.

The identifier must be selected and tested before launch to reduce the risk of conflicts with other merged-mining chains.

## 8. Mining Pool Requirements

Mining pools must explicitly implement Deliro support.

They must:

- Construct valid auxiliary mining jobs
- Provide correct mining templates
- Submit valid AuxPoW proofs
- Follow Deliro's consensus rules
- Distribute mining rewards transparently

## 9. Difficulty Adjustment

Deliro requires its own difficulty adjustment rules.

The exact algorithm must be specified, implemented, and tested against timestamp manipulation, sudden hash-rate changes, and irregular block production.

## 10. Reward Rules

AuxPoW does not change the Deliro monetary policy.

Block rewards must follow the exact Deliro subsidy schedule.

No parent-chain miner may create additional DEL outside valid consensus rewards.

## 11. Testing Requirements

Before launch, implementation must pass:

- Valid AuxPoW proof tests
- Invalid proof rejection tests
- Merkle branch tests
- Chain identifier tests
- Parent block validation tests
- Difficulty adjustment tests
- Mining pool integration tests
- Adversarial security tests

## 12. Launch Requirements

AuxPoW must not be considered operational until:

- The specification is complete.
- The code is implemented.
- Independent nodes validate proofs correctly.
- Mining pool integration is tested.
- Independent security review is completed.

## 13. Status

This document is a proposed design.

No operational Deliro merged-mining network is currently claimed to exist.

## 14. Core Principle

Don't trust the founder. Verify the rules.
