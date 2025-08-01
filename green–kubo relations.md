---
date: 1724919961.46529
tags:
- autogenerated
- source__oai
- conversation_id__ad2150e2-e599-43ae-9dc4-259111e0c751
- msg_aaa27c95-2a5a-472f-a092-10687f38eeb6
- msg_88ffc0f9-8e38-4771-81bf-0d89e81c4ebf
- colorclass/systems-theory
title: green–kubo relations
---

**USER**

Green–Kubo relations


**ASSISTANT**

### Green–Kubo Relations

The **Green–Kubo relations** are a set of mathematical expressions in statistical mechanics that relate the macroscopic transport coefficients of a system (such as viscosity, thermal conductivity, and electrical conductivity) to the time integrals of the autocorrelation functions of the corresponding microscopic fluxes. These relations are fundamental to the study of nonequilibrium statistical mechanics and provide a rigorous way to derive transport properties from the microscopic dynamics of particles.

#### Overview

The Green–Kubo relations were developed independently by Melville Green and Ryogo Kubo in the 1950s. They are named after these two physicists, who formulated a statistical mechanical approach to connect macroscopic transport coefficients with microscopic fluctuation phenomena, which can be seen as a specific application of the more general **fluctuation-dissipation theorem**.

In essence, the Green–Kubo relations express that the transport coefficients are proportional to the integral over time of the autocorrelation function of the current (flux) that corresponds to the property of interest.

#### General Formulation

Consider a macroscopic system in thermal equilibrium. The Green–Kubo relations are formulated for systems where transport properties, such as diffusion, thermal conductivity, and viscosity, are described by the response of the system to small perturbations. 

A **current** or **flux** $J(t)$ describes the transport of a conserved quantity (such as momentum, energy, or particle number). The **autocorrelation function** of the current $J(t)$ is defined as:

$$
C_{JJ}(t) = \langle J(0) J(t) \rangle,
$$

where:
- $C_{JJ}(t)$ is the autocorrelation function of the current $J(t)$,
- $\langle \cdot \rangle$ denotes an ensemble average over all the microscopic states of the system,
- $J(0)$ is the current at time $t = 0$,
- $J(t)$ is the current at a later time $t$.

The Green–Kubo relations state that the transport coefficient $\kappa$ associated with the flux $J(t)$ is given by:

$$
\kappa = \frac{1}{k_B T} \int_0^\infty \langle J(0) J(t) \rangle \, dt,
$$

where:
- $\kappa$ is the transport coefficient (e.g., diffusion coefficient, viscosity, thermal conductivity),
- $k_B$ is the Boltzmann constant,
- $T$ is the absolute temperature of the system.

The integral on the right-hand side of the equation is the **time integral** of the autocorrelation function, which measures how the flux $J(t)$ at a given time $t$ is correlated with the flux at a reference time $t = 0$. This relation connects microscopic dynamics to macroscopic properties by quantifying how the temporal fluctuations of microscopic currents contribute to macroscopic transport.

#### Specific Green–Kubo Relations for Transport Coefficients

1. **Diffusion Coefficient ($D$)**

For the self-diffusion coefficient $D$ of particles in a fluid, the current $J(t)$ can be associated with the velocity of particles:

$$
J(t) = \sum_{i=1}^N v_i(t),
$$

where $v_i(t)$ is the velocity of particle $i$ at time $t$. The Green–Kubo relation for the self-diffusion coefficient is:

$$
D = \frac{1}{3} \int_0^\infty \langle v_i(0) \cdot v_i(t) \rangle \, dt,
$$

where the factor $\frac{1}{3}$ accounts for the three-dimensional nature of the velocity vector $v_i(t)$. This integral is known as the **velocity autocorrelation function**.

2. **Viscosity ($\eta$)**

For the shear viscosity $\eta$ of a fluid, the current $J(t)$ is the momentum flux (related to the off-diagonal elements of the stress tensor $\sigma_{xy}$, for instance). The Green–Kubo relation for viscosity is:

$$
\eta = \frac{V}{k_B T} \int_0^\infty \langle \sigma_{xy}(0) \sigma_{xy}(t) \rangle \, dt,
$$

where:
- $\eta$ is the shear viscosity,
- $V$ is the volume of the system,
- $\sigma_{xy}(t)$ is the $xy$ component of the stress tensor at time $t$.

3. **Thermal Conductivity ($\kappa$)**

For the thermal conductivity $\kappa$ of a system, the current $J(t)$ is the heat flux vector $q(t)$. The Green–Kubo relation for thermal conductivity is:

$$
\kappa = \frac{V}{k_B T^2} \int_0^\infty \langle q(0) \cdot q(t) \rangle \, dt,
$$

where:
- $\kappa$ is the thermal conductivity,
- $q(t)$ is the heat flux at time $t$.

4. **Electrical Conductivity ($\sigma$)**

For the electrical conductivity $\sigma$ in a conducting medium, the current $J(t)$ is the electric current density. The Green–Kubo relation for electrical conductivity is:

$$
\sigma = \frac{V}{k_B T} \int_0^\infty \langle J(0) \cdot J(t) \rangle \, dt,
$$

where:
- $\sigma$ is the electrical conductivity,
- $J(t)$ is the current density at time $t$.

#### Physical Interpretation and Implications

The Green–Kubo relations provide a direct link between microscopic fluctuations and macroscopic transport phenomena. The key idea is that **transport coefficients** can be derived from equilibrium fluctuations in microscopic quantities, rather than from direct measurements of the macroscopic transport processes.

**Physical interpretation** of the Green–Kubo relations includes:
- **Fluctuation-Dissipation Theorem**: The Green–Kubo relations are specific instances of the fluctuation-dissipation theorem, which relates the response of a system to perturbations (dissipation) to its intrinsic fluctuations at equilibrium.
- **Time Correlations and Relaxation**: The autocorrelation functions describe how fluctuations in microscopic currents decay over time. A slower decay of correlations typically corresponds to lower transport coefficients (e.g., higher viscosity).
- **Computational Approaches**: The Green–Kubo relations are widely used in molecular dynamics simulations and computational physics to calculate transport properties from first principles by evaluating the relevant time-correlation functions.

#### Assumptions and Limitations

The Green–Kubo relations assume:
1. **Linear Response**: The relations are derived under the assumption of a linear response to small perturbations near equilibrium.
2. **Stationarity and Ergodicity**: The system must be stationary (its statistical properties do not change over time) and ergodic (time averages equal ensemble averages).
3. **Long-Time Behavior**: Accurate calculation of transport coefficients requires considering the behavior of autocorrelation functions over long time scales, which can be computationally challenging in practice.

### Conclusion

The **Green–Kubo relations** are foundational results in nonequilibrium statistical mechanics, providing a rigorous connection between microscopic dynamics and macroscopic transport properties. They illustrate how the statistical behavior of microscopic fluctuations underpins macroscopic physical laws, offering a powerful framework for both theoretical analysis and practical computation of transport coefficients in a wide range of systems, from simple fluids to complex materials.


---

preceding: [[onsager reciprocal relations]]  


following: [[fluctuation-dissipation theorem]]

See also: [[molecular dynamics]]


See also: [[computational physics]]