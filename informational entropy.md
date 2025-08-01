---
date: 1712292395.812909
tags:
- autogenerated
- source__oai
- conversation_id__5ae74654-7f02-4b97-8afa-ab8a475f0978
- msg_aaa2225c-a70a-466d-9ccd-9c9615735b54
- msg_cd654d35-88fe-4f0f-acae-926ce232d7ad
- colorclass/information-theory
title: informational entropy
---

**USER**

informational entropy


**ASSISTANT**

Informational entropy, often simply called entropy in the context of information theory, is a measure of the unpredictability or uncertainty associated with a random variable. Introduced by Claude Shannon in his seminal 1948 paper, "A Mathematical Theory of Communication," entropy has become a foundational concept in information theory, with applications ranging from telecommunications to thermodynamics, cryptography, and complexity theory.

### Mathematical Definition

For a discrete random variable $X$ with possible outcomes $x_1, x_2, \ldots, x_n$ that occur with probabilities $p(x_1), p(x_2), \ldots, p(x_n)$, the entropy $H(X)$ of $X$ is defined as:

$$H(X) = -\sum_{i=1}^{n} p(x_i) \log_b p(x_i)$$

where the base $b$ of the logarithm determines the unit of entropy. Common choices for $b$ are 2 (leading to units of bits), $e$ (nats), and 10 (dits or bans). The most common choice in information theory is base 2, reflecting the binary nature of digital communication and computation.

### Interpretation and Properties

- **Uncertainty and Information Content:** Entropy measures the average amount of information produced by a stochastic source of data. The higher the entropy, the greater the uncertainty or randomness of the random variable's outcomes, and thus, the more information is produced on average with each outcome.
- **Maximum Entropy:** The entropy of a random variable reaches its maximum when all outcomes are equally likely, signifying maximum uncertainty about which outcome will occur.
- **Additivity:** For two independent random variables $X$ and $Y$, the entropy of their joint distribution is the sum of their individual entropies, i.e., $H(X, Y) = H(X) + H(Y)$.

### Applications

- **Data Compression:** Entropy provides a lower bound on the average length of the shortest possible lossless encoding of messages produced by a source. Huffman coding and arithmetic coding are examples of entropy-based data compression algorithms.
- **Cryptographic Security:** In cryptography, the entropy of keys and passwords is a measure of their unpredictability and resistance to brute-force attacks.
- **Thermodynamics and Statistical Mechanics:** There is a deep analogy between informational entropy and the thermodynamic entropy defined in statistical mechanics, where entropy measures the disorder of a physical system. The Boltzmann entropy formula $S = k \log \Omega$, where $S$ is the entropy, $k$ is the Boltzmann constant, and $\Omega$ is the number of microstates, mirrors Shannon's formula in its logarithmic measure of the number of possible states.
- **Quantum Information Theory:** Entropy also plays a critical role in quantum computing and quantum information theory, where it is used to quantify entanglement and the information content of quantum states.

### Extensions and Related Concepts

- **Conditional Entropy:** Measures the amount of information needed to describe the outcome of a random variable $Y$ given that the value of another random variable $X$ is known.
- **Joint Entropy:** The entropy of a combined system of two random variables.
- **Mutual Information:** A measure of the amount of information that one random variable contains about another random variable.
- **Cross Entropy and Kullback–Leibler Divergence:** Measures of the difference between two probability distributions, widely used in machine learning to define loss functions.

Informational entropy is a powerful tool for understanding and quantifying information, uncertainty, and complexity in a wide range of disciplines.


---

preceding: [[group]]  


following: [[catallaxy]]

See also: [[information as a physical entity]]


See also: [[entropy as a bridge between information and physics]]


See also: [[reversibility is critical because it illustrates that energy dissipation in information processing is not due to the computation itself, but to the loss of information. this reinforces the idea that]]


See also: [[information theory]]


See also: [[thermodynamic entropy is essentially a measure of missing information about which microstate the system is in, given only knowledge of its macroscopic state. the more microstates there are that could]]


See also: [[revisit the relationship between variance explained and least action, taking into consideration the relationship between the fisher information matrix and the lagrangian]]


See also: [[biological information theory]]


See also: [[random variables]]


See also: [[infodynamics]]


See also: [[entropy management]]


See also: [[physicality of information]]