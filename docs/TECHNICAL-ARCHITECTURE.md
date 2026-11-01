# DELIRO — Technical Architecture

Version: 0.1
Status: Proposed Architecture — Not Implemented

## 1. Overview

Deliro is designed as an independent peer-to-peer cryptocurrency network.

The software will be open-source and independently verifiable.

## 2. Main Components

The planned software consists of:

- Full Node
- Blockchain Database
- Peer-to-Peer Network
- Transaction Validation
- Block Validation
- Proof-of-Work Mining
- AuxPoW Verification
- Wallet Software
- Command-Line Interface
- Blockchain Explorer

## 3. Full Nodes

Full nodes must independently verify:

- Blocks
- Transactions
- Mining rewards
- Proof-of-Work
- Consensus rules
- Maximum supply

No central server should be required to approve ordinary transactions.

## 4. Peer-to-Peer Network

Nodes communicate directly with other nodes.

The network must support:

- Peer discovery
- Block propagation
- Transaction propagation
- Network synchronization

## 5. Wallet

The wallet must allow users to:

- Generate private keys
- Generate public addresses
- Send transactions
- Receive transactions
- Verify transaction status

Private keys must remain under the user's control.

## 6. Mining

The planned mining algorithm is SHA-256d.

AuxPoW merged mining is planned.

Mining rewards must follow the exact consensus issuance schedule.

## 7. Security

The software requires:

- Independent code review
- Automated testing
- Network testing
- Cryptographic verification
- Security audits

## 8. Development Principle

No website administrator or founder account may control consensus rules, create coins, freeze balances, or confiscate funds.

## 9. Development Status

This document describes a proposed architecture.

No functional Deliro blockchain software is currently claimed to exist.
