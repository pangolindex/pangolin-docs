---
description: Liquidity Provider and Protocol Fees
---

# Fees

{% hint style="info" %}
At launch, the protocol charge is default to 0, and the liquidity provider fee is **0.30%**. If the protocol charge is switched on, it will become **0.05%** and the liquidity provider fee will be **0.25%**.
{% endhint %}

## Liquidity provider fees

There is a **0.30%** fee for swapping tokens. **This fee is split by liquidity providers proportional to their contribution to liquidity reserves.**

Swapping fees are immediately deposited into liquidity reserves. This increases the value of liquidity tokens, functioning as a payout to all liquidity providers proportional to their share of the pool. Fees are collected by burning liquidity tokens to remove a proportional share of the underlying reserves.

Since fees are added to liquidity pools, the invariant increases at the end of every trade. Within a single transaction, the invariant represents `token0_pool / token1_pool` at the end of the previous transaction.

## Protocol Fees

This feature, which is hard-coded into the core contracts and remain decentralized, non-upgradable and directed by a governance process, is currently turned **on** and is used for the funding of our market maker. Once funded, a community vote will be introduced for further use of it.

## Protocol Charge Calculation

The protocol-wide charge of **0.05%** per trade represents **⅙th** \(16.6̅%\) of the **0.30%** fee. The fee is in effect if `feeTo` is not `address(0)` `(0x0000000000000000000000000000000000000000)`, indicating that `feeTo` is the recipient of the charge.

This amount would not affect the fee paid by traders, but would affect the amount received by liquidity providers.

Rather than calculating this charge on swaps, which would significantly increase gas costs for all users, the charge is instead calculated when liquidity is added or removed.

