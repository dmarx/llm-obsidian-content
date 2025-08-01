---
date: 1712287389.094599
tags:
- autogenerated
- source__oai
- conversation_id__640a966b-b331-4c8a-bd2c-4a209b37b4f3
- msg_aaa26374-87b0-4897-80e8-cd764c0a52ee
- msg_89123d27-f485-4635-bad1-96040afd2ebc
- colorclass/information-theory
title: lebesgue measure
---

**USER**

Lebesgue Measure


**ASSISTANT**

The [[Lebesgue Measure|Lebesgue measure]] plays a foundational role in modern analysis, particularly in the theory of integration and probability. It generalizes the concept of length, area, and volume in a way that accommodates a broader class of sets than those typically manageable by the traditional Riemann integral. This measure was introduced by Henri Lebesgue in the early 20th century to facilitate the integration of functions that are difficult or impossible to integrate in the Riemann sense.

### Definition

The Lebesgue measure, denoted as $\lambda$, is a way of assigning a volume to subsets of $n$-dimensional Euclidean space $\mathbb{R}^n$. For $n=1$, it represents the length of intervals or unions of intervals; for $n=2$, it represents the area, and for $n=3$, the volume. This measure is defined for a more comprehensive set of objects than those typically measurable by simpler notions of volume.

The formal construction of the Lebesgue measure involves several steps, starting with the concept of outer measure and then restricting this measure to a class of sets called Lebesgue measurable sets.

#### Outer Measure

The Lebesgue outer measure of a set $A \subseteq \mathbb{R}^n$ is defined as the infimum of the sums of the volumes of countable collections of $n$-dimensional rectangles that cover $A$. Mathematically, this can be expressed as:

$$
\lambda^*(A) = \inf\left\{\sum_{k=1}^\infty \text{vol}(R_k) : A \subseteq \bigcup_{k=1}^\infty R_k, \, R_k \text{ are } n\text{-dimensional rectangles}\right\}
$$

where $\text{vol}(R_k)$ denotes the volume of the $k$-th rectangle.

#### Lebesgue Measurable Sets

A set $A \subseteq \mathbb{R}^n$ is Lebesgue measurable if, for every subset $E \subseteq \mathbb{R}^n$, the following holds:

$$
\lambda^*(E) = \lambda^*(E \cap A) + \lambda^*(E \setminus A)
$$

This condition essentially states that the outer measure of any set can be decomposed into the sum of the outer measures of its intersection with $A$ and the set difference with $A$. The collection of Lebesgue measurable sets is denoted by $\mathcal{M}$.

#### Properties of the Lebesgue Measure

The Lebesgue measure has several key properties that make it suitable for analysis:

- **Translation Invariance**: For any Lebesgue measurable set $A$ and any vector $v \in \mathbb{R}^n$, the set $A+v = \{a+v : a \in A\}$ is measurable, and $\lambda(A+v) = \lambda(A)$.
- **Countable Additivity**: If $\{A_i\}_{i=1}^\infty$ is a countable collection of disjoint Lebesgue measurable sets, then $\lambda(\bigcup_{i=1}^\infty A_i) = \sum_{i=1}^\infty \lambda(A_i)$.
- **Completeness**: Every subset of a set of Lebesgue measure zero is also Lebesgue measurable, and its measure is zero.

### Significance

The Lebesgue measure's ability to measure a wider class of sets than simple geometric shapes allows for the integration of functions that are discontinuous or not nicely behaved over intervals. This flexibility makes the [[Lebesgue Integral|Lebesgue integral]] a more powerful and general tool for analysis, laying the groundwork for modern probability theory, functional analysis, and other areas of mathematics.


---


following: [[monotone convergence theorem]]

See also: [[probability theory]]