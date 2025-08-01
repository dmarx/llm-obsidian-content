---
date: 1726201019.593531
tags:
- autogenerated
- source__oai
- conversation_id__66e3b3a4-0e90-8008-90aa-73f475e9aa4b
- msg_aaa25f52-a1ce-4610-b83a-390bec7bd433
- msg_50868e99-b499-445c-b7e4-6a3a1871c112
- colorclass/vector-space
title: thom's theorem
---

**USER**

Thom's Theorem


**ASSISTANT**

**Thom's Theorem** (also known as **Thom's Cobordism Theorem**) is a profound result in algebraic topology, named after the French mathematician **René Thom**. It provides a complete classification of cobordism classes of manifolds in terms of **[[stable homotopy theory]]**. Thom's work is foundational in cobordism theory and led to the development of **Thom spectra** and **Thom spaces**, which are central to modern homotopy theory.

### Context and Statement of Thom's Theorem

In **cobordism theory**, two \(n\)-dimensional manifolds \(M_1\) and \(M_2\) are considered **cobordant** if there exists an \( (n+1) \)-dimensional manifold \( W \) such that the boundary of \( W \) is the disjoint union of \( M_1 \) and \( M_2 \):

$$
\partial W = M_1 \sqcup M_2.
$$

Cobordism forms an **equivalence relation** on the set of closed, oriented \( n \)-manifolds, and the set of equivalence classes under cobordism forms an abelian group called the **cobordism group** \( \Omega_n \). Cobordism theory generalizes to various structures such as **unoriented**, **oriented**, **spin**, and **complex cobordism**. Thom's Theorem provides a powerful tool for understanding these cobordism groups.

### Thom's Theorem: Informal Statement

Thom's Theorem asserts that the cobordism classes of \( n \)-dimensional manifolds correspond to the **homotopy classes** of maps into a certain **Thom space**, which encodes the data of the vector bundles over the manifold.

Formally, for a given structure group \( G \) (such as \( \text{SO}(n) \) for oriented cobordism, \( \text{Spin}(n) \) for spin cobordism, etc.), the cobordism group \( \Omega_n^G \) is isomorphic to the **homotopy group** of the Thom spectrum associated with \( G \). Specifically:

$$
\Omega_n^G \cong \pi_n(MG),
$$

where:
- \( \Omega_n^G \) is the **cobordism group** of \( n \)-dimensional \( G \)-structured manifolds.
- \( MG \) is the **Thom spectrum** associated with the classifying space of the group \( G \).
- \( \pi_n(MG) \) is the **stable homotopy group** of the spectrum \( MG \).

### Understanding the Components of Thom's Theorem

#### 1. **Thom Spaces and Thom Spectra**

The notion of a **Thom space** arises naturally in the study of vector bundles. Given a vector bundle \( E \to M \) over a manifold \( M \), the **Thom space** \( T(E) \) is obtained by taking the total space of the vector bundle and collapsing the complement of the zero section to a point. The **Thom spectrum** generalizes this construction to families of vector bundles.

The Thom space construction captures the way a vector bundle "twists" over the base manifold and encodes important topological information about the bundle. For a classifying space \( BG \) of a group \( G \), the associated **Thom spectrum** \( MG \) organizes the Thom spaces for all possible vector bundles with structure group \( G \) over different manifolds.

- **Unoriented Cobordism**: The Thom space associated with unoriented cobordism is the Thom spectrum of the universal vector bundle over the **classifying space** of the **orthogonal group** \( BO \), denoted \( MO \). In this case, \( \Omega_n \cong \pi_n(MO) \), where \( \Omega_n \) is the \( n \)-th unoriented cobordism group.
  
- **Oriented Cobordism**: For oriented cobordism, the classifying space is \( BSO \), and the associated Thom spectrum is \( MSO \). Thus, oriented cobordism classes are described by \( \pi_n(MSO) \), where \( \Omega_n^{\text{SO}} \) is the oriented cobordism group.

#### 2. **Classifying Spaces**

A **classifying space** \( BG \) for a topological group \( G \) is a space such that principal \( G \)-bundles over a manifold \( M \) are classified by homotopy classes of maps from \( M \) to \( BG \). Classifying spaces play a central role in cobordism theory because they allow one to understand vector bundles through homotopy theory.

For example:
- \( BO \): Classifying space for real vector bundles (unoriented cobordism).
- \( BSO \): Classifying space for oriented vector bundles (oriented cobordism).
- \( BSpin \): Classifying space for spin vector bundles (spin cobordism).

The connection between cobordism and [[stable homotopy theory]] arises through **Thom spaces** and these **classifying spaces**.

#### 3. **Stable Homotopy Groups**

The **stable homotopy group** \( \pi_n(MG) \) is a limit of homotopy groups for a sequence of related spaces (the Thom spaces in this case). Thom's Theorem shows that cobordism groups are isomorphic to these stable homotopy groups, providing a link between cobordism and **[[stable homotopy theory]]**. This insight allows cobordism problems to be translated into questions about homotopy theory, which has powerful computational tools.

### Applications of Thom's Theorem

1. **Classification of Cobordism Classes**: Thom's Theorem provides a way to compute cobordism groups in various settings (oriented, unoriented, spin, complex) using [[stable homotopy theory]]. This classification helps distinguish between different manifolds based on their cobordism class.

2. **Characteristic Classes**: Cobordism classes can be distinguished by **[[characteristic classes]]** such as **Stiefel-Whitney classes**, **Pontryagin classes**, and **Chern classes**. Thom's work laid the foundation for understanding how these [[characteristic classes]] behave under cobordism.

3. **Homotopy Theory**: Thom's Theorem plays a central role in the development of **Thom spectra** and the application of cobordism to homotopy theory. Cobordism theory has deep connections with **[[stable homotopy theory]]**, where spectra like \( MO \), \( MSO \), and \( MU \) are used to compute homotopy groups of spheres and other spaces.

4. **Index Theory and Geometry**: The connection between cobordism and [[characteristic classes]] is crucial in **index theory**, particularly in the context of the **Atiyah-Singer Index Theorem**. The index of certain elliptic operators (like the Dirac operator on a spin manifold) is a cobordism invariant, and Thom's work helps explain these relationships.

5. **Mathematical Physics**: Cobordism theory, rooted in Thom's Theorem, plays a role in **quantum field theory**, **string theory**, and **topological quantum field theory** (TQFT). Cobordism invariants are used to classify possible topologies of space-time and to understand the behavior of fields and particles in these topologies.

### Example: Oriented Cobordism Groups

Using Thom's Theorem, we can compute the first few oriented cobordism groups \( \Omega_n^{\text{SO}} \) in terms of homotopy groups \( \pi_n(MSO) \). For small values of \( n \), these groups are:

- \( \Omega_0^{\text{SO}} = \mathbb{Z} \) (points can be oriented or not),
- \( \Omega_1^{\text{SO}} = 0 \),
- \( \Omega_2^{\text{SO}} = 0 \),
- \( \Omega_3^{\text{SO}} = 0 \),
- \( \Omega_4^{\text{SO}} = \mathbb{Z} \), related to the Euler characteristic of surfaces.

### Summary

**Thom's Theorem** provides a deep connection between **cobordism theory** and **[[stable homotopy theory]]** by showing that cobordism classes of manifolds correspond to stable homotopy groups of certain Thom spectra. This powerful result allows the classification of cobordism classes using tools from homotopy theory, leading to insights into the topology and geometry of manifolds. Thom's work laid the groundwork for much of modern topology and has profound implications in both pure mathematics and theoretical physics.

For further reading, see related topics like [[Cobordism Theory]], [[Stable Homotopy Theory]], and [[Characteristic Classes]].


---

preceding: [[cobordism theory]]  


following: [[thom spectra]]

See also: [[algebraic topology]]


See also: [[homotopy groups]]