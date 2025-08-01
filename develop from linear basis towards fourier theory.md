---
date: 1721509605.970678
tags:
- autogenerated
- source__oai
- conversation_id__98a4f107-a2cf-40c9-b0d2-45689415fcb9
- msg_aaa295ff-2732-4821-8b48-5b1c3b70db3b
- msg_57bf46ab-ac8c-4302-8f63-ad200576af7d
- colorclass/vector-space
title: develop from linear basis towards fourier theory
---

**USER**

develop from linear basis towards fourier theory


**ASSISTANT**

Fourier theory is deeply rooted in the concept of linear bases, specifically the idea of expressing functions in terms of basis functions. Here’s a step-by-step development from the concept of a linear basis to Fourier theory:

### From Linear Basis to Function Spaces

1. **Vector Spaces and Bases**:
   - In finite-dimensional vector spaces, a basis $\{v_1, v_2, \ldots, v_n\}$ allows any vector $v$ in the space to be uniquely expressed as a linear combination of basis vectors.
   - In function spaces, we extend this idea to express functions as linear combinations of a set of basis functions.

2. **Function Spaces**:
   - Consider a function space such as $L^2([a,b])$, the space of square-integrable functions on the interval $[a, b]$.
   - A basis for this function space consists of functions $\{ \phi_1(x), \phi_2(x), \ldots \}$ such that any function $f(x) \in L^2([a,b])$ can be written as
     $$ f(x) = \sum_{i=1}^\infty c_i \phi_i(x), $$
     where $c_i$ are coefficients.

### Orthogonal Bases and Fourier Series

3. **Orthogonality**:
   - An important property for bases in function spaces is orthogonality. Two functions $\phi_i(x)$ and $\phi_j(x)$ are orthogonal if
     $$ \int_a^b \phi_i(x) \phi_j(x) \, dx = 0 \text{ for } i \neq j. $$
   - If $\{\phi_i(x)\}$ is an orthogonal basis, the coefficients $c_i$ can be found using the inner product:
     $$ c_i = \frac{\int_a^b f(x) \phi_i(x) \, dx}{\int_a^b \phi_i(x)^2 \, dx}. $$

4. **Fourier Series**:
   - In the context of Fourier series, the basis functions are sines and cosines. For a function $f(x)$ defined on $[-\pi, \pi]$, the Fourier series expansion is:
     $$ f(x) = \frac{a_0}{2} + \sum_{n=1}^\infty \left( a_n \cos(nx) + b_n \sin(nx) \right), $$
     where the coefficients $a_n$ and $b_n$ are given by:
     $$ a_n = \frac{1}{\pi} \int_{-\pi}^{\pi} f(x) \cos(nx) \, dx, $$
     $$ b_n = \frac{1}{\pi} \int_{-\pi}^{\pi} f(x) \sin(nx) \, dx. $$

### Fourier Transform

5. **From Fourier Series to Fourier Transform**:
   - Fourier series are suitable for periodic functions. For non-periodic functions, we generalize to the Fourier transform.
   - The Fourier transform of a function $f(x)$ is given by:
     $$ \hat{f}(\xi) = \int_{-\infty}^{\infty} f(x) e^{-2\pi i \xi x} \, dx, $$
     where $\hat{f}(\xi)$ is the Fourier transform of $f(x)$.
   - The inverse Fourier transform is:
     $$ f(x) = \int_{-\infty}^{\infty} \hat{f}(\xi) e^{2\pi i \xi x} \, d\xi. $$

### Properties and Applications

6. **Properties**:
   - **Linearity**: Both the Fourier series and Fourier transform are linear operations.
   - **Parseval's Theorem**: For Fourier series, it states that the total energy (sum of squares) of the function is equal to the sum of the squares of its Fourier coefficients.
   - **Convolution Theorem**: The Fourier transform of the convolution of two functions is the pointwise product of their Fourier transforms.

7. **Applications**:
   - **Signal Processing**: Fourier transforms are used to analyze the frequency components of signals.
   - **Differential Equations**: Solutions to differential equations can often be found using Fourier series or transforms.
   - **Quantum Mechanics**: The wave function in quantum mechanics is often analyzed using Fourier transforms.

### Summary

Starting from the concept of a linear basis in finite-dimensional vector spaces, we extended the idea to function spaces where functions can be expressed as linear combinations of basis functions. Orthogonality is a crucial property for simplifying the computation of coefficients. Fourier series utilize sines and cosines as basis functions for periodic functions, while the Fourier transform generalizes this to non-periodic functions, allowing for the analysis and synthesis of functions in terms of their frequency components. These concepts have widespread applications in various fields, highlighting the importance of basis functions in both finite and infinite-dimensional spaces.


---

preceding: [[linear basis]]  


following: [[from fourier basis to spherical harmonics]]

See also: [[linear basis]]


See also: [[vector space]]


See also: [[wave function]]


See also: [[wave function in quantum mechanics]]


See also: [[spherical harmonics]]