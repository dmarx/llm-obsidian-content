---
date: 1721882305.742364
tags:
- autogenerated
- source__oai
- conversation_id__91d0b461-37b0-4e34-904d-d5ee935d61bb
- msg_aaa2bb03-b7eb-402e-b6f5-a7725cfd57e2
- msg_bfb69d4e-1986-48c6-97c1-b73c0371356e
- colorclass/information-theory
title: optional stopping theorem
---

**USER**

Optional Stopping Theorem


**ASSISTANT**

### Optional Stopping Theorem

The **Optional Stopping Theorem** (OST) is a fundamental result in the theory of [[martingales]]. It provides conditions under which the expected value of a martingale at a stopping time is equal to its initial expected value. This theorem has significant implications in [[gambling theory]], finance, and stochastic processes.

### Statement of the Optional Stopping Theorem

Let \( \{M_t\}_{t \geq 0} \) be a martingale with respect to a filtration \( \{ \mathcal{F}_t \} \) and let \( \tau \) be a stopping time with respect to the same filtration. The Optional Stopping Theorem states that if \( \tau \) satisfies certain conditions, then:

$$
E[M_\tau] = E[M_0].
$$

### Conditions for the Theorem

The OST holds under any one of the following conditions:

1. **Bounded Stopping Time**: \( \tau \) is almost surely bounded, i.e., there exists a constant \( C \) such that \( \tau \leq C \) almost surely.
2. **Square-Integrable Martingale and Stopping Time**: The martingale \( M_t \) is uniformly integrable, or \( M_t \) is a square-integrable martingale (i.e., \( E[M_t^2] < \infty \) for all \( t \)), and \( \tau \) is a stopping time such that \( E[\tau] < \infty \).
3. **Martingale and Finite Expectation**: The martingale \( M_t \) is such that the stopped process \( M_{t \wedge \tau} \) is uniformly integrable.

### Intuition and Interpretation

The Optional Stopping Theorem provides a formal way to understand the concept of "fair games" in the context of [[martingales]]. It asserts that under suitable conditions, stopping a martingale at a random time (that depends on the history up to that time) does not change the expected value of the martingale. This is crucial in ensuring that no arbitrage opportunities exist in fair games or financial markets.

### Proof Sketch

The proof of the Optional Stopping Theorem relies on the Doob's Optional Sampling Theorem and the concept of uniformly integrable [[martingales]]. Here's a brief sketch for the case where \( \tau \) is bounded:

1. **Bounded Stopping Time**: If \( \tau \) is almost surely bounded by \( C \), then \( M_\tau = M_{\tau \wedge C} \).

2. **Doob's Stopping Time**: Applying Doob's Stopping Time theorem, we have:
   \[
   E[M_{\tau \wedge C}] = E[M_0].
   \]

3. **Conclusion**: Since \( \tau \) is bounded by \( C \), we conclude:
   \[
   E[M_\tau] = E[M_{\tau \wedge C}] = E[M_0].
   \]

### Applications in Finance

#### 1. **Gambling Strategies**

In gambling, the Optional Stopping Theorem implies that a fair betting strategy cannot lead to a guaranteed profit if the game is fair (i.e., the betting outcomes form a martingale). This result discourages the notion of "sure-win" betting strategies.

#### 2. **American Option Pricing**

In the context of American options, the holder has the right to exercise the option at any time before expiration. The OST can be used to show that the fair price of the option must consider the optimal stopping strategy, ensuring no arbitrage in pricing.

### Example

Consider a simple symmetric random walk \( \{S_n\}_{n \geq 0} \), where \( S_n = \sum_{i=1}^n X_i \) with \( X_i \) being i.i.d. random variables taking values \( +1 \) or \( -1 \) with equal probability. Let \( \tau \) be the first time \( S_n \) reaches \( +k \) or \(-k \), for some \( k > 0 \).

1. **Martingale Property**: The process \( \{S_n\} \) is a martingale with \( E[S_n] = 0 \).

2. **Stopping Time**: \( \tau \) is the stopping time defined by:
   \[
   \tau = \inf\{n \geq 0 : |S_n| = k \}.
   \]

3. **Expected Value at Stopping Time**: Applying the OST, we have:
   \[
   E[S_\tau] = E[S_0] = 0.
   \]

4. **Symmetry**: Given the symmetry of the problem, the probability of reaching \( +k \) or \(-k \) is equal. Therefore, the expected value at the stopping time is zero, confirming the OST result.

### Conclusion

The Optional Stopping Theorem is a cornerstone in the theory of [[martingales]], providing essential insights into the behavior of stochastic processes under random stopping times. Its applications span various fields, including finance, [[gambling theory]], and stochastic processes, ensuring that expectations remain consistent under fair conditions. Understanding the conditions and implications of the OST is crucial for anyone working with [[martingales]] and their applications.


---

preceding: [[radon-nikodym derivative]]  


following: [[theory of [[martingales]]]]

See also: [[random variables]]


See also: [[stochastic processes]]