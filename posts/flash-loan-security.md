---
title: "Flash Loan Security Best Practices"
date: "2025-12-12"
description: "How to protect your protocol from flash loan attacks and price manipulation."
---

Flash loans have revolutionized DeFi but also introduced new attack vectors. Here's how to build flash-loan resistant protocols.

## Understanding the Risk

Flash loans allow borrowing unlimited funds without collateral, as long as the loan is repaid within the same transaction. Attackers use this to:

- Manipulate oracle prices
- Exploit governance voting
- Drain liquidity pools

## Defense Strategies

1. **Use time-weighted oracles** (TWAP)
2. **Implement transaction delays** for sensitive operations
3. **Check for flash loan indicators**
4. **Limit single-transaction impacts**

Build with these patterns in mind to create more resilient protocols.
