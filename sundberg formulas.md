---
date: 1717805613.003956
tags:
- autogenerated
- source__oai
- conversation_id__77e70e10-f02a-4f98-bd5c-6217b10122cf
- msg_aaa2704c-7e0e-493c-95c9-f4a17c945755
- msg_974a9359-d393-48f5-8977-3be1d9a4ce52
- colorclass/information-theory
title: sundberg formulas
---

**USER**

the sundberg formulas


**ASSISTANT**

The Sundberg formulas are important in the context of the multivariate delta method, particularly for obtaining higher-order moments of a function of random variables. These formulas provide a way to approximate the mean and covariance matrix of a nonlinear function of a vector of random variables.

### Context and Motivation

When dealing with a random vector \(\mathbf{X} = (X_1, X_2, \ldots, X_p)^\top\) and a smooth function \(g: \mathbb{R}^p \to \mathbb{R}^q\), it is often useful to approximate the distribution of \(g(\mathbf{X})\). If \(\mathbf{X}\) is approximately multivariate normal with mean vector \(\mathbf{\mu}\) and covariance matrix \(\Sigma\), the delta method gives first-order approximations. Sundberg's formulas extend this by providing second-order approximations.

### Sundberg's Formulas

Given a multivariate random vector \(\mathbf{X} \sim N_p(\mathbf{\mu}, \Sigma)\) and a twice continuously differentiable function \(g: \mathbb{R}^p \to \mathbb{R}^q\), the Sundberg formulas help approximate the mean vector \(E[g(\mathbf{X})]\) and the covariance matrix \(\text{Cov}(g(\mathbf{X}))\).

#### First-Order Approximation

The first-order approximation (the multivariate delta method) for the mean vector is:
\[ E[g(\mathbf{X})] \approx g(\mathbf{\mu}). \]

#### Second-Order Approximation

The second-order approximation for the mean vector is:
\[ E[g(\mathbf{X})] \approx g(\mathbf{\mu}) + \frac{1}{2} \sum_{i=1}^p \sum_{j=1}^p \frac{\partial^2 g}{\partial x_i \partial x_j} (\mathbf{\mu}) \Sigma_{ij}. \]

For the covariance matrix, the second-order approximation is:
\[ \text{Cov}(g(\mathbf{X})) \approx J_g(\mathbf{\mu}) \Sigma J_g(\mathbf{\mu})^\top + \frac{1}{2} \sum_{i=1}^p \sum_{j=1}^p \frac{\partial^2 g}{\partial x_i \partial x_j} (\mathbf{\mu}) \Sigma_{ij} \left[ \frac{\partial^2 g}{\partial x_i \partial x_j} (\mathbf{\mu}) \right]^\top, \]
where \( J_g(\mathbf{\mu}) \) is the Jacobian matrix of \(g\) evaluated at \(\mathbf{\mu}\):
\[ J_g(\mathbf{\mu}) = \left( \frac{\partial g}{\partial x_1}(\mathbf{\mu}), \frac{\partial g}{\partial x_2}(\mathbf{\mu}), \ldots, \frac{\partial g}{\partial x_p}(\mathbf{\mu}) \right). \]

### Detailed Components

#### Jacobian Matrix

The Jacobian matrix \( J_g(\mathbf{\mu}) \) of a function \( g \) at \(\mathbf{\mu}\) is a \(q \times p\) matrix containing the first partial derivatives of \(g\):
\[ J_g(\mathbf{\mu}) = \begin{bmatrix}
\frac{\partial g_1}{\partial x_1}(\mathbf{\mu}) & \frac{\partial g_1}{\partial x_2}(\mathbf{\mu}) & \cdots & \frac{\partial g_1}{\partial x_p}(\mathbf{\mu}) \\
\frac{\partial g_2}{\partial x_1}(\mathbf{\mu}) & \frac{\partial g_2}{\partial x_2}(\mathbf{\mu}) & \cdots & \frac{\partial g_2}{\partial x_p}(\mathbf{\mu}) \\
\vdots & \vdots & \ddots & \vdots \\
\frac{\partial g_q}{\partial x_1}(\mathbf{\mu}) & \frac{\partial g_q}{\partial x_2}(\mathbf{\mu}) & \cdots & \frac{\partial g_q}{\partial x_p}(\mathbf{\mu})
\end{bmatrix}. \]

#### Second-Order Partial Derivatives

The second-order partial derivatives of \(g\) evaluated at \(\mathbf{\mu}\) are used in the correction terms for both the mean and the covariance matrix. For a scalar function \(g\) (i.e., \(q=1\)), the term \(\frac{\partial^2 g}{\partial x_i \partial x_j} (\mathbf{\mu})\) is a scalar, and for a vector-valued function \(g\), it becomes a matrix of appropriate dimensions.

### Example

Consider a simple example where \( g: \mathbb{R}^2 \to \mathbb{R} \) is defined by \( g(\mathbf{X}) = X_1^2 + X_2^2 \). Let \(\mathbf{X} \sim N_2(\mathbf{\mu}, \Sigma)\), where \(\mathbf{\mu} = (\mu_1, \mu_2)^\top\) and
\[ \Sigma = \begin{bmatrix}
\sigma_{11} & \sigma_{12} \\
\sigma_{12} & \sigma_{22}
\end{bmatrix}. \]

First, calculate the first-order approximation for the mean:
\[ E[g(\mathbf{X})] \approx g(\mathbf{\mu}) = \mu_1^2 + \mu_2^2. \]

Next, apply the second-order approximation for the mean:
\[ \frac{\partial^2 g}{\partial x_1^2} = 2, \quad \frac{\partial^2 g}{\partial x_2^2} = 2, \quad \frac{\partial^2 g}{\partial x_1 \partial x_2} = 0. \]
Thus,
\[ E[g(\mathbf{X})] \approx \mu_1^2 + \mu_2^2 + \frac{1}{2} (2 \sigma_{11} + 2 \sigma_{22}) = \mu_1^2 + \mu_2^2 + \sigma_{11} + \sigma_{22}. \]

For the covariance matrix, since \( g(\mathbf{X}) \) is scalar-valued (\(q=1\)), the covariance matrix reduces to the variance:
\[ \text{Var}(g(\mathbf{X})) \approx J_g(\mathbf{\mu}) \Sigma J_g(\mathbf{\mu})^\top + \frac{1}{2} \sum_{i=1}^2 \sum_{j=1}^2 \frac{\partial^2 g}{\partial x_i \partial x_j}(\mathbf{\mu}) \Sigma_{ij} \left( \frac{\partial^2 g}{\partial x_i \partial x_j}(\mathbf{\mu}) \right). \]

Since
\[ J_g(\mathbf{\mu}) = \begin{bmatrix}
2\mu_1 & 2\mu_2
\end{bmatrix}, \]
we have
\[ J_g(\mathbf{\mu}) \Sigma J_g(\mathbf{\mu})^\top = 4 (\mu_1^2 \sigma_{11} + 2\mu_1\mu_2 \sigma_{12} + \mu_2^2 \sigma_{22}). \]

The second-order term is
\[ \frac{1}{2} \left( 2\sigma_{11} \cdot 2 + 2\sigma_{22} \cdot 2 \right) = 2\sigma_{11} + 2\sigma_{22}. \]

Thus,
\[ \text{Var}(g(\mathbf{X})) \approx 4 (\mu_1^2 \sigma_{11} + 2\mu_1\mu_2 \sigma_{12} + \mu_2^2 \sigma_{22}) + 2\sigma_{11} + 2\sigma_{22}. \]

### Conclusion

Sundberg's formulas extend the delta method to provide higher-order approximations for the mean and covariance of a function of random variables. These approximations are particularly useful when dealing with nonlinear transformations and when higher-order accuracy is required.

### Further Reading

For more details on Sundberg's formulas and their applications, consider exploring the following references:

- "Asymptotic Statistics" by A. W. van der Vaart.
- "The Delta Method and Its Extensions" by Kai-Tai Fang and Samuel Kotz in the book "Multivariate Analysis: Future Directions" edited by C. R. Rao.
- "Elements of Large-Sample Theory" by E. L. Lehmann.


---

preceding: [[martingale central limit theorem]]  


following: [[expectation maximization]]

See also: [[partial derivatives]]


See also: [[random variables]]