---
date: 1739751244.433847
tags:
- autogenerated
- source__oai
- conversation_id__67b26c18-8610-8008-8f24-866d5f3c6ed8
- msg_c719c31b-b65e-4b1b-9b8d-1ad211d80bc8
- msg_aac74978-b855-46f1-8f3b-39b2f3a0569e
- colorclass/information-theory
title: glivenko-cantelli theorem
---

**USER**

Glivenko-Cantelli theorem


**ASSISTANT**

### **Glivenko-Cantelli Theorem**

The **Glivenko-Cantelli theorem** is a fundamental result in empirical process theory that establishes the uniform convergence of the empirical distribution function to the true distribution function. It can be seen as a strong law of large numbers in the space of distribution functions.

---

## **1. Statement of the Theorem**
Let $X_1, X_2, \dots, X_n$ be i.i.d. random variables with cumulative distribution function (CDF) $F(x)$. The **empirical distribution function** (EDF) is defined as:

\[
\hat{F}_n(x) = \frac{1}{n} \sum_{i=1}^{n} \mathbf{1}\{X_i \leq x\},
\]

where $\mathbf{1}\{X_i \leq x\}$ is the indicator function that is 1 if $X_i \leq x$ and 0 otherwise.

The **Glivenko-Cantelli theorem** states that:

\[
\sup_{x \in \mathbb{R}} |\hat{F}_n(x) - F(x)| \xrightarrow{\text{a.s.}} 0.
\]

This means that the empirical distribution function $\hat{F}_n(x)$ converges to the true distribution function $F(x)$ **uniformly** almost surely.

---

## **2. Interpretation and Importance**
This result is significant because it guarantees that the empirical distribution approximates the true distribution uniformly over all values of $x$ as the sample size $n \to \infty$. This uniform convergence is stronger than pointwise convergence (which follows from the weak law of large numbers).

The theorem forms the basis for:
- **Nonparametric statistics** (e.g., empirical process theory)
- **Goodness-of-fit tests** (e.g., Kolmogorov-Smirnov test)
- **Statistical learning theory**, where uniform convergence is crucial for proving generalization bounds.

---

## **3. Proof Sketch**
A rigorous proof relies on **Vapnik-Chervonenkis (VC) theory** and **Donsker's theorem**, but an intuitive approach follows these steps:

1. **Kolmogorov-Smirnov Inequality:** 
   Using the **Dvoretzky–Kiefer–Wolfowitz (DKW) inequality**, we bound the probability of large deviations:

   \[
   P\left( \sup_x |\hat{F}_n(x) - F(x)| > \epsilon \right) \leq 2e^{-2n\epsilon^2}.
   \]

   This ensures that deviations larger than $\epsilon$ decay exponentially with $n$.

2. **Borel-Cantelli Lemma:** 
   Applying Borel-Cantelli, we conclude that:

   \[
   \sup_x |\hat{F}_n(x) - F(x)| \to 0 \quad \text{almost surely}.
   \]

---

## **4. Extension: Uniform Law of Large Numbers (ULLN)**
A more general version of the theorem states that for any **Glivenko-Cantelli class** $\mathcal{F}$ of functions $f: \mathbb{R} \to \mathbb{R}$:

\[
\sup_{f \in \mathcal{F}} \left| \frac{1}{n} \sum_{i=1}^{n} f(X_i) - \mathbb{E}[f(X)] \right| \xrightarrow{\text{a.s.}} 0.
\]

This uniform convergence property is central to **empirical process theory** and **statistical learning**.

---

## **5. Rate of Convergence**
A stronger version of the theorem gives a **rate of convergence** using the DKW inequality:

\[
\sup_x |\hat{F}_n(x) - F(x)| = O\left(\sqrt{\frac{\log n}{n}}\right) \quad \text{with high probability}.
\]

For smoother distributions (e.g., absolutely continuous with a bounded density), convergence can be even faster.

---

## **6. Applications**
- **Kolmogorov-Smirnov Test**: Uses $\sup_x |\hat{F}_n(x) - F(x)|$ as a test statistic.
- **Empirical Process Theory**: Forms the foundation for extending LLN and CLT results to function classes.
- **Statistical Learning Theory**: Guarantees uniform convergence in empirical risk minimization.

Would you like me to expand on any of these aspects, such as the connection to Donsker's theorem or applications in machine learning?


---

preceding: [[empirical process theory]]  


following: [[rate of convergence in the glivenko-cantelli theorem via the dkw inequality]]---
date: 1717800988.901962
tags:
- autogenerated
- source__oai
- conversation_id__77e70e10-f02a-4f98-bd5c-6217b10122cf
- msg_aaa28306-75b0-4a73-aad9-ca9644639055
- msg_20c69179-365b-4e98-80d0-9007b435aabf
title: glivenko-cantelli theorem
---


**USER**

Glivenko-Cantelli theorem


**ASSISTANT**

The Glivenko-Cantelli Theorem is a fundamental result in probability theory and statistics, particularly in the theory of empirical processes. It asserts the uniform convergence of the empirical distribution function to the true distribution function.

### Statement of the Glivenko-Cantelli Theorem

Let $X_1, X_2, \ldots, X_n$ be i.i.d. random variables with common cumulative distribution function (CDF) $F$. The empirical distribution function $F_n$ is defined as:
$$ F_n(x) = \frac{1}{n} \sum_{i=1}^n \mathbf{1}_{(-\infty, x]}(X_i), $$
where $\mathbf{1}_{(-\infty, x]}$ is the indicator function, which is 1 if $X_i \leq x$ and 0 otherwise.

The Glivenko-Cantelli Theorem states that the empirical distribution function $F_n$ converges uniformly to the true distribution function $F$ almost surely as $n \to \infty$:
$$ \sup_{x \in \mathbb{R}} |F_n(x) - F(x)| \to 0 \quad \text{almost surely as} \quad n \to \infty. $$

### Proof Sketch

The proof of the Glivenko-Cantelli Theorem leverages the following key ideas:

1. **Pointwise Convergence**:
   By the Strong Law of Large Numbers, for any fixed $x \in \mathbb{R}$, $F_n(x)$ converges almost surely to $F(x)$.

2. **Uniform Convergence**:
   The challenge is to show that this convergence is uniform over all $x \in \mathbb{R}$. This can be achieved using techniques from [[empirical process theory]] and properties of the CDF.

### Steps in the Proof

1. **Donsker's Theorem**:
   Donsker's Theorem states that the empirical process $\sqrt{n}(F_n(x) - F(x))$ converges in distribution to a Brownian bridge $B(F(x))$:
   $$ \sqrt{n}(F_n(x) - F(x)) \rightsquiggle B(F(x)) \quad \text{in} \quad l^\infty(\mathbb{R}). $$

2. **Kolmogorov-Smirnov Statistic**:
   Consider the Kolmogorov-Smirnov statistic:
   $$ D_n = \sup_{x \in \mathbb{R}} |F_n(x) - F(x)|. $$
   We need to show that $D_n \to 0$ almost surely.

3. **Borel-Cantelli Lemma**:
   Using the Borel-Cantelli Lemma, one can show that the probability of $D_n$ exceeding a small threshold $\epsilon > 0$ infinitely often is zero. Specifically, we show:
   $$ P(D_n > \epsilon \text{ i.o.}) = 0. $$

4. **Entropy and Covering Numbers**:
   The concept of covering numbers can be used to handle the uniformity aspect. By covering the space with a finite number of intervals and using the pointwise convergence results, one can establish uniform convergence.

### Applications

#### 1. **Consistency of Estimators**

The Glivenko-Cantelli Theorem ensures that empirical distribution-based estimators, such as the empirical CDF, are consistent.

#### 2. **Nonparametric Statistics**

In nonparametric statistics, the theorem guarantees the consistency of methods based on empirical measures, such as the empirical CDF, histograms, and kernel density estimators.

#### 3. **Bootstrap Methods**

The theorem underpins the theoretical foundation of bootstrap methods, where the empirical distribution is used to approximate the sampling distribution of a statistic.

### Extensions and Generalizations

#### 1. **Uniform Glivenko-Cantelli Classes**

A class of functions $\mathcal{F}$ is called a Glivenko-Cantelli class if:
$$ \sup_{f \in \mathcal{F}} |P_n(f) - P(f)| \to 0 \quad \text{almost surely as} \quad n \to \infty, $$
where $P_n(f) = \frac{1}{n} \sum_{i=1}^n f(X_i)$ and $P(f) = E[f(X)]$. This generalizes the notion of uniform convergence to more complex function classes.

#### 2. **Multivariate Versions**

The Glivenko-Cantelli Theorem has been extended to multivariate settings, ensuring uniform convergence of empirical measures in higher dimensions.

### Further Reading

For a comprehensive study of the Glivenko-Cantelli Theorem and its implications, consider the following references:

- "Weak Convergence and Empirical Processes" by [[A.W. van der Vaart]] and [[J.A. Wellner]].
- "Probability and Statistics" by [[M. DeGroot]] and [[M. Schervish]].
- "Asymptotic Statistics" by [[A.W. van der Vaart]].

These texts provide detailed proofs, extensions, and applications of the Glivenko-Cantelli Theorem, offering a deep understanding of this fundamental result in probability and statistics.


---

preceding: [[large deviations theory]]  


following: [[donsker's theorem]]

See also: [[probability theory]]


See also: [[rate of convergence in the glivenko-cantelli theorem via the dkw inequality]]


See also: [[strong law of large numbers]]


See also: [[random variables]]


See also: [[empirical risk minimization]]