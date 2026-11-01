# DELIRO — Mining and Supply Draft

Version: 0.1
Status: Draft — Not Active

## 1. Maximum Supply

The proposed maximum supply is 8,000,000 DEL.

One DEL is divisible into 100,000,000 base units.

The network must never create coins beyond the maximum supply.

## 2. Initial Block Reward

Proposed initial block reward:

19.04761904 DEL

This value is provisional and must be validated by exact integer arithmetic before implementation.

## 3. Block Time

Target block interval: 10 minutes.

## 4. Halving

The proposed block reward halving interval is 210,000 blocks.

The reward is intended to decrease by half after each halving interval.

All reward calculations must use integer base units, never floating-point arithmetic.

## 5. Mining Only

All coins must enter circulation through valid mining rewards.

There will be:

- No premine.
- No founder allocation.
- No hidden rewards.
- No central minting authority.

## 6. Transaction Fees

Transaction fees are paid to the block producer according to public consensus rules.

## 7. No Tail Emission

No permanent block reward after scheduled rewards reach zero is currently planned.

## 8. Supply Verification

Before launch, independent tests must verify:

- Total possible issuance.
- Every halving boundary.
- Integer rounding behavior.
- Maximum supply enforcement.
- Rejection of invalid block rewards.

## 9. Important Notice

This document is a proposal, not active blockchain software.

The exact emission schedule must be mathematically verified before it becomes a consensus rule.
