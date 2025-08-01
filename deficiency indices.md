---
date: '2025-06-29T18:35:11.475838Z'
tags:
- autogenerated
- source__claude
- conversation_id__b8985c54-72f1-4b0b-8c80-057448445379
- msg_d8675dcb-d747-4137-9f4d-4409d62ad251
- msg_f62f2489-10f0-4179-9f60-7200e624fd65
- colorclass/vector-space
title: deficiency indices
---

**USER**

deficiency indices


**ASSISTANT**

The user is asking about deficiency indices. This is a specific concept in operator theory related to symmetric operators on Hilbert spaces and their self-adjoint extensions. I need to provide a clear, focused explanation without going off on too many tangents.

Key points to cover:
1. Definition of deficiency indices
2. Connection to symmetric operators and their adjoints
3. The von Neumann extension theory
4. Classification of extensions based on deficiency indices
5. Examples
6. Applications

I should be precise and mathematical but not overly verbose.# Deficiency Indices

**Deficiency indices** are a pair of non-negative integers $(n_+, n_-)$ that characterize a [[symmetric operator]] on a [[Hilbert space]] and determine the existence and uniqueness of its [[self-adjoint extensions]]. They measure the "deficiency" of the operator in being self-adjoint.

## Definition

For a symmetric operator $T$ on a Hilbert space $H$ (i.e., $T \subset T^*$), the **deficiency indices** are:

$$n_+ = \dim \ker(T^* - iI)$$
$$n_- = \dim \ker(T^* + iI)$$

where $T^*$ is the [[adjoint operator]] of $T$.

## von Neumann's Extension Theory

**Theorem (von Neumann):** Let $T$ be a symmetric operator with deficiency indices $(n_+, n_-)$. Then:

1. $T$ has self-adjoint extensions if and only if $n_+ = n_-$
2. When $n_+ = n_- = n$, the set of self-adjoint extensions is parameterized by $n \times n$ unitary matrices
3. If $n_+ = n_- = 0$, then $T$ is essentially self-adjoint (has a unique self-adjoint extension, namely its closure)
4. If $n_+ \neq n_-$, then $T$ has no self-adjoint extensions

## Deficiency Subspaces

The **deficiency subspaces** are:
$$\mathcal{N}_+ = \ker(T^* - iI) = \{f \in D(T^*) : T^*f = if\}$$
$$\mathcal{N}_- = \ker(T^* + iI) = \{f \in D(T^*) : T^*f = -if\}$$

These are finite-dimensional subspaces of $H$.

## Key Properties

### Dimension Stability
For any $\lambda \in \mathbb{C} \setminus \mathbb{R}$:
- $\dim \ker(T^* - \lambda I) = n_+$ if $\text{Im}(\lambda) > 0$
- $\dim \ker(T^* - \lambda I) = n_-$ if $\text{Im}(\lambda) < 0$

### Orthogonality
The deficiency subspaces are orthogonal: $\mathcal{N}_+ \perp \mathcal{N}_-$.

### Domain Decomposition
$$D(T^*) = D(T) \oplus \mathcal{N}_+ \oplus \mathcal{N}_-$$

## Construction of Self-Adjoint Extensions

When $n_+ = n_- = n$, self-adjoint extensions are constructed as follows:

1. Choose any [[unitary operator]] $U: \mathcal{N}_+ \to \mathcal{N}_-$
2. Define the extension $T_U$ with domain:
   $$D(T_U) = D(T) \oplus \{f + Uf : f \in \mathcal{N}_+\}$$
3. For $x \in D(T)$ and $f \in \mathcal{N}_+$:
   $$T_U(x + f + Uf) = Tx + if - iUf$$

## Examples

### Momentum Operator
Consider $T = -i\frac{d}{dx}$ on $L^2([0,1])$ with domain $D(T) = \{f \in H^1([0,1]) : f(0) = f(1) = 0\}$.

**Calculation:**
- $T^*$ has domain $H^1([0,1])$ and acts as $T^*f = -if'$
- $(T^* - iI)f = 0 \Rightarrow -if' - if = 0 \Rightarrow f(x) = ce^{-x}$
- $(T^* + iI)f = 0 \Rightarrow -if' + if = 0 \Rightarrow f(x) = ce^x$
- Both give one-dimensional spaces, so $(n_+, n_-) = (1,1)$

**Extensions:** Parameterized by boundary conditions $f(1) = e^{i\theta}f(0)$ for $\theta \in [0,2\pi)$.

### Laplacian on Interval
For $T = -\frac{d^2}{dx^2}$ on $L^2([0,1])$ with domain $D(T) = \{f \in H^2([0,1]) : f(0) = f'(0) = f(1) = f'(1) = 0\}$:

**Result:** $(n_+, n_-) = (2,2)$, leading to a 4-parameter family of self-adjoint extensions corresponding to different boundary conditions.

### Harmonic Oscillator
For $T = -\frac{d^2}{dx^2} + x^2$ on $L^2(\mathbb{R})$ with domain $C_0^\infty(\mathbb{R})$:

**Result:** $(n_+, n_-) = (0,0)$, so $T$ is essentially self-adjoint.

## Applications

### Quantum Mechanics
**Self-adjoint operators** represent [[observables]] in quantum mechanics. Deficiency indices determine:
- Whether a symmetric Hamiltonian can be made self-adjoint
- The boundary conditions needed for self-adjointness
- The physical interpretation of different extensions

### Differential Equations
For [[Sturm-Liouville problems]], deficiency indices classify:
- Regular vs. singular endpoints
- Limit-point vs. limit-circle behavior
- Number of boundary conditions needed

### Scattering Theory
Deficiency indices affect:
- Number of scattering channels
- Existence of bound states
- Resonance phenomena

## Computational Aspects

### Numerical Determination
For discretized operators:
1. Compute the adjoint operator matrix
2. Find kernels of $(T^* \pm iI)$
3. Count dimensions (accounting for numerical tolerance)

### Boundary Condition Implementation
Self-adjoint extensions correspond to:
- Dirichlet boundary conditions
- Neumann boundary conditions  
- Robin boundary conditions
- Periodic boundary conditions
- More exotic boundary conditions for higher deficiency indices

## Related Concepts

### Essential Self-Adjointness
An operator is **essentially self-adjoint** if $(n_+, n_-) = (0,0)$. Criteria include:
- **Weyl's criterion:** $(T \pm iI)$ have dense range
- **Nelson's theorem:** For generators of strongly continuous groups

### Spectral Theory
Deficiency indices affect:
- Spectral properties of extensions
- Completeness of eigenfunctions
- Resolvent behavior

### Index Theory
Connected to:
- [[Fredholm index]] for elliptic operators
- [[Morse index]] in variational problems
- Topological invariants of operator families

Deficiency indices provide a complete classification of the self-adjoint extension problem for symmetric operators, forming a cornerstone of the theory connecting functional analysis with applications in physics and differential equations.


---

preceding: [[operator theory]]