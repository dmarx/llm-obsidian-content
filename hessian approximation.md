---
date: 1717808906.698096
tags:
- autogenerated
- source__oai
- conversation_id__77e70e10-f02a-4f98-bd5c-6217b10122cf
- msg_aaa2c78b-af24-44cd-9cac-ffe781e46272
- msg_7511397f-4eef-4893-ab84-0f8809b768b9
- colorclass/system-dynamics
title: hessian approximation
---

**USER**

Hessian approximation


**ASSISTANT**

In optimization, the Hessian matrix provides second-order information about a function, capturing the curvature of the function. However, computing the exact Hessian can be computationally expensive, especially for large-scale problems. Quasi-Newton methods approximate the Hessian to achieve a balance between computational efficiency and the benefits of using second-order information.

### Key Quasi-Newton Methods for Hessian Approximation

1. **BFGS (Broyden-Fletcher-Goldfarb-Shanno) Method**
2. **DFP (Davidon-Fletcher-Powell) Method**
3. **L-BFGS (Limited-memory BFGS) Method**

### 1. BFGS Method

The BFGS method is one of the most widely used quasi-Newton methods. It updates an approximation \(B_k\) of the inverse Hessian matrix \(H_f(x_k)^{-1}\) using gradient information.

#### BFGS Update Formula

Given:
- Current and previous iterates \(x_{k+1}\) and \(x_k\)
- Gradient at current and previous iterates \(g_{k+1}\) and \(g_k\)
- \(s_k = x_{k+1} - x_k\)
- \(y_k = g_{k+1} - g_k\)

The BFGS update for the inverse Hessian approximation \(B_{k+1}\) is:
\[ B_{k+1} = \left(I - \frac{s_k y_k^T}{y_k^T s_k}\right) B_k \left(I - \frac{y_k s_k^T}{y_k^T s_k}\right) + \frac{s_k s_k^T}{y_k^T s_k} \]

### 2. DFP Method

The DFP method is another quasi-Newton method, named after its developers. It updates the Hessian approximation directly rather than its inverse.

#### DFP Update Formula

Given the same \(s_k\) and \(y_k\) as above, the DFP update for the Hessian approximation \(H_{k+1}\) is:
\[ H_{k+1} = H_k + \frac{y_k y_k^T}{y_k^T s_k} - \frac{H_k s_k s_k^T H_k}{s_k^T H_k s_k} \]

### 3. L-BFGS Method

The Limited-memory BFGS (L-BFGS) method is designed for large-scale optimization problems where storing the full Hessian approximation is impractical. L-BFGS maintains a limited number of updates and implicitly constructs the Hessian approximation.

#### L-BFGS Algorithm

1. **Initialization**: Initialize \(x_0\) and set the memory parameter \(m\) (number of correction pairs to store). Initialize the gradient \(g_0\) and \(H_0 = I\) (identity matrix).
2. **Storage**: Store the last \(m\) pairs \((s_i, y_i)\).
3. **Two-loop recursion**: Compute the search direction \(p_k\) using:
   - First loop: 
     \[
     \alpha_i = \frac{\rho_i s_i^T q}{y_i^T s_i}
     \]
     \[
     q = q - \alpha_i y_i
     \]
   - Second loop:
     \[
     \beta_i = \frac{\rho_i y_i^T r}{y_i^T s_i}
     \]
     \[
     r = r + s_i (\alpha_i - \beta_i)
     \]
4. **Update step**:
   \[
   x_{k+1} = x_k - \alpha_k r
   \]

### Properties and Practical Considerations

- **Symmetry and Positive Definiteness**: Both BFGS and DFP updates maintain the symmetry and positive definiteness of the Hessian approximation.
- **Superlinear Convergence**: Quasi-Newton methods exhibit superlinear convergence under appropriate conditions, meaning that the rate of convergence accelerates as it approaches the solution.
- **Memory Efficiency**: L-BFGS is particularly suited for large-scale problems due to its limited memory requirements.

### Example Implementation of BFGS in Python

Here is a simple implementation of the BFGS method in Python:

```python
import numpy as np

def bfgs_update(B, s, y):
    Bs = B @ s
    sT_y = np.dot(s.T, y)
    if sT_y == 0:
        return B  # To avoid division by zero
    term1 = np.outer(y, y) / sT_y
    term2 = np.outer(Bs, Bs) / np.dot(s.T, Bs)
    return B + term1 - term2

def bfgs_method(f, grad, x0, tol=1e-5, max_iter=100):
    x = x0
    B = np.eye(len(x0))  # Initial approximation of the inverse Hessian
    for i in range(max_iter):
        g = grad(x)
        p = -B @ g
        alpha = line_search(f, grad, x, p)
        s = alpha * p
        x_new = x + s
        g_new = grad(x_new)
        y = g_new - g
        B = bfgs_update(B, s, y)
        x = x_new
        if np.linalg.norm(g_new) < tol:
            break
    return x

def line_search(f, grad, x, p, alpha=1, c1=1e-4, rho=0.9):
    while f(x + alpha * p) > f(x) + c1 * alpha * np.dot(grad(x).T, p):
        alpha *= rho
    return alpha

# Example usage:
def f(x):
    return (x[0] - 2)**2 + (x[1] - 3)**2

def grad_f(x):
    return np.array([2 * (x[0] - 2), 2 * (x[1] - 3)])

x0 = np.array([0.0, 0.0])
result = bfgs_method(f, grad_f, x0)
print("Optimized parameters:", result)
```

### Conclusion

Quasi-Newton methods are powerful optimization techniques that approximate the Hessian matrix, making them suitable for large-scale problems. Methods like BFGS and L-BFGS balance computational efficiency and the use of second-order information, providing robust and rapid convergence. Understanding and implementing these methods can significantly enhance the performance of optimization tasks in various applications.


---

preceding: [[quasi-newton methods]]  


following: [[optimal control theory]]

See also: [[control theory]]