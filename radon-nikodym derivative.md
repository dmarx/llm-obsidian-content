---
date: 1721882254.868389
tags:
- autogenerated
- source__oai
- conversation_id__91d0b461-37b0-4e34-904d-d5ee935d61bb
- msg_aaa2eae6-ee3c-4e77-b32b-aa82f2517f86
- msg_747aab67-6e90-49a8-8301-55e4418aed42
- colorclass/information-theory
title: radon-nikodym derivative
---

**USER**

Radon-Nikodym Derivative


**ASSISTANT**

### Radon-Nikodym Derivative

The **Radon-Nikodym Derivative** is a fundamental concept in measure theory that provides a way to relate two measures. It plays a crucial role in probability theory and financial mathematics, especially in the context of changing probability measures (e.g., moving from a real-world measure to a risk-neutral measure in option pricing).

### Definition

Let \( \mu \) and \( \nu \) be two \(\sigma\)-finite measures on a measurable space \((\Omega, \mathcal{F})\). If \(\nu\) is absolutely continuous with respect to \(\mu\) (denoted by \(\nu \ll \mu\)), there exists a measurable function \( \frac{d\nu}{d\mu} \) called the **Radon-Nikodym derivative** of \(\nu\) with respect to \(\mu\) such that for any measurable set \( A \in \mathcal{F} \),

$$
\nu(A) = \int_A \frac{d\nu}{d\mu} \, d\mu.
$$

### Properties

1. **Linearity**: If \( \nu_1 \) and \( \nu_2 \) are absolutely continuous with respect to \( \mu \), and \( a_1 \) and \( a_2 \) are constants, then

   $$
   \frac{d(a_1 \nu_1 + a_2 \nu_2)}{d\mu} = a_1 \frac{d\nu_1}{d\mu} + a_2 \frac{d\nu_2}{d\mu}.
   $$

2. **Chain Rule**: If \( \nu \ll \mu \) and \( \mu \ll \lambda \), then

   $$
   \frac{d\nu}{d\lambda} = \frac{d\nu}{d\mu} \cdot \frac{d\mu}{d\lambda}.
   $$

3. **Non-Negativity**: The Radon-Nikodym derivative \( \frac{d\nu}{d\mu} \) is non-negative \(\mu\)-almost everywhere.

### Example

Consider a probability space \((\Omega, \mathcal{F}, P)\) and a sub-\(\sigma\)-algebra \(\mathcal{G} \subseteq \mathcal{F}\). The conditional expectation \( E[X \mid \mathcal{G}] \) can be interpreted as the Radon-Nikodym derivative of the measure \( \nu(A) = E[X \mathbf{1}_A] \) with respect to \( P \):

$$
E[X \mid \mathcal{G}] = \frac{d\nu}{dP}.
$$

### Application in Financial Mathematics

#### 1. **Change of Measure**

In financial mathematics, the Radon-Nikodym derivative is used to change from the real-world probability measure \( P \) to the risk-neutral measure \( Q \). This is crucial for pricing derivatives.

Suppose \( \{W_t\}_{t \geq 0} \) is a standard Brownian motion under the measure \( P \). To change to a new measure \( Q \) where the process has a different drift, we define:

$$
\left. \frac{dQ}{dP} \right|_{\mathcal{F}_t} = Z_t,
$$

where \( Z_t \) is a density process satisfying:

$$
Z_t = \exp \left( -\int_0^t \theta_s \, dW_s - \frac{1}{2} \int_0^t \theta_s^2 \, ds \right),
$$

with \( \theta_t \) being an adapted process.

Under the new measure \( Q \), the process \( W_t^Q = W_t + \int_0^t \theta_s \, ds \) is a Brownian motion.

#### 2. **Girsanov's Theorem**

Girsanov's Theorem leverages the Radon-Nikodym derivative to change the measure such that the Brownian motion under the original measure \( P \) is transformed into a Brownian motion with a new drift under the measure \( Q \). This theorem is fundamental in the risk-neutral pricing of derivatives.

### Proof Sketch of the Radon-Nikodym Theorem

To prove the existence and uniqueness of the Radon-Nikodym derivative, we use the Radon-Nikodym Theorem. The proof involves the following steps:

1. **Existence**: Construct the Radon-Nikodym derivative by considering the set function \( \nu \) and demonstrating that it can be expressed as an integral with respect to \( \mu \).

2. **Uniqueness**: Show that if there were two different functions satisfying the Radon-Nikodym property, their difference would integrate to zero over any measurable set, implying they are equal almost everywhere.

### Conclusion

The Radon-Nikodym derivative is a powerful tool in measure theory that allows for the transformation of one measure into another. Its applications in probability theory and financial mathematics, particularly in the context of changing measures and pricing derivatives, are profound. Understanding this concept is crucial for anyone working in fields that involve stochastic processes and measure-theoretic probability.


---

preceding: [[doob's decomposition theorem]]  


following: [[optional stopping theorem]]---
date: '2024-11-26T15:38:01.589907Z'
tags:
- autogenerated
- source__claude
- conversation_id__f5981a65-0e29-42ab-ad41-7909aa1e5199
- msg_cb8f5cf2-301b-4c28-ae63-ebe208455c24
- msg_c5e2f543-2d0f-45f6-b77c-2f3734caf1ca
title: radon-nikodym derivative
---


**USER**

Radon-Nikodym derivative


**ASSISTANT**

# Radon-Nikodym Derivative

The [[Radon-Nikodym derivative]] is a fundamental concept in [[measure theory]] that generalizes the notion of probability density functions and enables the comparison of measures. It represents how one measure can be expressed in terms of another measure through a function.

## Formal Definition

Let $(X, \Sigma)$ be a [[measurable space]], and let $\mu$ and $\nu$ be [[σ-finite measures]] on this space. If $\nu$ is [[absolutely continuous]] with respect to $\mu$ (denoted $\nu \ll \mu$), then there exists a unique (up to $\mu$-almost everywhere equivalence) measurable function $f: X \rightarrow [0,\infty]$ such that:

$\nu(E) = \int_E f \, d\mu$

for all measurable sets $E \in \Sigma$. This function $f$ is called the Radon-Nikodym derivative of $\nu$ with respect to $\mu$, denoted:

$f = \frac{d\nu}{d\mu}$

## Properties

1. **Uniqueness**: The Radon-Nikodym derivative is unique up to $\mu$-almost everywhere equivalence.

2. **Chain Rule**: For measures $\lambda \ll \nu \ll \mu$:
   
   $\frac{d\lambda}{d\mu} = \frac{d\lambda}{d\nu} \cdot \frac{d\nu}{d\mu}$ ($\mu$-almost everywhere)

3. **Leibniz Rule**: For measures $\nu_1, \nu_2 \ll \mu$:
   
   $\frac{d(\nu_1 + \nu_2)}{d\mu} = \frac{d\nu_1}{d\mu} + \frac{d\nu_2}{d\mu}$ ($\mu$-almost everywhere)

## Applications

### Probability Theory

In probability theory, the Radon-Nikodym derivative appears as:

1. **Probability Density Functions**: For a continuous random variable, the PDF is the Radon-Nikodym derivative of its probability measure with respect to Lebesgue measure.

2. **Likelihood Ratios**: The [[likelihood ratio]] between two probability measures $P$ and $Q$ is:

   $L(x) = \frac{dP}{dQ}(x)$

### Statistical Physics

In [[statistical mechanics]], the [[relative entropy]] (or [[Kullback-Leibler divergence]]) between probability measures $P$ and $Q$ is defined using the Radon-Nikodym derivative:

$D_{KL}(P\|Q) = \int \log\left(\frac{dP}{dQ}\right) \, dP$

### Machine Learning

The concept appears in:

1. **[[Importance Sampling]]**: The importance weight is a Radon-Nikodym derivative.
2. **[[Variational Inference]]**: Many variational methods involve optimizing over Radon-Nikodym derivatives.

## Geometric Interpretation

The Radon-Nikodym derivative can be understood geometrically as the "local ratio" between measures. In differential geometry terms, it represents the [[Jacobian determinant]] of the transformation between measure spaces.

## Related Concepts

- [[Lebesgue Decomposition Theorem]]
- [[Absolutely Continuous Functions]]
- [[Change of Measure]]
- [[Likelihood Ratio]]
- [[Information Geometry]]

See also: [[probability measure]]


See also: [[probability theory]]


See also: [[stochastic processes]]


See also: [[variational methods]]