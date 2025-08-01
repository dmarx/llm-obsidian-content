---
date: 1721547795.650423
tags:
- autogenerated
- source__oai
- conversation_id__7678c9df-b2e7-490a-a121-059ebdb8156b
- msg_aaa25714-d017-43af-9d01-5ff8c4d86186
- msg_dd4a78b8-1907-411e-a48e-a27851eddf37
- colorclass/game-theory
title: myerson's optimal auction
---

**USER**

Myerson's Optimal Auction


**ASSISTANT**

## Myerson's Optimal Auction

Roger Myerson's seminal work in 1981 introduced a framework for designing auctions that maximize the seller's expected revenue. Myerson's optimal [[auction theory]] incorporates the concept of **virtual valuations**, which adjust bidders' actual valuations to account for their probability of winning. This approach ensures that the auction design is optimal given the bidders' valuations and distribution.

### Key Concepts

1. **Virtual Valuations**: An adjusted valuation that reflects a bidder's true value and their probability of winning.
2. **Incentive Compatibility**: Ensuring bidders reveal their true valuations.
3. **Revenue Maximization**: The primary goal of the auction design.

### Virtual Valuations

The virtual valuation $\phi(v)$ for a bidder with valuation $v$ and cumulative distribution function (CDF) $F(v)$, with probability density function (PDF) $f(v)$, is given by:

$$
\phi(v) = v - \frac{1 - F(v)}{f(v)}
$$

The virtual valuation essentially adjusts the bidder's valuation to account for the distribution of other bidders' valuations, making it easier to design an auction that maximizes expected revenue.

### Myerson's Optimal Auction Mechanism

1. **Compute Virtual Valuations**: For each bidder, compute the virtual valuation $\phi(v)$.
2. **Allocation Rule**: Allocate the item to the bidder with the highest non-negative virtual valuation. If all virtual valuations are negative, do not allocate the item.
3. **Payment Rule**: The payment each winner makes is determined such that the auction remains incentive-compatible and individually rational.

### Mathematical Formalism

#### Allocation Rule

Let $v_1, v_2, \ldots, v_n$ be the valuations of $n$ bidders. The auctioneer computes the virtual valuations $\phi(v_1), \phi(v_2), \ldots, \phi(v_n)$. The item is allocated to the bidder $i^*$ with the highest non-negative virtual valuation:

$$
i^* = \arg \max_{i} \{ \phi(v_i) \mid \phi(v_i) \geq 0 \}
$$

If $\phi(v_i) < 0$ for all $i$, the item is not allocated.

#### Payment Rule

The payment $p_i$ for the winning bidder $i$ is set such that the mechanism is incentive-compatible. The payment rule is derived from the requirement that the mechanism must be truthful and individual rationality must be satisfied.

To ensure [[incentive compatibility]], the payment for the winning bidder is derived from the threshold valuation $\hat{v}_i$ at which the bidder would be indifferent between winning and losing. This threshold is the lowest valuation for which the bidder would still win the auction. The payment rule can be represented as:

$$
p_i = \phi^{-1}(\max \{\phi(\hat{v}_i), 0\})
$$

### Example

Consider a simple example with two bidders whose valuations $v_1$ and $v_2$ are drawn from the uniform distribution $U[0,1]$.

1. **Compute Virtual Valuations**:
   
   For a uniform distribution $U[0,1]$, $F(v) = v$ and $f(v) = 1$. The virtual valuation $\phi(v)$ is:

   $$
   \phi(v) = v - \frac{1 - v}{1} = 2v - 1
   $$

2. **Allocation Rule**:
   
   Allocate the item to the bidder with the highest virtual valuation. Suppose $v_1 = 0.6$ and $v_2 = 0.8$:

   $$
   \phi(v_1) = 2 \cdot 0.6 - 1 = 0.2
   $$
   $$
   \phi(v_2) = 2 \cdot 0.8 - 1 = 0.6
   $$

   Since $\phi(v_2) > \phi(v_1)$, bidder 2 wins the item.

3. **Payment Rule**:
   
   Calculate the payment for bidder 2. The threshold valuation $\hat{v}_2$ is the valuation at which bidder 2 would just win over bidder 1:

   $$
   \phi(\hat{v}_2) = \phi(v_1) = 0.2
   $$
   Solving for $\hat{v}_2$:
   $$
   2\hat{v}_2 - 1 = 0.2 \implies \hat{v}_2 = 0.6
   $$

   The payment $p_2$ is $\phi^{-1}(0.2)$, which corresponds to the original valuation $\hat{v}_2 = 0.6$. Thus, bidder 2 pays $0.6$.

### Revenue Maximization

Myerson's optimal auction is designed to maximize the seller's expected revenue by appropriately adjusting the allocation and payment rules. This approach ensures that bidders' strategies align with the auction's revenue goals while maintaining [[incentive compatibility]].

### Applications

Myerson's optimal [[auction theory]] has been applied in various domains, including:

- **Spectrum Auctions**: Governments use these principles to design auctions that allocate spectrum licenses efficiently and maximize revenue.
- **Online Advertising**: Ad platforms use auction mechanisms inspired by Myerson's theory to sell ad placements effectively.
- **Procurement**: Businesses use these auction designs to procure goods and services at optimal prices.

### Conclusion

Myerson's optimal [[auction theory]] provides a robust framework for designing auctions that achieve revenue maximization while ensuring truthful bidding and efficient allocation. This theory is a cornerstone of modern auction design, applicable across diverse fields. For further exploration, consider studying [[Revenue Equivalence Theorem]], [[Incentive Compatibility]], and [[VCG Mechanism]].


---

preceding: [[vickrey-clarke-groves (vcg) mechanism]]  


following: [[spectrum auctions]]