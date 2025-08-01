---
date: 1726730947.576609
tags:
- autogenerated
- source__oai
- conversation_id__66ebd29c-ad84-8008-8c0b-97c85d6b5d2a
- msg_69ff84bb-0e7a-4e35-bf33-338411a55fde
title: _untitled_69ff84bb-0e7a-4e35-bf33-338411a55fde
---


**ASSISTANT**

A **Machin-like formula** is a type of identity for $\pi$ that generalizes the famous formula discovered by John Machin in 1706. These formulas express $\pi$ as a sum of arctangents of rational numbers, and they are particularly useful for high-precision computations of $\pi$ because of their fast convergence properties.

The original Machin's formula for $\pi$ is:

$$
\frac{\pi}{4} = 4 \arctan\left(\frac{1}{5}\right) - \arctan\left(\frac{1}{239}\right)
$$

More generally, a **Machin-like formula** for $\pi$ takes the form:

$$
\frac{\pi}{4} = \sum_{i=1}^{n} a_i \arctan\left(\frac{1}{b_i}\right)
$$

where $a_i$ are integers (or rational numbers), and $b_i$ are integers, often carefully chosen to ensure that the series converges quickly.

### Derivation Outline
The derivation of these formulas usually relies on the additive and subtractive identities for the arctangent function. Specifically:

$$
\arctan(x) + \arctan(y) = \arctan\left( \frac{x + y}{1 - xy} \right)
$$

and

$$
\arctan(x) - \arctan(y) = \arctan\left( \frac{x - y}{1 + xy} \right)
$$

These identities allow for the decomposition of a larger arctangent into sums of smaller ones, which can often be represented as rational numbers.

### Example of a Machin-like Formula
One well-known example of a Machin-like formula is due to William Jones:

$$
\frac{\pi}{4} = 12 \arctan\left(\frac{1}{18}\right) + 8 \arctan\left(\frac{1}{57}\right) - 5 \arctan\left(\frac{1}{239}\right)
$$

### Convergence Properties
The fast convergence of Machin-like formulas makes them particularly useful for the computation of $\pi$. Each arctangent term can be expanded in its power series:

$$
\arctan(x) = \sum_{n=0}^{\infty} \frac{(-1)^n x^{2n+1}}{2n+1}, \quad \text{for} \ |x| \leq 1
$$

When $x$ is small, the terms in the series diminish quickly, allowing for efficient computation of $\arctan(x)$. This is the reason why Machin-like formulas often use small values for the arguments of the arctangent function.

### Computational Significance
Machin-like formulas have been crucial in computing $\pi$ to many digits. For example, the modern record calculations of $\pi$—extending to trillions of digits—often use variations of Machin-like formulas because they provide high precision with fewer terms in the expansion compared to direct methods based on the Leibniz series for $\pi$.

If you want to explore other related methods, check out the [[Leibniz Formula for Pi]] and the [[Gauss-Legendre Algorithm]], which are also historically important in the computation of $\pi$.


---

preceding: [[machin-like formula]]