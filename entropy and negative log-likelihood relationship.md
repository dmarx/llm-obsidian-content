---
date: '2025-05-22T01:44:05.230011Z'
tags:
- autogenerated
- source__claude
- conversation_id__aaf8b1a1-aac7-4fed-af23-cacc3cc02b59
- msg_504d19b0-77b9-4ad1-a4fe-eb165f1b9206
- msg_7f875065-5656-4599-a0d2-4afd5669f786
title: entropy and negative log-likelihood relationship
---


**USER**

relate entropy of a random variable to nll


**ASSISTANT**

# Entropy and Negative Log-Likelihood Relationship

## Fundamental Connection

The [[entropy]] of a discrete random variable $X$ with probability mass function $p(x)$ is defined as:

$$H(X) = -\sum_{x \in \mathcal{X}} p(x) \log p(x) = \mathbb{E}[-\log p(X)]$$

The [[negative log-likelihood]] (NLL) for a single observation $x$ drawn from distribution $p$ is:

$$\text{NLL}(x) = -\log p(x)$$

## Mathematical Relationship

The entropy is precisely the **expected negative log-likelihood** under the true distribution:

$$H(X) = \mathbb{E}_{X \sim p}[\text{NLL}(X)] = \mathbb{E}_{X \sim p}[-\log p(X)]$$

### Cross-Entropy Generalization

For distributions $p$ (true) and $q$ (model), the [[cross-entropy]] extends this relationship:

$$H(p,q) = -\sum_{x} p(x) \log q(x) = \mathbb{E}_{X \sim p}[-\log q(X)]$$

The cross-entropy represents the expected NLL when:
- Data is sampled from distribution $p$
- Model assigns probabilities according to distribution $q$

## Information-Theoretic Interpretation

### Optimal Coding Length

Under [[Shannon's source coding theorem]], entropy represents the minimum expected [[code length]] for optimal compression. The NLL $-\log p(x)$ gives the optimal code length for symbol $x$ under distribution $p$.

Let $\ell(x)$ denote the code length assigned to symbol $x$. For optimal coding:

$$\ell^*(x) = -\log_2 p(x) \text{ bits}$$

The expected code length equals entropy:

$$\mathbb{E}[\ell^*(X)] = H(X)$$

### Surprise and Information Content

The NLL quantifies the [[surprisal]] or [[self-information]] of an observation:

$$I(x) = -\log p(x)$$

Entropy is the expected surprisal:

$$H(X) = \mathbb{E}[I(X)]$$

## Machine Learning Applications

### Maximum Likelihood Estimation

For i.i.d. samples $\{x_1, \ldots, x_n\}$, the [[empirical entropy]] approximates true entropy:

$$\hat{H}_n = -\frac{1}{n}\sum_{i=1}^n \log p(x_i)$$

This is equivalent to the average NLL over the training set.

### Loss Function Perspective

In classification with [[categorical cross-entropy loss]]:

$$\mathcal{L}(\theta) = -\frac{1}{n}\sum_{i=1}^n \sum_{k=1}^K y_{i,k} \log q_\theta(k|x_i)$$

where $y_{i,k}$ are one-hot labels and $q_\theta$ is the model distribution.

The loss equals the cross-entropy between empirical label distribution and model predictions.

## Continuous Case

For continuous random variable $X$ with density $f(x)$, the [[differential entropy]] is:

$$h(X) = -\int f(x) \log f(x) \, dx = \mathbb{E}[-\log f(X)]$$

The relationship with NLL remains: differential entropy equals expected NLL under the true density.

## Symbolic Notation

Let $\mathbf{S}(p)$ denote the entropy operator and $\mathbf{L}(x;p)$ the NLL operator:

$$\mathbf{S}(p) = \mathbb{E}_{X \sim p}[\mathbf{L}(X;p)]$$

For cross-entropy:

$$\mathbf{S}(p,q) = \mathbb{E}_{X \sim p}[\mathbf{L}(X;q)]$$

The [[Kullback-Leibler divergence]] decomposes as:

$$D_{KL}(p \parallel q) = \mathbf{S}(p,q) - \mathbf{S}(p)$$

This fundamental relationship underlies the optimization of probabilistic models through NLL minimization, which implicitly minimizes the cross-entropy between data and model distributions.