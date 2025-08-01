---
date: 1721431591.052374
tags:
- autogenerated
- source__oai
- conversation_id__477f6a44-cc39-46b4-a63b-875670feb057
- msg_aaa2cfbb-5dfe-450a-88ca-c8379b79828b
- msg_587babf2-7271-4458-913c-db7f185b9c3f
- colorclass/systems-theory
title: tight-binding model
---

**USER**

Tight-Binding Model


**ASSISTANT**

The tight-binding model is a theoretical approach used to describe the electronic structure of solids. It assumes that electrons are tightly bound to atoms and that their wavefunctions overlap slightly with those of neighboring atoms. This model is particularly useful for understanding the electronic properties of materials with localized electrons, such as transition metals, semiconductors, and molecular crystals.

### Key Concepts

1. **Localized Atomic Orbitals**:
   In the tight-binding model, electrons are assumed to occupy localized atomic orbitals \( \phi_i(\vec{r}) \) centered at atomic sites \( \vec{R}_i \). These orbitals form the basis states for constructing the electronic wavefunctions.

2. **Hamiltonian**:
   The Hamiltonian of the tight-binding model is expressed in terms of creation and annihilation operators acting on these localized states. It includes on-site energies and hopping integrals representing the probability amplitude for an electron to hop from one site to another.

3. **On-Site Energy and Hopping Integrals**:
   - **On-Site Energy (\(\epsilon_i\))**: The energy associated with an electron residing at site \( \vec{R}_i \).
   - **Hopping Integral (\(t_{ij}\))**: The energy associated with an electron hopping from site \( \vec{R}_i \) to site \( \vec{R}_j \). It accounts for the overlap of atomic orbitals on neighboring sites.

### Mathematical Formalism

The tight-binding Hamiltonian for a single electron in a crystal lattice can be written as:
$$
\hat{H} = \sum_{i} \epsilon_i c_i^\dagger c_i + \sum_{\langle i, j \rangle} t_{ij} c_i^\dagger c_j
$$
where \( c_i^\dagger \) and \( c_i \) are the creation and annihilation operators for an electron at site \( \vec{R}_i \), respectively, and \( \langle i, j \rangle \) denotes the sum over nearest-neighbor pairs.

### Example: 1D Tight-Binding Model

Consider a one-dimensional chain of atoms with a single atomic orbital per site. The Hamiltonian is:
$$
\hat{H} = \sum_{i} \epsilon_i c_i^\dagger c_i + \sum_{i} t (c_i^\dagger c_{i+1} + c_{i+1}^\dagger c_i)
$$
Assuming uniform on-site energy \(\epsilon_i = \epsilon\) and uniform hopping \(t_{ij} = t\), the Hamiltonian simplifies to:
$$
\hat{H} = \epsilon \sum_{i} c_i^\dagger c_i + t \sum_{i} (c_i^\dagger c_{i+1} + c_{i+1}^\dagger c_i)
$$

To find the energy eigenvalues, we solve the Schrödinger equation in the basis of Bloch states:
$$
\psi_k(x) = \frac{1}{\sqrt{N}} \sum_{j} e^{ikx_j} \phi(x - x_j)
$$
where \( k \) is the wavevector, \( N \) is the number of atoms, and \( \phi(x - x_j) \) is the atomic orbital centered at site \( j \).

The eigenvalues are obtained by applying the Hamiltonian to the Bloch states:
$$
\hat{H} \psi_k = E(k) \psi_k
$$

For the 1D chain, this leads to the energy dispersion relation:
$$
E(k) = \epsilon + 2t \cos(k a)
$$
where \( a \) is the lattice constant. This dispersion relation shows that the energy spectrum forms a band, with the width of the band determined by the hopping parameter \( t \).

### Higher-Dimensional Systems

The tight-binding model can be extended to higher-dimensional systems by considering more complex lattices and including additional hopping terms. For example, in a two-dimensional square lattice, the Hamiltonian is:
$$
\hat{H} = \epsilon \sum_{i,j} c_{i,j}^\dagger c_{i,j} + t \sum_{i,j} \left( c_{i,j}^\dagger c_{i+1,j} + c_{i,j}^\dagger c_{i,j+1} + \text{H.c.} \right)
$$
where \( (i,j) \) denotes the lattice site indices in the two-dimensional grid. The corresponding energy dispersion relation is:
$$
E(\vec{k}) = \epsilon + 2t (\cos(k_x a) + \cos(k_y a))
$$
where \( \vec{k} = (k_x, k_y) \) is the wavevector in the 2D Brillouin zone.

### Applications

1. **Electronic Properties of Solids**:
   The tight-binding model helps in understanding the electronic band structure of solids, including metals, semiconductors, and insulators. It provides insights into the formation of energy bands and band gaps.

2. **Magnetism**:
   The model can be extended to include spin interactions, leading to the study of magnetic properties in materials. The Hubbard model, for instance, is a tight-binding model that includes electron-electron interactions and is used to study magnetism and electron correlation effects.

3. **Topological Insulators**:
   The tight-binding model is essential in studying topological phases of matter. By incorporating spin-orbit coupling and other terms, it helps in predicting and understanding the behavior of topological insulators and other exotic phases.

4. **Molecular Electronics**:
   In molecular electronics, the tight-binding model is used to study the electronic properties of molecular chains and networks, providing a basis for designing molecular-scale electronic devices.

### Conclusion

The tight-binding model is a powerful and versatile tool in [[condensed matter physics]] and materials science. It provides a simple yet effective way to understand the electronic properties of solids by focusing on the localized nature of atomic orbitals and their interactions. By capturing the essence of band formation and electronic behavior in various materials, it lays the foundation for more complex models and computational methods used in modern electronic structure calculations.


---

preceding: [[wannier functions]]  


following: [[hopping integrals]]

See also: [[dispersion relation]]


See also: [[anderson localization]]


See also: [[spectral properties of band matrices]]


See also: [[materials science]]


See also: [[transfer matrix method]]


See also: [[bloch's theorem]]