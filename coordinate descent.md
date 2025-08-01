---
date: 1717810985.356174
tags:
- autogenerated
- source__oai
- conversation_id__77e70e10-f02a-4f98-bd5c-6217b10122cf
- msg_aaa2d1b5-1eca-45db-8437-a0c9a63cb093
- msg_bddc2c6b-0f71-4987-8708-7f22a587b634
- colorclass/game-theory
title: coordinate descent
---

**USER**

coordinate descent


**ASSISTANT**

Coordinate descent is an optimization algorithm that is particularly useful for solving large-scale optimization problems. It works by optimizing a single coordinate (or a subset of coordinates) of the decision variable at a time, while keeping the other coordinates fixed. This process is repeated iteratively for each coordinate until convergence.

### Basic Idea

Consider a general optimization problem of the form:
\[ \min_{\mathbf{x} \in \mathbb{R}^n} f(\mathbf{x}), \]
where \( f: \mathbb{R}^n \to \mathbb{R} \) is the objective function to be minimized, and \( \mathbf{x} = (x_1, x_2, \ldots, x_n) \) is the decision variable vector.

In coordinate descent, the optimization problem is broken down into a sequence of simpler problems, each involving only a single coordinate or a block of coordinates.

### Algorithm

1. **Initialization**: Start with an initial guess \(\mathbf{x}^0\).
2. **Iterative Update**:
   - For each coordinate \( i = 1, 2, \ldots, n \):
     \[
     x_i^{k+1} = \arg\min_{x_i} f(x_1^k, \ldots, x_{i-1}^k, x_i, x_{i+1}^k, \ldots, x_n^k).
     \]
   - Update the coordinate \( x_i \) while keeping all other coordinates fixed.
3. **Convergence Check**: Check for convergence, typically by monitoring the change in the objective function or the norm of the gradient. If the stopping criterion is not met, repeat the iterative update.

### Properties

1. **Convergence**: Coordinate descent algorithms often converge to a local minimum, especially when \( f \) is convex. For strictly convex functions, coordinate descent converges to the global minimum.
2. **Scalability**: Coordinate descent is particularly effective for large-scale problems since each step involves solving a lower-dimensional optimization problem.
3. **Simplicity**: The algorithm is simple to implement and can be applied to a wide range of optimization problems.

### Variants

1. **Gauss-Seidel Coordinate Descent**: This version updates the coordinates sequentially, i.e., one after the other in a fixed order.
2. **Gauss-Southwell Rule**: In this variant, the coordinate with the largest gradient (or largest change in the objective function) is updated.
3. **Randomized Coordinate Descent**: Coordinates are selected randomly for updates. This variant can sometimes lead to faster convergence, especially for high-dimensional problems.
4. **Block Coordinate Descent**: Instead of updating one coordinate at a time, a block (subset) of coordinates is updated simultaneously. This can be useful for problems with a naturally block-structured objective function.

### Example: Lasso Regression

Lasso regression is a common application of coordinate descent. The optimization problem for Lasso is:
\[ \min_{\mathbf{w}} \frac{1}{2} \|\mathbf{y} - \mathbf{X} \mathbf{w}\|_2^2 + \lambda \|\mathbf{w}\|_1, \]
where \( \mathbf{y} \) is the response vector, \( \mathbf{X} \) is the design matrix, \( \mathbf{w} \) is the vector of coefficients, and \( \lambda \) is the regularization parameter.

Coordinate descent for Lasso regression involves iteratively solving the optimization problem for each coefficient \( w_j \):
\[ w_j^{k+1} = S\left(\frac{(\mathbf{y} - \mathbf{X}_{-j} \mathbf{w}_{-j})^T \mathbf{x}_j}{n}, \lambda \right), \]
where \( \mathbf{X}_{-j} \) and \( \mathbf{w}_{-j} \) denote the design matrix and coefficient vector excluding the \( j \)-th feature, \( \mathbf{x}_j \) is the \( j \)-th feature, and \( S \) is the soft-thresholding operator.

### Example Implementation in Python

Here's a simple implementation of coordinate descent for Lasso regression in Python:

```python
import numpy as np

def soft_thresholding(rho, lambda_):
    if rho < -lambda_:
        return (rho + lambda_)
    elif rho > lambda_:
        return (rho - lambda_)
    else:
        return 0

def coordinate_descent_lasso(X, y, lambda_, num_iters=100, tol=1e-6):
    m, n = X.shape
    w = np.zeros(n)
    X_transpose = X.T
    for _ in range(num_iters):
        w_old = np.copy(w)
        for j in range(n):
            residual = y - X @ w + X[:, j] * w[j]
            rho = X[:, j] @ residual
            w[j] = soft_thresholding(rho, lambda_)
        if np.sum(np.abs(w - w_old)) < tol:
            break
    return w

# Example usage:
np.random.seed(0)
X = np.random.randn(100, 10)
y = X @ np.random.randn(10) + np.random.randn(100)
lambda_ = 0.1
w = coordinate_descent_lasso(X, y, lambda_)
print("Coefficients:", w)
```

### Summary

Coordinate descent is a powerful optimization method, especially useful for large-scale and high-dimensional problems. Its simplicity and efficiency make it suitable for various applications, including Lasso regression, matrix factorization, and other machine learning tasks. The method's flexibility allows for different variants to be applied depending on the problem structure and requirements.


---

preceding: [[fundamental results in the theory of optimal control in decentralized systems]]  


following: [[mean field game theory]]

See also: [[gibbs sampling]]


See also: [[relate gibbs sampling to coordinate descent]]


See also: [[gelman-rubin statistic]]


See also: [[significant works of nesterov]]


See also: [[game theory]]


See also: [[nesterov momentum doesn't make the list]]