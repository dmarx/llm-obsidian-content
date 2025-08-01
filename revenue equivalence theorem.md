---
date: 1721547527.7953
tags:
- autogenerated
- source__oai
- conversation_id__7678c9df-b2e7-490a-a121-059ebdb8156b
- msg_aaa28fac-474b-4856-8d45-c8809008289a
- msg_1b7d9343-d92c-4fd2-a452-ecbe449c5a1e
- colorclass/game-theory
title: revenue equivalence theorem
---

**USER**

Revenue Equivalence Theorem


**ASSISTANT**

## Revenue Equivalence Theorem

The **Revenue Equivalence Theorem (RET)** is a foundational result in [[auction theory]], which states that under certain conditions, all standard auction formats yield the same expected revenue. This theorem has significant implications for the design and analysis of auction mechanisms.

### Conditions for Revenue Equivalence

The RET holds under the following assumptions:

1. **Risk-Neutral Bidders**: Bidders are indifferent to risk and aim to maximize their expected utility.
2. **Independent Private Values**: Each bidder knows their own valuation of the item, which is independent of the valuations of other bidders.
3. **Symmetric Bidders**: All bidders have valuations drawn from the same probability distribution.
4. **Auction Symmetry**: The auction format treats all bidders identically.
5. **Payment Rules**: The payment by the winning bidder depends only on their bid.

### Statement of the Theorem

Under these conditions, the expected revenue for the seller is the same across different standard auction formats, including:

- **First-Price Sealed-Bid Auction**: Each bidder submits a single bid without knowing the others' bids. The highest bidder wins and pays their bid.
- **Second-Price Sealed-Bid Auction (Vickrey Auction)**: Each bidder submits a single bid without knowing the others' bids. The highest bidder wins but pays the second-highest bid.
- **English Auction**: An open ascending auction where bidders continuously bid higher amounts until no one is willing to bid higher. The highest bidder wins and pays their bid.
- **Dutch Auction**: An open descending auction where the auctioneer starts with a high price, which is lowered until a bidder accepts the price. The first bidder to accept wins and pays the current price.

### Mathematical Formalization

Let's denote the value of the $i$-th bidder as $V_i$, which is a random variable drawn from a common cumulative distribution function (CDF) $F(v)$ with probability density function (PDF) $f(v)$. 

Consider an auction with $n$ bidders. The expected revenue, $R$, can be expressed as:

$$
R = \mathbb{E}[B(V_{(1)})]
$$

where $V_{(1)}$ is the highest order statistic (the highest valuation among the bidders), and $B(V_{(1)})$ is the bid corresponding to this highest valuation.

### Proof Outline

The proof of the RET involves several steps:

1. **Symmetry and Risk Neutrality**: Due to symmetry and risk neutrality, all bidders employ the same bidding strategy, denoted as $B(v)$.
2. **Incentive Compatibility**: Bidding strategies must be incentive-compatible, meaning each bidder maximizes their expected utility by truthfully revealing their valuation.
3. **Expected Payment**: For each bidder, the expected payment conditional on winning must be the same across different auction formats. In a second-price auction, the expected payment is equal to the expected value of the second-highest bid. In a first-price auction, the equilibrium strategy ensures that the expected payment is the same as in the second-price auction.

#### Detailed Proof for First-Price Auction

Consider a [[first-price sealed-bid auction]] with $n$ bidders. The bidding strategy $B(v)$ for a bidder with valuation $v$ can be derived from the first-order condition for expected utility maximization:

$$
\max_{B_i} \left( V_i - B_i \right) F(B_i)^{n-1}
$$

The first-order condition gives:

$$
V_i F(B_i)^{n-1} - B_i (n-1) F(B_i)^{n-2} f(B_i) = 0
$$

Solving this differential equation, we find the equilibrium bidding strategy:

$$
B(v) = v - \int_0^v \frac{1 - F(t)}{F(t)^{n-1}} dt
$$

This strategy ensures that the expected payment in a first-price auction is equal to the expected payment in a second-price auction, proving revenue equivalence.

### Implications of the RET

The RET has profound implications for auction design:

- **Flexibility in Auction Choice**: Sellers can choose among different auction formats without worrying about differences in expected revenue, provided the RET conditions hold.
- **Focus on Simplicity and Transparency**: Since revenue equivalence holds, sellers can prioritize auction formats that are simpler and more transparent for bidders.
- **Risk Considerations**: While RET assumes risk-neutral bidders, in practice, bidders' risk preferences might influence the choice of auction format.

### Conclusion

The Revenue Equivalence Theorem is a powerful result that simplifies the analysis and design of auctions by demonstrating that, under certain conditions, all standard auction formats yield the same expected revenue. For deeper insights, you might explore related topics such as [[Optimal Auction Design]], [[Myerson's Optimal Auction Theory]], and [[Nash Equilibrium in Auctions]].


---

preceding: [[fundamental results in [[auction theory]]]]  


following: [[incentive compatibility]]