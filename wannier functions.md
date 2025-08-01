---
date: 1721431462.755244
tags:
- autogenerated
- source__oai
- conversation_id__477f6a44-cc39-46b4-a63b-875670feb057
- msg_aaa200ed-3046-49c4-b78c-b6751ff7c27a
- msg_50f09ada-e8da-401d-a69d-331fa5a3f111
- colorclass/systems-theory
title: wannier functions
---

**USER**

Wannier Functions


**ASSISTANT**

Wannier functions are a set of orthogonal functions that provide a real-space representation of electronic states in a crystal. They are particularly useful in solid-state physics for describing localized states and are the real-space counterparts of Bloch functions. Wannier functions are named after the physicist Gregory Wannier, who introduced them in the context of the tight-binding model and electronic structure calculations.

### Definition and Construction

Consider a crystalline solid with a periodic potential. The electronic states in such a solid are described by Bloch functions \( \psi_{n\vec{k}}(\vec{r}) \), where \( n \) is the band index and \( \vec{k} \) is the wavevector in the first Brillouin zone. Bloch functions can be written as:
$$
\psi_{n\vec{k}}(\vec{r}) = e^{i\vec{k} \cdot \vec{r}} u_{n\vec{k}}(\vec{r})
$$
where \( u_{n\vec{k}}(\vec{r}) \) is a periodic function with the same periodicity as the crystal lattice.

The Wannier functions \( w_n(\vec{r} - \vec{R}) \) for band \( n \) and lattice vector \( \vec{R} \) are defined as the Fourier transform of the Bloch functions:
$$
w_n(\vec{r} - \vec{R}) = \frac{V}{(2\pi)^3} \int_{\text{BZ}} d\vec{k} \, e^{-i\vec{k} \cdot \vec{R}} \psi_{n\vec{k}}(\vec{r})
$$
where \( V \) is the volume of the unit cell, and the integral is over the first Brillouin zone (BZ).

### Properties of Wannier Functions

1. **Orthogonality**:
   Wannier functions are orthogonal and normalized:
   $$ 
   \langle w_n(\vec{r} - \vec{R}) | w_{n'}(\vec{r} - \vec{R'}) \rangle = \delta_{nn'} \delta_{\vec{R}\vec{R'}}
   $$

2. **Localization**:
   Wannier functions are typically localized in real space, meaning they decay rapidly away from their center. This localization makes them useful for studying local electronic properties and interactions in solids.

3. **Periodic Lattice Translation**:
   Wannier functions inherit the periodicity of the lattice. If \( \vec{R} \) is a lattice vector, then:
   $$ 
   w_n(\vec{r} - \vec{R}) = w_n(\vec{r}) \quad \text{for any lattice vector} \; \vec{R}
   $$

### Wannier Functions and Tight-Binding Model

In the tight-binding approximation, electrons are assumed to be tightly bound to atoms, and the overlap between neighboring atomic orbitals is treated as a perturbation. Wannier functions are particularly useful in this context as they can represent the localized atomic-like orbitals.

The Hamiltonian in the tight-binding model can be expressed in terms of Wannier functions:
$$
H = \sum_{n,\vec{R},\vec{R'}} t_{n\vec{R},n'\vec{R'}} c_{n\vec{R}}^\dagger c_{n'\vec{R'}}
$$
where \( t_{n\vec{R},n'\vec{R'}} \) are the [[hopping integrals]], representing the probability amplitude for an electron to hop from site \( \vec{R} \) in band \( n \) to site \( \vec{R'} \) in band \( n' \).

### Maximally Localized Wannier Functions

Maximally localized Wannier functions (MLWFs) are a special set of Wannier functions that are constructed to minimize the spatial spread. This is achieved through a unitary transformation of the Bloch functions. The goal is to find Wannier functions that are as localized as possible, which is useful for studying localized electronic states and constructing tight-binding Hamiltonians from first-principles calculations.

### Applications of Wannier Functions

1. **Electronic Structure Calculations**:
   Wannier functions are used to interpolate band structures and compute electronic properties with high precision. They are especially useful in large-scale [[density functional theory]] (DFT) calculations.

2. **Tight-Binding Models**:
   Wannier functions provide a natural basis for tight-binding models, allowing for the study of electronic, magnetic, and optical properties of materials.

3. **Topological Insulators and Superconductors**:
   Wannier functions help in understanding the localized states at the edges or surfaces of topological insulators and superconductors, aiding in the study of topological properties.

4. **Quantum Transport**:
   In quantum transport calculations, Wannier functions can be used to model the conductance and other transport properties of nanoscale devices.

### Example: One-Dimensional Chain

Consider a one-dimensional chain with a single atomic orbital per site. The Bloch functions are:
$$
\psi_k(x) = \frac{1}{\sqrt{N}} \sum_{j} e^{ikx_j} \phi(x - x_j)
$$
where \( \phi(x - x_j) \) is the atomic orbital centered at site \( x_j \).

The Wannier function \( w(x - x_j) \) is given by the Fourier transform of the Bloch functions:
$$
w(x - x_j) = \frac{1}{\sqrt{N}} \sum_{k} e^{-ikx_j} \psi_k(x)
$$

If the atomic orbitals \( \phi(x - x_j) \) are well localized, the Wannier functions \( w(x - x_j) \) will also be localized around \( x_j \).

### Conclusion

Wannier functions are a powerful tool in solid-state physics, providing a localized real-space description of electronic states in crystals. They complement the momentum-space Bloch functions and are instrumental in constructing tight-binding models, studying localized states, and understanding electronic properties of materials. Maximally localized Wannier functions, in particular, are crucial for accurately modeling complex materials and exploring topological phenomena.


---

preceding: [[bloch's theorem]]  


following: [[tight-binding model]]