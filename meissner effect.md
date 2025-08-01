---
date: 1721432779.799054
tags:
- autogenerated
- source__oai
- conversation_id__477f6a44-cc39-46b4-a63b-875670feb057
- msg_aaa253eb-5e3d-4a40-a914-55ae0fc5688f
- msg_a1523468-737a-464d-8d50-254f00dc834c
- colorclass/systems-theory
title: meissner effect
---

**USER**

Meissner Effect


**ASSISTANT**

The Meissner effect is a fundamental phenomenon observed in superconductors, discovered by Walther Meissner and Robert Ochsenfeld in 1933. It describes the expulsion of magnetic fields from the interior of a superconductor when it transitions into the superconducting state below a critical temperature. This effect is a hallmark of superconductivity and demonstrates the perfect diamagnetism of superconductors.

### Key Concepts

1. **Superconductivity**:
   Superconductivity is a state of matter characterized by zero electrical resistance and the expulsion of magnetic fields, occurring below a certain critical temperature \(T_c\).

2. **Perfect Diamagnetism**:
   Superconductors exhibit perfect diamagnetism, meaning they completely repel external magnetic fields from their interior.

3. **Critical Temperature (\(T_c\))**:
   The temperature below which a material becomes superconducting and exhibits the Meissner effect.

### The Meissner Effect

#### Description

When a material transitions from the normal state to the superconducting state below its critical temperature, it expels any magnetic field present within it. This expulsion of magnetic fields is complete, even if the material was in a magnetic field before the transition. This effect distinguishes superconductors from perfect conductors, which would merely freeze the magnetic flux in place without expelling it.

#### Mathematical Formulation

The Meissner effect can be described mathematically using Maxwell's equations and the London equations for superconductors.

**London Equations**:

1. **First London Equation**:
   $$
   \vec{E} + \frac{\partial \vec{J}}{\partial t} = 0
   $$
   This equation states that in a superconductor, an electric field \( \vec{E} \) can induce a current density \( \vec{J} \) with no resistance.

2. **Second London Equation**:
   $$
   \vec{\nabla} \times \vec{J} = -\frac{n_s e^2}{m} \vec{B}
   $$
   where \( n_s \) is the density of superconducting carriers (Cooper pairs), \( e \) is the charge of an electron, \( m \) is the mass of an electron, and \( \vec{B} \) is the magnetic field.

Combining the second London equation with Ampère's law:
$$
\vec{\nabla} \times \vec{B} = \mu_0 \vec{J}
$$
we get:
$$
\vec{\nabla} \times (\vec{\nabla} \times \vec{B}) = -\frac{n_s e^2 \mu_0}{m} \vec{B}
$$
Using the vector identity \( \vec{\nabla} \times (\vec{\nabla} \times \vec{B}) = \vec{\nabla}(\vec{\nabla} \cdot \vec{B}) - \nabla^2 \vec{B} \) and the fact that \( \vec{\nabla} \cdot \vec{B} = 0 \), we obtain:
$$
\nabla^2 \vec{B} = \frac{\vec{B}}{\lambda_L^2}
$$
where \( \lambda_L \) is the London penetration depth:
$$
\lambda_L = \sqrt{\frac{m}{\mu_0 n_s e^2}}
$$

This equation shows that the magnetic field decays exponentially inside the superconductor with a characteristic length scale given by the London penetration depth \( \lambda_L \).

### Penetration Depth

The London penetration depth \( \lambda_L \) is a measure of the distance over which an external magnetic field penetrates into a superconductor before being exponentially attenuated. For a typical superconductor, \( \lambda_L \) is on the order of 100 nm.

### Experimental Observation

The Meissner effect can be observed experimentally by cooling a superconducting material below its critical temperature in the presence of a magnetic field. The magnetic field lines are expelled from the bulk of the superconductor, and this expulsion can be detected using sensitive magnetometers or by visualizing the levitation of a magnet above a superconducting material (due to the repulsive magnetic forces).

### Type I and Type II Superconductors

- **Type I Superconductors**: Exhibit a complete Meissner effect and transition sharply from the normal state to the superconducting state at a critical magnetic field \( H_c \).

- **Type II Superconductors**: Exhibit a partial Meissner effect and allow magnetic flux to penetrate in the form of quantized vortices between two critical magnetic fields \( H_{c1} \) and \( H_{c2} \). These materials enter a mixed state where regions of superconductivity coexist with normal regions carrying magnetic flux.

### Applications

The Meissner effect has several practical applications:

1. **Magnetic Levitation**: Used in maglev trains, where superconductors can levitate magnets, reducing friction and allowing high-speed travel.

2. **Magnetic Shielding**: Superconductors can be used to shield sensitive electronic equipment from external magnetic fields.

3. **SQUIDs (Superconducting Quantum Interference Devices)**: Utilize the Meissner effect for extremely sensitive magnetic field measurements, important in medical imaging (MRI) and other applications.

### Conclusion

The Meissner effect is a defining feature of superconductivity, demonstrating the expulsion of magnetic fields from the interior of a superconductor below its critical temperature. This phenomenon is fundamental to the understanding of superconductors and has significant implications for both theoretical research and practical applications. The mathematical description using the London equations provides a clear framework for understanding how superconductors achieve perfect diamagnetism and the exponential decay of magnetic fields within them.


---

preceding: [[gutzwiller approximation]]  


following: [[solid state physics]]

See also: [[quantized vortices]]


See also: [[characteristic length scale]]