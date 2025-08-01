---
date: 1717811141.200567
tags:
- autogenerated
- source__oai
- conversation_id__77e70e10-f02a-4f98-bd5c-6217b10122cf
- msg_aaa2d93c-e2f5-4fa7-8ab4-cc33d6c0ba5a
- msg_b8c9c494-c4ae-4490-803c-17b48ab9da53
- colorclass/information-theory
title: fokker-planck equation
---

**USER**

Fokker-Planck Equation


**ASSISTANT**

The Fokker-Planck equation, also known as the Kolmogorov forward equation, describes the time evolution of the probability density function of the state of a stochastic process. In the context of mean field game theory and stochastic processes, it plays a critical role in characterizing how the distribution of agents' states evolves over time.

### Mathematical Formulation

Consider a stochastic process \( \mathbf{x}(t) \) governed by the stochastic differential equation (SDE):
\[ d\mathbf{x}(t) = \mathbf{f}(\mathbf{x}(t), t) \, dt + \mathbf{G}(\mathbf{x}(t), t) \, d\mathbf{w}(t), \]
where:
- \( \mathbf{x}(t) \in \mathbb{R}^n \) is the state vector,
- \( \mathbf{f}(\mathbf{x}, t) \) is the drift term,
- \( \mathbf{G}(\mathbf{x}, t) \) is the diffusion term,
- \( \mathbf{w}(t) \) is a Wiener process (Brownian motion).

The Fokker-Planck equation describes the evolution of the probability density function \( p(\mathbf{x}, t) \) of the state \( \mathbf{x} \).

### Fokker-Planck Equation

The Fokker-Planck equation corresponding to the SDE above is given by:
\[ \frac{\partial p(\mathbf{x}, t)}{\partial t} = -\nabla \cdot (\mathbf{f}(\mathbf{x}, t) p(\mathbf{x}, t)) + \frac{1}{2} \sum_{i,j} \frac{\partial^2}{\partial x_i \partial x_j} \left[ ( \mathbf{G}(\mathbf{x}, t) \mathbf{G}^T(\mathbf{x}, t) )_{ij} p(\mathbf{x}, t) \right], \]
where \( p(\mathbf{x}, t) \) is the probability density function of \( \mathbf{x}(t) \), and \( \nabla \cdot \) denotes the divergence operator.

### Interpretation

- **Drift Term**: The term \( -\nabla \cdot (\mathbf{f}(\mathbf{x}, t) p(\mathbf{x}, t)) \) represents the deterministic part of the state evolution, driving the probability density function in the direction of the drift \( \mathbf{f}(\mathbf{x}, t) \).
- **Diffusion Term**: The term \( \frac{1}{2} \sum_{i,j} \frac{\partial^2}{\partial x_i \partial x_j} \left[ ( \mathbf{G}(\mathbf{x}, t) \mathbf{G}^T(\mathbf{x}, t) )_{ij} p(\mathbf{x}, t) \right] \) represents the stochastic part, spreading the probability density due to the random fluctuations governed by the diffusion matrix \( \mathbf{G}(\mathbf{x}, t) \).

### Example: One-Dimensional Case

For a one-dimensional stochastic process described by:
\[ dx(t) = f(x(t), t) \, dt + g(x(t), t) \, dW(t), \]
the Fokker-Planck equation simplifies to:
\[ \frac{\partial p(x, t)}{\partial t} = -\frac{\partial}{\partial x} \left[ f(x, t) p(x, t) \right] + \frac{1}{2} \frac{\partial^2}{\partial x^2} \left[ g^2(x, t) p(x, t) \right]. \]

### Application in Mean Field Games

In mean field game theory, the Fokker-Planck equation is used to model the evolution of the distribution of the states of a large population of agents. Each agent's state evolves according to a stochastic process influenced by both individual controls and the aggregate effect of the population (mean field).

#### Coupled System of HJB and Fokker-Planck Equations

The mean field game problem typically involves solving a coupled system of the Hamilton-Jacobi-Bellman (HJB) equation for the value function \( V \) and the Fokker-Planck equation for the density \( p \):

1. **HJB Equation**:
   \[ \frac{\partial V}{\partial t} + \min_{\alpha} \left[ L(x, \alpha, m) + \nabla V \cdot f(x, \alpha, m) + \frac{1}{2} \text{Tr}(G G^T \mathbf{H} V) \right] = 0, \]
   with terminal condition:
   \[ V(x, T) = \phi(x, m(T)). \]

2. **Fokker-Planck Equation**:
   \[ \frac{\partial m}{\partial t} + \nabla \cdot (m f(x, \alpha^*, m)) - \frac{1}{2} \nabla \cdot (\nabla \cdot (m G G^T)) = 0, \]
   where \( \alpha^* \) is the optimal control derived from the HJB equation.

### Numerical Solution

Numerical methods for solving the Fokker-Planck equation include finite difference methods, finite element methods, and spectral methods. These approaches discretize the spatial and temporal domains to approximate the solution of the PDE.

### Example Application: Ornstein-Uhlenbeck Process

Consider the Ornstein-Uhlenbeck process, a common example in stochastic processes:
\[ dx(t) = \theta (\mu - x(t)) \, dt + \sigma \, dW(t), \]
where \( \theta \) is the rate of mean reversion, \( \mu \) is the long-term mean, and \( \sigma \) is the volatility.

The corresponding Fokker-Planck equation is:
\[ \frac{\partial p(x, t)}{\partial t} = \theta \frac{\partial}{\partial x} [(x - \mu) p(x, t)] + \frac{\sigma^2}{2} \frac{\partial^2 p(x, t)}{\partial x^2}. \]

### Conclusion

The Fokker-Planck equation is a fundamental tool for understanding the evolution of probability distributions in stochastic systems. In mean field game theory, it provides a way to model the distribution of states in a large population of agents, enabling the analysis and design of optimal strategies in complex, dynamic environments.


---

preceding: [[mean field game theory]]  


following: [[key results of mean field game theory]]

See also: [[spectral methods]]


See also: [[stochastic differential equation perspective of sgd dynamics]]


See also: [[game theory]]


See also: [[stochastic processes]]


See also: [[considerable effort has been expended on understanding sgd for neural networks, including attempts to relate sgd to a discretization of a continuous time process via stochastic differential equations]]


See also: [[relate this discussion to the fokker-planck equation]]