---
date: 1720112437.89591
tags:
- autogenerated
- source__oai
- conversation_id__b730c2ba-6b58-4afa-b11c-113af5d1e02e
- msg_aaa26471-7043-4a01-9a45-1013c75ef32b
- msg_c9d49669-537f-4216-aebf-42380a50eeab
- colorclass/systems-theory
title: conformal field theory
---

**USER**

conformal field theory


**ASSISTANT**

Conformal Field Theory (CFT) is a type of quantum field theory (QFT) that is invariant under conformal transformations, which include transformations that preserve angles but not necessarily distances. CFTs are essential in various areas of theoretical physics, including string theory, statistical mechanics, and condensed matter physics. They provide powerful tools for understanding [[critical phenomena]] and the properties of strongly correlated systems.

## Overview

### Conformal Transformations

Conformal transformations preserve the angle between curves but can change their lengths. In \(d\)-dimensional space, conformal transformations include:
- **Translations**: Shifting all points by a constant vector.
- **Rotations**: Rotating points around an origin.
- **Dilations**: Scaling all distances by a constant factor.
- **Special Conformal Transformations**: Combining an inversion, translation, and another inversion.

### Conformal Symmetry

A theory is conformally invariant if its action remains unchanged under conformal transformations. This symmetry imposes stringent constraints on the theory, leading to the simplification of many problems.

### Primary Operators and Correlation Functions

Primary operators are fields that transform in a specific way under conformal transformations. They form the building blocks of CFTs. Correlation functions of primary operators are highly constrained by conformal symmetry.

For example, the two-point correlation function of a primary operator \(\mathcal{O}(x)\) with scaling dimension \(\Delta\) is:

$$
\langle \mathcal{O}(x) \mathcal{O}(y) \rangle = \frac{C}{|x - y|^{2\Delta}}
$$

where \(C\) is a constant.

### Conformal Algebra

The conformal algebra in \(d\)-dimensions is \(so(d,2)\). In two dimensions, the conformal algebra is infinite-dimensional, consisting of the Virasoro algebra, which extends the Lie algebra of infinitesimal conformal transformations.

## Two-Dimensional Conformal Field Theory

Two-dimensional (2D) CFTs are particularly rich and well-studied due to their enhanced symmetry. The conformal group in 2D is infinite-dimensional, leading to the Virasoro algebra with central charge \(c\).

### Virasoro Algebra

The Virasoro algebra is generated by modes \(L_n\) and a central charge \(c\):

$$
[L_m, L_n] = (m-n)L_{m+n} + \frac{c}{12}(m^3 - m) \delta_{m+n,0}
$$

### Primary Fields and Conformal Blocks

Primary fields \(\phi(z, \bar{z})\) in 2D CFT transform under conformal transformations with scaling dimensions \(h\) and \(\bar{h}\). Correlation functions can be decomposed into conformal blocks, which encode the contribution of primary fields and their descendants.

### Operator Product Expansion (OPE)

The OPE is a crucial concept in CFT, allowing the product of two operators to be expanded as a series of local operators:

$$
\mathcal{O}_i(x) \mathcal{O}_j(y) = \sum_k C_{ij}^k |x - y|^{\Delta_k - \Delta_i - \Delta_j} \mathcal{O}_k(y)
$$

### Minimal Models

Minimal models are specific 2D CFTs characterized by a finite number of primary fields. They are exactly solvable and classified by their central charge \(c\) and the spectrum of primary fields.

## Higher-Dimensional Conformal Field Theory

In higher dimensions, CFTs also exhibit rich structures and are relevant in various contexts such as the AdS/CFT correspondence.

### Conformal Bootstrap

The conformal bootstrap is a non-perturbative method for studying CFTs by exploiting the constraints of conformal symmetry and crossing symmetry of four-point functions:

$$
\langle \mathcal{O}_1(x_1) \mathcal{O}_2(x_2) \mathcal{O}_3(x_3) \mathcal{O}_4(x_4) \rangle
$$

The bootstrap equations relate different channels of the four-point function, providing powerful constraints on the operator dimensions and OPE coefficients.

### Applications

CFTs are used to understand:
- **Critical Phenomena**: Describing universality classes of phase transitions.
- **String Theory**: Worldsheet theories of strings are 2D CFTs.
- **AdS/CFT Correspondence**: Relating CFTs on the boundary of AdS space to gravity in the bulk.
- **Quantum Gravity**: Providing insights into the holographic principle and quantum aspects of black holes.

## Mathematical Formalism

### Radial Quantization

Radial quantization is a method used in CFT where time evolution is replaced by scaling transformations, with the origin acting as a time-like point. This approach simplifies the analysis of operator insertions and correlation functions.

### Modular Invariance

In 2D CFT, the torus partition function must be invariant under modular transformations, providing constraints on the spectrum of the theory.

### Central Charge

The central charge \(c\) measures the number of degrees of freedom in the CFT. It appears in the Virasoro algebra and the Cardy formula for the density of states:

$$
S = 2\pi \sqrt{\frac{c}{6} (L_0 - \frac{c}{24})}
$$

## Further Reading

For more detailed treatments of conformal field theory and its applications, consider exploring the following topics:

- [[Virasoro Algebra]]
- [[Minimal Models]]
- [[Conformal Bootstrap]]
- [[AdS/CFT Correspondence]]
- [[Critical Phenomena]]
- [[String Theory]]

These topics provide comprehensive insights into the theoretical foundations, mathematical structures, and practical applications of conformal field theory in various fields of physics.


---

preceding: [[adscft correspondence]]  


following: [[operator product expansion]]

See also: [[adscft correspondence overview]]


See also: [[anti-de sitter space overview]]


See also: [[condensed matter physics]]


See also: [[conformal structure]]


See also: [[schramm–loewner evolution]]


See also: [[root system]]


See also: [[introduction to gaussian free fields]]


See also: [[universality classes]]


See also: [[conformal field theory (cft) overview]]


See also: [[solitons]]