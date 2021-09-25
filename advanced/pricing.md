---
description: Learn how prices are determined and handled
---

# Pricing

## How are prices determined?

Each pair on **Pangolin** is actually underpinned by a liquidity pool. Liquidity pools are smart contracts that hold balances of two unique tokens and enforces rules around depositing and withdrawing them. The primary rule is the constant product formula `x * y = k`. When a token is withdrawn \(bought\), a proportional amount must be deposited \(sold\) to maintain the constant. The ratio of tokens in the pool, in combination with the constant product formula, ultimately determine the price that a swap executes at.

## How Pangolin handles prices

Pairs directly check whether the invariant was satisfied \(accounting for fees\) after every trade. This means that rather than relying on a pricing function to _also_ enforce the invariant, pairs simply and transparently ensure their own safety. One downstream benefit is that pairs will more naturally support other flavors of trades which may emerge, \(e.g. trading to a specific price at execution time\).

At a high level, _trades must be priced in the periphery_. The good news is that internal functions make this quite simple, and all swapping functions in the router are designed with this in mind.

## Understanding Returns

**Pangolin** incentivizes users to add liquidity to trading pools by rewarding providers with the fees generated when other users trade with those pools. Market making, in general, is a complex activity. There is a risk of losing money during large and sustained movement in the underlying asset price compared to simply holding an asset \(Impermanent Loss\)

