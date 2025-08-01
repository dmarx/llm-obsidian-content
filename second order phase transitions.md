---
date: 1716303864.74622
tags:
- autogenerated
- source__oai
- conversation_id__a808cc68-12aa-40bd-ac4d-430e88f727f4
- msg_aaa2dea0-2951-46e4-bd03-28f6c8bc0a5a
- msg_d2a689a7-d44c-433b-aa59-63f5fb87d528
- colorclass/systems-theory
title: second order phase transitions
---

**USER**

second order phase transitions


**ASSISTANT**

Second-order phase transitions, also known as continuous or continuous-symmetry-breaking transitions, are characterized by a continuous change in the order parameter and the absence of latent heat. These transitions are associated with critical phenomena, where physical properties exhibit power-law behavior near the critical point.

### Key Characteristics

1. **Order Parameter Continuity:**
   The order parameter, which describes the degree of order in the system, changes continuously at the transition. For example, in the ferromagnetic transition, the magnetization gradually decreases to zero as the temperature approaches the critical temperature \(T_c\) from below.

2. **No Latent Heat:**
   Unlike first-order phase transitions, second-order transitions do not involve latent heat. The transition occurs without an abrupt change in entropy or energy.

3. **Divergence of Correlation Length:**
   Near the critical point, the correlation length \(\xi\), which measures the distance over which fluctuations in the order parameter are correlated, diverges:
   $$
   \xi \sim |T - T_c|^{-\nu}
   $$
   where \(\nu\) is a critical exponent.

4. **Critical Exponents and Scaling Laws:**
   Physical quantities near the critical point follow power-law behaviors characterized by critical exponents. Common critical exponents include:
   - \(\alpha\) for specific heat \(C \sim |T - T_c|^{-\alpha}\)
   - \(\beta\) for the order parameter \(\phi \sim (T_c - T)^{\beta}\)
   - \(\gamma\) for susceptibility \(\chi \sim |T - T_c|^{-\gamma}\)
   - \(\delta\) for the order parameter near \(T_c\) when subjected to an external field \(H \sim \phi^{\delta}\)

### Examples of Second-Order Phase Transitions

1. **Ferromagnetic Transition:**
   In a ferromagnetic material, the magnetization \(M\) serves as the order parameter. The free energy \(F(M, T)\) near the critical temperature \(T_c\) is often approximated as:
   $$
   F(M, T) = a(T) M^2 + b M^4
   $$
   where \(a(T) = a_0 (T - T_c)\) and \(b > 0\). For \(T > T_c\), the system is in the paramagnetic phase (\(M = 0\)), and for \(T < T_c\), the system exhibits spontaneous magnetization (\(M \neq 0\)).

2. **Superconducting Transition:**
   The transition of a material to a superconducting state at the critical temperature \(T_c\) is a second-order phase transition. The order parameter is the superconducting gap parameter \(\Delta\), which continuously goes to zero as \(T\) approaches \(T_c\) from below.

3. **Liquid-Gas Critical Point:**
   At the critical point of a liquid-gas transition, the distinction between liquid and gas phases disappears. The density difference between the liquid and gas phases serves as the order parameter, which vanishes continuously at the critical temperature.

### Landau Theory of Second-Order Phase Transitions

Landau theory provides a phenomenological framework to describe second-order phase transitions. The free energy \(F(\phi, T)\) is expanded as a power series in the order parameter \(\phi\):
$$
F(\phi, T) = F_0 + a(T) \phi^2 + b \phi^4 + \ldots
$$
where \(a(T)\) changes sign at the critical temperature \(T_c\):
$$
a(T) = a_0 (T - T_c)
$$
The equilibrium value of \(\phi\) minimizes the free energy:
$$
\frac{\partial F}{\partial \phi} = 0 \quad \Rightarrow \quad a(T) \phi + 2b \phi^3 = 0
$$
For \(T > T_c\), \(a(T) > 0\), and the only solution is \(\phi = 0\). For \(T < T_c\), \(a(T) < 0\), leading to:
$$
\phi = \pm \sqrt{\frac{|a(T)|}{2b}} \sim (T_c - T)^{\frac{1}{2}}
$$

### Renormalization Group Theory

Renormalization group (RG) theory is a powerful tool for analyzing second-order phase transitions. It provides insights into how physical quantities transform under changes of length scales and helps determine the universality classes of critical behavior. The key idea is to progressively integrate out short-wavelength fluctuations and study how the system's behavior evolves under rescaling.

### Conclusion

Second-order phase transitions are marked by continuous changes in the order parameter, absence of latent heat, and critical phenomena characterized by diverging correlation lengths and power-law behavior of physical quantities. These transitions are well-described by Landau theory and further elucidated by renormalization group theory. For more in-depth analysis, refer to [[Phase Transition|Phase Transition Dynamics]] and [[Critical Phenomena|Critical Phenomena and Scaling]].


---

preceding: [[relate [[transcritical bifurcation]] to the emergence of collective behavior following a phase transition]]  


following: [[frechet derivatives]]

See also: [[second-order phase transitions]]


See also: [[critical phenomena]]


See also: [[specific heat]]


See also: [[collective behavior]]


See also: [[universality classes]]


See also: [[free energy]]


See also: [[correlation length]]