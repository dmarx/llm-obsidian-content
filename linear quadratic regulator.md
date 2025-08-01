---
date: 1717809987.876906
tags:
- autogenerated
- source__oai
- conversation_id__77e70e10-f02a-4f98-bd5c-6217b10122cf
- msg_aaa23186-9985-42af-a202-f49a677fe7c6
- msg_90771029-9ddd-4aeb-9f49-8c8e03207363
- colorclass/system-dynamics
title: linear quadratic regulator
---

**USER**

Linear Quadratic Regulator


**ASSISTANT**

The Linear Quadratic Regulator (LQR) is a fundamental method in [[optimal control theory]] that provides a systematic way to design controllers for linear dynamical systems. The LQR problem involves finding a control law that minimizes a quadratic cost function over a given time horizon. This method is widely used in various engineering applications due to its simplicity and robustness.

### Problem Formulation

Consider a linear time-invariant system described by the state-space equations:
\[ \dot{\mathbf{x}}(t) = A\mathbf{x}(t) + B\mathbf{u}(t), \]
where:
- \(\mathbf{x}(t) \in \mathbb{R}^n\) is the state vector at time \(t\),
- \(\mathbf{u}(t) \in \mathbb{R}^m\) is the control input vector at time \(t\),
- \(A \in \mathbb{R}^{n \times n}\) is the system matrix,
- \(B \in \mathbb{R}^{n \times m}\) is the input matrix.

The objective is to find a control input \(\mathbf{u}(t)\) that minimizes the following quadratic cost function:
\[ J = \int_{0}^{\infty} \left( \mathbf{x}(t)^T Q \mathbf{x}(t) + \mathbf{u}(t)^T R \mathbf{u}(t) \right) dt, \]
where:
- \(Q \in \mathbb{R}^{n \times n}\) is a symmetric positive semi-definite matrix (state weighting matrix),
- \(R \in \mathbb{R}^{m \times m}\) is a symmetric positive definite matrix (control weighting matrix).

### Optimal Control Law

The optimal control law for the LQR problem is given by a state feedback law:
\[ \mathbf{u}^*(t) = -K \mathbf{x}(t), \]
where \(K\) is the optimal feedback gain matrix. This gain matrix \(K\) is derived from the solution to the Algebraic Riccati Equation (ARE).

### Algebraic Riccati Equation

The ARE is given by:
\[ A^T P + P A - P B R^{-1} B^T P + Q = 0, \]
where \(P\) is a symmetric positive semi-definite matrix. The solution \(P\) to this equation is used to compute the optimal feedback gain matrix:
\[ K = R^{-1} B^T P. \]

### Properties of the LQR

1. **Stability**: The LQR controller guarantees the closed-loop system \( \dot{\mathbf{x}}(t) = (A - BK) \mathbf{x}(t) \) is stable if \(Q\) and \(R\) are chosen appropriately.
2. **Optimality**: The control law minimizes the given quadratic cost function, ensuring optimal performance according to the defined criteria.
3. **Robustness**: The LQR controller is known for its robustness to certain types of model uncertainties and disturbances.

### Solving the LQR Problem

To solve the LQR problem, we typically follow these steps:

1. **Formulate the ARE**: Write down the Algebraic Riccati Equation corresponding to the system matrices \(A\), \(B\) and the weighting matrices \(Q\), \(R\).
2. **Solve the ARE**: Use numerical methods or software tools to solve the ARE for the matrix \(P\).
3. **Compute the Feedback Gain**: Calculate the optimal feedback gain matrix \(K\) using \( K = R^{-1} B^T P \).

### Example

Consider a simple system with:
\[ A = \begin{bmatrix} 0 & 1 \\ 0 & -1 \end{bmatrix}, \quad B = \begin{bmatrix} 0 \\ 1 \end{bmatrix}, \quad Q = \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix}, \quad R = 1. \]

1. **Formulate the ARE**:
   \[ A^T P + P A - P B R^{-1} B^T P + Q = 0. \]

2. **Solve the ARE**: Assume \( P = \begin{bmatrix} p_{11} & p_{12} \\ p_{12} & p_{22} \end{bmatrix} \). Substituting into the ARE and solving for the elements of \(P\), we get:
   \[
   \begin{bmatrix} 0 & 0 \\ 0 & -2 \end{bmatrix} + \begin{bmatrix} p_{11} & p_{12} \\ p_{12} & p_{22} \end{bmatrix} \begin{bmatrix} 0 & 1 \\ 0 & -1 \end{bmatrix} + \begin{bmatrix} 0 & 1 \\ 0 & -1 \end{bmatrix} \begin{bmatrix} p_{11} & p_{12} \\ p_{12} & p_{22} \end{bmatrix} - \begin{bmatrix} 0 & p_{12} \\ p_{12} & p_{22} \end{bmatrix} + \begin{bmatrix} 1 & 0 \\ 0 & 1 \end{bmatrix} = 0.
   \]

   Solving this set of equations will give the values for \(p_{11}\), \(p_{12}\), and \(p_{22}\).

3. **Compute the Feedback Gain**: 
   \[
   K = R^{-1} B^T P = \begin{bmatrix} 0 & 1 \end{bmatrix} \begin{bmatrix} p_{11} & p_{12} \\ p_{12} & p_{22} \end{bmatrix}.
   \]

### Practical Implementation

In practice, solving the LQR problem often involves using numerical solvers available in control libraries, such as MATLAB, SciPy in Python, or other specialized software. Here's a simple example using Python and SciPy:

```python
import numpy as np
from scipy.linalg import solve_continuous_are
from scipy.linalg import inv

# Define system matrices
A = np.array([[0, 1],
              [0, -1]])
B = np.array([[0],
              [1]])
Q = np.array([[1, 0],
              [0, 1]])
R = np.array([[1]])

# Solve the continuous-time Algebraic Riccati Equation (ARE)
P = solve_continuous_are(A, B, Q, R)

# Compute the LQR gain
K = inv(R).dot(B.T).dot(P)

print("Optimal gain matrix K:")
print(K)
```

### Conclusion

The Linear Quadratic Regulator (LQR) is a powerful method for designing optimal controllers for linear systems with quadratic cost functions. By solving the Algebraic Riccati Equation, one can determine the optimal feedback gain that minimizes the cost function while ensuring stability and robustness. LQR is widely used in various applications due to its effectiveness and relatively straightforward implementation.


---

preceding: [[hamilton-jacobi-bellman equation]]  


following: [[gain matrix]]

See also: [[linear quadratic regulator (lqr)]]


See also: [[dynamics and control of mechanical systems]]


See also: [[vibration analysis]]


See also: [[control theory]]