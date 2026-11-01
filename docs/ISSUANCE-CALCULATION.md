# DELIRO — Issuance Calculation

Version: 0.1
Status: Verified Mathematical Draft — Not Active

## 1. Supply Limit

Maximum permitted supply: 8,000,000 DEL.

One DEL equals 100,000,000 base units.

## 2. Initial Reward

Initial block subsidy: 1,904,761,904 base units.

Equivalent to 19.04761904 DEL.

## 3. Halving Rules

Halving interval: 210,000 blocks.

At each halving, the subsidy is calculated using integer division:

new_subsidy = previous_subsidy / 2

Any fractional base unit is discarded.

Floating-point arithmetic is forbidden in consensus calculations.

## 4. Issuance Calculation

Each reward era contains 210,000 blocks.

The subsidy reaches 1 base unit in era 30.

The subsidy becomes zero in era 31.

Total scheduled mining issuance:

799,999,997,160,000 base units.

Equivalent to:

7,999,999.9716 DEL.

## 5. Remaining Supply

The difference between the maximum supply and scheduled issuance is:

2,840,000 base units.

Equivalent to:

0.0284 DEL.

This amount is not automatically issued.

## 6. Consensus Requirements

- The maximum supply must never be exceeded.
- Block rewards must follow the exact integer schedule.
- Zero subsidy must remain zero.
- No administrator may create additional coins.
- Independent tests must verify every halving boundary.

## 7. Important Notice

This is a mathematical protocol draft.

It is not yet implemented in blockchain software.

All consensus rules require independent review and testing before launch.
