---
date: 1713994796.064424
tags:
- autogenerated
- source__oai
- conversation_id__d42b6698-cc74-4885-8a67-5c84e54c2d57
- msg_aaa2ec75-2195-453a-a937-86735c35992f
- msg_aa42a922-9b44-457d-9fcf-9e8c33be7ac0
- colorclass/information-theory
title: pullback operator
---

**USER**

pullback operator


**ASSISTANT**

### Pullback Operator

In mathematics, particularly within the realms of [[Differential Geometry]], the pullback operator is a fundamental concept used to transfer geometric, algebraic, and functional structures from one space to another through a smooth mapping. This operator is primarily associated with functions, forms, and tensors, rather than directly with measures, reflecting its broader applicability in various mathematical contexts.

### Definition and Description

Suppose we have a smooth map $f: M \to N$ between two smooth manifolds $M$ and $N$. The pullback operator associated with $f$, denoted by $f^*$, operates on differential forms (and more generally on tensor fields) defined on $N$, pulling them back to differential forms on $M$.

#### Differential Forms

For a differential form $\omega$ on $N$, the pullback form $f^*\omega$ on $M$ is defined by the rule:
$$
(f^*\omega)_p(v_1, \dots, v_k) = \omega_{f(p)}(df_p(v_1), \dots, df_p(v_k))
$$
for any $p \in M$ and $v_1, \dots, v_k \in T_pM$ (the tangent space to $M$ at $p$). Here, $df_p$ is the differential of $f$ at $p$, which maps tangent vectors from $M$ at $p$ to tangent vectors in $N$ at $f(p)$.

### Properties of the Pullback Operator

1. **Linearity**: The pullback operator is linear, i.e., $f^*(\alpha \omega + \beta \eta) = \alpha f^*\omega + \beta f^*\eta$ for differential forms $\omega, \eta$ on $N$ and scalars $\alpha, \beta$.

2. **Composition**: For two smooth maps $f: M \to N$ and $g: N \to P$, the pullback operators satisfy $(g \circ f)^* = f^* \circ g^*$, reflecting the composition of the underlying mappings.

3. **Wedge Product**: The pullback operator commutes with the wedge product, i.e., $f^*(\omega \wedge \eta) = f^*\omega \wedge f^*\eta$ for forms $\omega$ and $\eta$ on $N$.

4. **Pullback of a Function**: If $f: M \to N$ is smooth and $\phi: N \to \mathbb{R}$ is a smooth function, then $f^*\phi = \phi \circ f$, which means the pullback of $\phi$ is the composition of $\phi$ with $f$.

### Applications of the Pullback Operator

- **Differential Topology and Geometry**: The pullback operator is crucial in defining and analyzing geometric structures on manifolds, particularly in situations involving submanifolds, coverings, or more complex structures like fiber bundles.
- **Physics and Engineering**: In theoretical physics, the pullback operator is used to define how fields and physical laws transform under coordinate changes or more general transformations, essential for formulating theories like general relativity.
- **Analysis on Manifolds**: The pullback is fundamental in the integration on manifolds, particularly through the change of variables formula in integration. If $\omega$ is a differential form on $N$ and $f: M \to N$ is a smooth surjective map, then integrating $\omega$ over $N$ can be related to integrating $f^*\omega$ over $M$.

### Summary

The pullback operator, $f^*$, is a powerful mathematical tool that provides a method for transferring structures from one manifold to another via a smooth map, preserving and adapting geometric, algebraic, and functional attributes suited to the analysis and understanding of complex mathematical and physical phenomena.


---

preceding: [[pushforward and pullback measures]]  


following: [[operator vs. function vs. form]]

See also: [[change of variables]]