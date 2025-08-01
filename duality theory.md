---
date: 1721688087.174173
tags:
- autogenerated
- source__oai
- conversation_id__a2d4a2dc-4888-4b9b-aa34-ef6394b04fb7
- msg_aaa28825-c8c2-4c95-92b2-5dd8368c974e
- msg_521c93ad-5a21-49f1-8a41-8b988515ed49
- colorclass/information-theory
title: duality theory
---

**USER**

duality theory


**ASSISTANT**

## Duality Theory

### Overview

Duality theory is a fundamental concept in optimization that establishes a relationship between a given optimization problem (the primal problem) and another related problem (the dual problem). The solutions to these problems provide valuable insights into the properties of the original problem, and in many cases, solving the dual problem is easier or more informative than solving the primal problem directly.

### Primal and Dual Problems

#### Primal Problem

Consider a general optimization problem (the primal problem) in the form:

$$
\min_{x \in \mathcal{X}} f(x),
$$

subject to constraints \(g_i(x) \leq 0\) for \(i = 1, \ldots, m\), and \(h_j(x) = 0\) for \(j = 1, \ldots, p\). Here, \(f(x)\) is the objective function, \(\mathcal{X}\) is the feasible region defined by the constraints, and \(x\) is the vector of decision variables.

#### Lagrangian Function

The Lagrangian function \(L(x, \lambda, \nu)\) combines the objective function and the constraints using Lagrange multipliers (dual variables) \(\lambda\) and \(\nu\):

$$
L(x, \lambda, \nu) = f(x) + \sum_{i=1}^m \lambda_i g_i(x) + \sum_{j=1}^p \nu_j h_j(x),
```

where \(\lambda_i \geq 0\) for all \(i\).

#### Dual Problem

The dual problem is derived by considering the infimum of the Lagrangian function with respect to the primal variables \(x\):

$$
\inf_{x \in \mathcal{X}} L(x, \lambda, \nu).
$$

The resulting function, known as the dual function \(g(\lambda, \nu)\), is given by:

$$
g(\lambda, \nu) = \inf_{x \in \mathcal{X}} \left[ f(x) + \sum_{i=1}^m \lambda_i g_i(x) + \sum_{j=1}^p \nu_j h_j(x) \right].
```

The dual problem is then formulated as a maximization problem:

$$
\max_{\lambda \geq 0, \nu} g(\lambda, \nu).
```

### Weak and Strong Duality

#### Weak Duality

Weak duality states that the optimal value of the dual problem provides a lower bound on the optimal value of the primal problem. Specifically, if \(x^*\) is a feasible solution to the primal problem and \((\lambda^*, \nu^*)\) is a feasible solution to the dual problem, then:

$$
f(x^*) \geq g(\lambda^*, \nu^*).
```

#### Strong Duality

Strong duality holds when the optimal values of the primal and dual problems are equal. This means that if \(x^*\) is an optimal solution to the primal problem and \((\lambda^*, \nu^*)\) is an optimal solution to the dual problem, then:

$$
f(x^*) = g(\lambda^*, \nu^*).
```

Strong duality does not always hold, but it is guaranteed under certain conditions, such as convexity of the primal problem and satisfaction of constraint qualifications (e.g., Slater's condition).

### Examples

#### Example 1: Linear Programming

Consider the linear programming (LP) problem:

**Primal Problem:**

$$
\min_{x} \, c^T x \\
\text{subject to} \\
Ax \leq b \\
x \geq 0,
```

where \(c \in \mathbb{R}^n\), \(A \in \mathbb{R}^{m \times n}\), and \(b \in \mathbb{R}^m\).

**Dual Problem:**

$$
\max_{y} \, b^T y \\
\text{subject to} \\
A^T y \leq c \\
y \geq 0,
```

where \(y \in \mathbb{R}^m\) are the dual variables.

In linear programming, strong duality always holds, meaning the optimal values of the primal and dual problems are equal.

#### Example 2: Quadratic Programming

Consider the quadratic programming (QP) problem:

**Primal Problem:**

$$
\min_{x} \, \frac{1}{2} x^T Q x + c^T x \\
\text{subject to} \\
Ax \leq b,
```

where \(Q \in \mathbb{R}^{n \times n}\) is a symmetric positive definite matrix.

**Dual Problem:**

The dual problem for a QP can be derived similarly to the LP case, leading to another QP involving the dual variables.

### Applications

#### Economics

In economics, duality theory is used to analyze consumer behavior, production optimization, and cost minimization. The dual variables often have economic interpretations, such as shadow prices or marginal costs.

#### Engineering

In engineering, duality theory is applied to solve optimization problems in control systems, signal processing, and network design. It helps in designing efficient algorithms for resource allocation and system optimization.

#### Machine Learning

In machine learning, duality theory is used in support vector machines (SVMs) and other optimization-based learning algorithms. The dual problem formulation often leads to more efficient algorithms for training and inference.

### Further Reading

- [[Convex Optimization]]
- [[Large Deviations Theory]]
- [[Gartner-Ellis Theorem]]
- [[Cramér's Theorem]]
- [[Legendre-Fenchel Transform]]
- [[Lagrangian Duality]]
- [[Optimization Problems in Spin Glasses]]

Duality theory provides a powerful and elegant framework for understanding and solving optimization problems. For a comprehensive exploration, refer to specialized texts in convex analysis, optimization theory, and operations research.


---

preceding: [[legendre-fenchel transform]]  


following: [[cramér's theorem]]

See also: [[signal processing]]


See also: [[consumer behavior]]


See also: [[support vector machines]]


See also: [[operations research]]


See also: [[slack in optimization]]


See also: [[resource allocation]]