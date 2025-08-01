---
date: 1714499411.625676
tags:
- autogenerated
- source__oai
- conversation_id__de32c34b-d1de-471e-8a15-a68b9a9862a8
- msg_aaa239c7-e117-41e8-92eb-fccc4ca5e0cc
- msg_815f94cb-de1d-4f9b-96b3-8b53ac43fe0a
title: laplace approximation
---


**USER**

laplace approximation


**ASSISTANT**

The [[Laplace Approximation]] is a method used in statistics to approximate complex integrals of probability distributions, especially when the dimensionality of the integral makes exact calculation infeasible. This approximation technique is highly relevant in the context of Bayesian statistics for approximating posterior distributions. It hinges on using a second-order Taylor expansion of the logarithm of the density around its mode.

### Mathematical Background

Consider a probability density function $p(\theta)$ which can be hard to integrate directly, particularly in the Bayesian framework where the posterior distributions become complex. The Laplace approximation provides a way to approximate this integral by assuming the log of the density, $\log p(\theta)$, is well-approximated by a Gaussian density around its mode $\hat{\theta}$. 

The mode $\hat{\theta}$ is the value of $\theta$ that maximizes the log density, i.e.,

$$
\hat{\theta} = \arg \max_{\theta} \log p(\theta).
$$

### Taylor Expansion

To apply the Laplace approximation, expand $\log p(\theta)$ in a Taylor series around $\hat{\theta}$ up to the second order:

$$
\log p(\theta) \approx \log p(\hat{\theta}) + \frac{1}{2} (\theta - \hat{\theta})^\top H (\theta - \hat{\theta}),
$$

where $H$ is the Hessian matrix of second derivatives of $\log p(\theta)$ evaluated at $\hat{\theta}$. Assuming $H$ is negative definite (as expected at a maximum), the matrix $-H$ is positive definite.

### Gaussian Approximation

This approximation suggests that near its mode, the distribution $p(\theta)$ can be approximated by a Gaussian distribution with mean $\hat{\theta}$ and covariance matrix given by the inverse of the negative Hessian:

$$
q(\theta) = \mathcal{N}(\theta | \hat{\theta}, (-H)^{-1}).
$$

### Use in Bayesian Statistics

In Bayesian inference, you often need to compute integrals of the form:

$$
\int f(\theta) p(\theta | data) \, d\theta
$$

where $p(\theta | data)$ is the posterior distribution. Using Laplace's approximation, the integral can be approximated as:

$$
\int f(\theta) \mathcal{N}(\theta | \hat{\theta}, (-H)^{-1}) \, d\theta.
$$

### Advantages and Limitations

**Advantages**:
- Provides a straightforward computational technique that only requires the calculation of a mode and a Hessian.
- Useful for high-dimensional problems where numerical integration would be otherwise intractable.

**Limitations**:
- The accuracy depends on the unimodality and symmetry of the log density around the mode.
- It might not perform well if the true posterior is multi-modal or highly skewed.

### Conclusion

The [[Laplace Approximation]] is an essential tool in the applied mathematician's arsenal, especially useful in the field of Bayesian inference, where the direct calculation of posteriors and related expectations might otherwise be prohibitive due to the complexity or dimensionality of the model.


---


following: [[generalized gauss-newton matrix]]