# DELIRO — Security Threat Model

Version: 0.1
Status: Draft — Not Implemented

## 1. Purpose

This document identifies potential security threats to the Deliro network and describes the protections that must be designed and tested before launch.

## 2. Consensus Attacks

Potential threats include:

- Invalid blocks
- Invalid transactions
- Unauthorized coin creation
- Double-spending
- Invalid mining rewards
- Manipulation of block timestamps
- Attempts to bypass the maximum supply

Full nodes must independently validate every block and transaction according to the consensus rules.

## 3. Mining Attacks

Potential threats include:

- 51% hash-rate attacks
- Selfish mining
- Block withholding
- Mining pool centralization
- Invalid AuxPoW proofs

The network must validate all Proof-of-Work and AuxPoW data.

Merged mining does not guarantee protection from attacks.

## 4. Network Attacks

Potential threats include:

- Sybil attacks
- Eclipse attacks
- Denial-of-Service attacks
- Malicious peer connections
- Network partitioning

The peer-to-peer network must be designed to reduce these risks.

## 5. Wallet Security

Wallet software must protect private keys.

Required protections include:

- Secure private-key generation
- Secure key storage
- Transaction verification
- Clear backup and recovery procedures
- Protection against unauthorized signing

The project must never collect users' private keys.

## 6. Founder and Administrator Restrictions

No founder, developer, website administrator, or mining pool operator may have protocol-level authority to:

- Create additional coins
- Freeze user balances
- Confiscate funds
- Reverse valid transactions
- Change consensus rules unilaterally

Website administration must remain separate from blockchain consensus.

## 7. Software Supply Chain

The project must protect its source code and release process.

Required measures include:

- Public source code
- Reviewed code changes
- Reproducible builds where practical
- Signed software releases
- Dependency review
- Security vulnerability reporting

## 8. Testing Requirements

Before launch, the project requires:

- Unit tests
- Integration tests
- Consensus tests
- Adversarial testing
- AuxPoW validation tests
- Independent security audits

## 9. Incident Response

The project must publish a transparent process for reporting vulnerabilities and communicating security incidents.

Emergency procedures must not create hidden centralized control over user funds or consensus.

## 10. Launch Requirement

Deliro must not be presented as a secure, operational blockchain until its software has been implemented, independently reviewed, and tested.

## 11. Core Principle

Don't trust the founder. Verify the rules.
