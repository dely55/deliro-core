# DELIRO — Transaction Rules

Version: 0.1
Status: Draft — Not Implemented

## 1. Purpose

This document describes the proposed rules for creating, validating, and confirming transactions on the Deliro network.

## 2. Transaction Model

Deliro plans to use the Unspent Transaction Output (UTXO) model.

Each transaction spends one or more previously created unspent outputs and creates new outputs.

## 3. Transaction Structure

A transaction is expected to contain:

- Transaction version
- Input references
- Output values
- Locking scripts
- Unlocking scripts or witnesses
- Transaction lock time

The exact serialization format must be specified before implementation.

## 4. Transaction Signatures

Transactions must be authorized by valid cryptographic signatures.

Private keys must remain under the control of their owners.

Full nodes must verify transaction signatures independently.

## 5. Double-Spending Protection

A transaction must not spend an output that has already been spent.

Full nodes must maintain and verify the current UTXO set.

Conflicting transactions must not both be accepted into the same valid chain history.

## 6. Value Conservation

For every valid transaction:

Total input value must be greater than or equal to total output value.

The difference is the transaction fee.

All monetary calculations must use integer base units.

Floating-point arithmetic is forbidden.

## 7. Transaction Fees

Users may specify transaction fees according to the network's fee policy.

The exact fee calculation and relay policy must be defined before implementation.

Valid transaction fees are collected by the block producer.

## 8. Mempool

Full nodes may maintain a memory pool of valid, unconfirmed transactions.

Mempool transactions are not final until included in a valid block.

Nodes may apply transparent relay and resource limits.

## 9. Block Inclusion

Miners may select valid transactions for inclusion in a block.

Every full node must independently verify all included transactions.

Invalid transactions must cause the block to be rejected.

## 10. Transaction Confirmation

A transaction is considered confirmed when included in a valid block.

Additional confirmations increase confidence that the transaction will remain in the accepted chain history.

No fixed number of confirmations guarantees absolute finality.

## 11. Invalid Transactions

Nodes must reject transactions with:

- Invalid signatures
- Invalid input references
- Already-spent inputs
- Negative or out-of-range values
- Outputs exceeding inputs
- Invalid serialization
- Unauthorized creation of coins

## 12. Privacy

The public blockchain will expose transaction data.

Users should not assume that ordinary transactions provide complete privacy.

Privacy features must be separately specified and reviewed before implementation.

## 13. Testing Requirements

Before launch, the implementation must include:

- Signature validation tests
- UTXO consistency tests
- Double-spend rejection tests
- Value conservation tests
- Fee calculation tests
- Mempool validation tests
- Transaction serialization tests
- Invalid transaction rejection tests

## 14. Launch Status

These rules are a proposed design.

They are not yet implemented or active consensus rules.

## 15. Core Principle

Don't trust the founder. Verify the rules.
