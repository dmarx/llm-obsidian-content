---
date: 1726424570.993899
tags:
- autogenerated
- source__oai
- conversation_id__66e723d5-a48c-8008-98ac-50583dd0cb1d
- msg_198cb83b-1139-44b7-bb72-69d02d44e1b4
- msg_29e126fe-0eef-4eb2-9a61-d6c471567c1e
- colorclass/system-dynamics
title: floquet multipliers
---

**USER**

Floquet multipliers


**ASSISTANT**

### Floquet Multipliers

**Floquet multipliers** are a key concept in the analysis of **linear differential equations with periodic coefficients**, used primarily in the context of [[Floquet Theory]]. These multipliers determine the **stability** of periodic solutions by describing how perturbations to a periodic system grow or decay over time.

#### Definition

Consider a linear system of differential equations with **periodic coefficients**:

$$
\frac{d}{dt} \mathbf{x}(t) = A(t) \mathbf{x}(t),
$$

where:

- $\mathbf{x}(t) \in \mathbb{R}^n$ is the state vector.
- $A(t) \in \mathbb{R}^{n \times n}$ is a matrix of coefficients that is **periodic** with period $T$, meaning $A(t + T) = A(t)$ for all $t$.

The **fundamental matrix solution** $\Phi(t)$ of this system satisfies:

$$
\frac{d}{dt} \Phi(t) = A(t) \Phi(t), \quad \Phi(0) = I
$$

where $I$ is the identity matrix.

The **monodromy matrix** is the fundamental matrix evaluated at the period $T$:

$$
M = \Phi(T)
$$

The **Floquet multipliers** are the eigenvalues $\mu_i$ of the monodromy matrix $M$:

$$
M \mathbf{v}_i = \mu_i \mathbf{v}_i
$$

where $\mathbf{v}_i$ are the corresponding eigenvectors.

These multipliers characterize how the system behaves over one period and are crucial for understanding the long-term stability of the system.

#### Floquet Exponents

The **Floquet exponents** $\lambda_i$ are related to the Floquet multipliers by the equation:

$$
\mu_i = e^{\lambda_i T}
$$

where $T$ is the period of the system. The Floquet exponents describe the growth or decay of perturbations in a continuous-time framework, while the multipliers capture the behavior over discrete periods.

- If $\text{Re}(\lambda_i) < 0$, the solution decays, corresponding to $|\mu_i| < 1$.
- If $\text{Re}(\lambda_i) > 0$, the solution grows, corresponding to $|\mu_i| > 1$.
- If $\text{Re}(\lambda_i) = 0$, the solution is marginally stable, corresponding to $|\mu_i| = 1$.

#### Stability Criterion

The **stability of the system** depends on the magnitude of the Floquet multipliers:

- **Stable system**: If all Floquet multipliers satisfy $|\mu_i| < 1$, the system is **asymptotically stable**. Small perturbations decay over time, and the system's solutions remain bounded.
  
- **Unstable system**: If any Floquet multiplier satisfies $|\mu_i| > 1$, the system is **unstable**. Small perturbations grow exponentially, leading to unbounded solutions.

- **Marginally stable system**: If $|\mu_i| = 1$ for some multipliers, and all other multipliers satisfy $|\mu_i| \leq 1$, the system is **marginally stable**. In this case, perturbations neither grow nor decay but may persist as oscillations or bounded variations.

#### Example: Stability of a Periodically Forced Oscillator

Consider the following example of a periodically forced harmonic oscillator:

$$
\frac{d^2 x(t)}{dt^2} + \omega_0^2 (1 + \epsilon \cos(\Omega t)) x(t) = 0,
$$

where $\omega_0$ is the natural frequency of the oscillator, $\epsilon$ is the strength of the periodic forcing, and $\Omega$ is the forcing frequency. This is a form of **Mathieu's equation**, a classic example where Floquet multipliers help analyze stability.

To convert this into a first-order system, let $x_1(t) = x(t)$ and $x_2(t) = \frac{dx(t)}{dt}$:

$$
\frac{d}{dt}
\begin{pmatrix}
x_1(t) \\
x_2(t)
\end{pmatrix}
=
\begin{pmatrix}
0 & 1 \\
-\omega_0^2 (1 + \epsilon \cos(\Omega t)) & 0
\end{pmatrix}
\begin{pmatrix}
x_1(t) \\
x_2(t)
\end{pmatrix}
$$

This system has periodic coefficients with period $T = \frac{2\pi}{\Omega}$. By solving for the monodromy matrix $M = \Phi(T)$, we can compute the Floquet multipliers (eigenvalues of $M$), which indicate whether the solutions are stable (if $|\mu_i| < 1$) or unstable (if $|\mu_i| > 1$).

For certain parameter ranges of $\omega_0$, $\epsilon$, and $\Omega$, this system exhibits **parametric resonance**, where the Floquet multipliers become larger than 1, indicating that small perturbations will grow exponentially.

#### Computation of Floquet Multipliers

For most systems, the Floquet multipliers cannot be computed analytically and must be found numerically:

1. **Solve the fundamental matrix equation**: Compute the fundamental matrix $\Phi(t)$ by solving the system of differential equations for the fundamental solution, typically using numerical methods like Runge-Kutta.

2. **Evaluate the monodromy matrix**: Evaluate the fundamental matrix at time $T$ to obtain the monodromy matrix $M = \Phi(T)$.

3. **Compute the eigenvalues**: The Floquet multipliers $\mu_i$ are the eigenvalues of $M$, which can be found using standard numerical methods for eigenvalue computation.

Many software tools, such as MATLAB, have built-in solvers for periodic systems, and specific functions like `floquet` or `ode45` can be used in conjunction with numerical eigenvalue routines to compute the multipliers.

#### Floquet Theory in Delay Differential Equations (DDEs)

Floquet theory can also be extended to analyze **delay differential equations (DDEs)** with periodic coefficients. For a linear DDE of the form:

$$
\frac{d}{dt} y(t) = A(t) y(t) + B(t) y(t - \tau),
$$

where $A(t)$ and $B(t)$ are periodic with period $T$, Floquet multipliers can be computed similarly by analyzing the **monodromy operator**, which maps the state over one period.

In the DDE case, numerical methods for solving delayed systems are typically used to compute the monodromy matrix, and its eigenvalues give the Floquet multipliers.

#### Summary

- **Floquet multipliers** are eigenvalues of the **monodromy matrix** and describe the stability of a periodic system.
- These multipliers tell whether small perturbations will grow, decay, or remain bounded over time.
- They are related to **Floquet exponents** through the relation $\mu_i = e^{\lambda_i T}$.
- The system is stable if all Floquet multipliers lie within the unit circle, unstable if any lie outside, and marginally stable if any are on the unit circle.

Floquet multipliers provide a structured way to analyze the long-term behavior of periodically driven or time-periodic systems across many disciplines, from mechanical systems and control theory to biological systems and [[delay differential equations]].


---

preceding: [[monodromy matrix]]  


following: [[floquet exponents]]

See also: [[control theory]]