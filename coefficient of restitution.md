---
date: 1719878399.751411
tags:
- autogenerated
- source__oai
- conversation_id__3cca3c71-e000-42f3-8854-e196e7b4d682
- msg_aaa20e66-73c7-4ebc-8cb0-93775202f001
- msg_238191d0-4cd4-4c97-8365-f362c7bd8c98
- colorclass/energy-dissipation
title: coefficient of restitution
---

**USER**

coefficient of restitution


**ASSISTANT**

The coefficient of restitution (COR) is a measure of the elasticity of collisions between two bodies. It quantifies how much kinetic energy is conserved in a collision. Mathematically, it is defined as the ratio of the relative speed of separation to the relative speed of approach of two colliding bodies. 

Formally, for two bodies with velocities $u_1$ and $u_2$ before collision and velocities $v_1$ and $v_2$ after collision, the coefficient of restitution \(e\) is given by:

$$
e = \frac{v_2 - v_1}{u_1 - u_2}
$$

Here, the velocities are taken along the line of impact. The value of \(e\) ranges from 0 to 1, where:
- \(e = 1\) corresponds to a perfectly elastic collision, meaning no kinetic energy is lost.
- \(e = 0\) corresponds to a perfectly inelastic collision, where the bodies stick together and move with a common velocity after impact.
- \(0 < e < 1\) corresponds to a partially elastic collision, where some kinetic energy is lost.

### Derivation and Physical Interpretation

To derive the expression for the coefficient of restitution, consider the following:
1. **Relative Velocity Before Collision**: The relative velocity of body 1 with respect to body 2 before the collision is \(u_1 - u_2\).
2. **Relative Velocity After Collision**: The relative velocity after the collision is \(v_2 - v_1\).

The coefficient of restitution is the ratio of these velocities:

$$
e = \frac{\text{Relative velocity after collision}}{\text{Relative velocity before collision}} = \frac{v_2 - v_1}{u_1 - u_2}
$$

### Implications and Usage

The coefficient of restitution is critical in various fields such as mechanical engineering, materials science, and sports physics. For instance:
- In **mechanical engineering**, it helps in analyzing impact forces and designing materials that can withstand impacts.
- In **materials science**, it aids in understanding the properties of materials, particularly their elastic and plastic deformation characteristics.
- In **sports physics**, it is used to analyze the behavior of balls and other equipment upon impact, influencing design and material choices for optimal performance.

### Example Calculation

Consider two spheres in a one-dimensional collision:
- Sphere 1: Initial velocity \(u_1 = 5 \, \text{m/s}\), final velocity \(v_1 = 2 \, \text{m/s}\)
- Sphere 2: Initial velocity \(u_2 = 0 \, \text{m/s}\), final velocity \(v_2 = 3 \, \text{m/s}\)

The coefficient of restitution is:

$$
e = \frac{v_2 - v_1}{u_1 - u_2} = \frac{3 - 2}{5 - 0} = \frac{1}{5} = 0.2
$$

This indicates a partially elastic collision where some kinetic energy is lost.

### Energy Considerations

The kinetic energy of a system of particles before and after a collision can be compared using the coefficient of restitution. In a perfectly elastic collision ($e = 1$), the kinetic energy is conserved, while in other cases, the loss of kinetic energy can be quantified.

If the masses of the bodies are \(m_1\) and \(m_2\), the kinetic energies before and after collision can be expressed as:

- **Before Collision**: \( KE_{\text{before}} = \frac{1}{2} m_1 u_1^2 + \frac{1}{2} m_2 u_2^2 \)
- **After Collision**: \( KE_{\text{after}} = \frac{1}{2} m_1 v_1^2 + \frac{1}{2} m_2 v_2^2 \)

The loss in kinetic energy can be found as:

$$
\Delta KE = KE_{\text{before}} - KE_{\text{after}}
$$

Understanding the coefficient of restitution thus provides insight into the dynamics of collisions and energy transformations in physical systems. For further reading, see the articles on [[Elastic Collision]], [[Inelastic Collision]], and [[Kinetic Energy]].

See also: [[materials science]]


See also: [[plastic deformation]]


See also: [[kinetic energy]]