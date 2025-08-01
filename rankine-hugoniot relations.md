---
date: 1724179549.770709
tags:
- autogenerated
- source__oai
- conversation_id__b5133a55-2d8e-4055-8e26-6b03e01a24fa
- msg_aaa2f5fc-a547-4999-adf3-15fdc4a321dc
- msg_346b1fab-edda-4485-b4ec-a705620e1e6c
- colorclass/energy-dissipation
title: rankine-hugoniot relations
---

**USER**

Rankine-Hugoniot relations


**ASSISTANT**

### Rankine-Hugoniot Relations

The **Rankine-Hugoniot relations** are fundamental equations that describe the conservation of mass, momentum, and energy across a shock wave or other types of discontinuities in a compressible fluid. These relations are crucial for understanding the changes in fluid properties such as pressure, density, temperature, and velocity as the fluid passes through a shock.

### Overview

When a shock wave passes through a fluid, it creates a sudden, nearly discontinuous change in the fluid's state. The Rankine-Hugoniot relations provide the mathematical framework to relate the properties of the fluid on either side of the shock front.

### Governing Equations

The Rankine-Hugoniot relations are derived from the fundamental conservation laws applied to a control volume straddling the shock front. These include:

1. **Conservation of Mass**:
   $$
   \rho_1 u_1 = \rho_2 u_2
   $$
   where:
   - \( \rho_1 \) and \( \rho_2 \) are the fluid densities before and after the shock, respectively.
   - \( u_1 \) and \( u_2 \) are the velocities normal to the shock in the pre-shock and post-shock regions, respectively.

2. **Conservation of Momentum**:
   $$
   p_1 + \rho_1 u_1^2 = p_2 + \rho_2 u_2^2
   $$
   where:
   - \( p_1 \) and \( p_2 \) are the pressures before and after the shock, respectively.
   - The term \( \rho u^2 \) represents the momentum flux.

3. **Conservation of Energy**:
   $$
   h_1 + \frac{u_1^2}{2} = h_2 + \frac{u_2^2}{2}
   $$
   where:
   - \( h_1 \) and \( h_2 \) are the specific enthalpies before and after the shock, respectively.
   - The specific enthalpy \( h \) is given by \( h = e + \frac{p}{\rho} \), where \( e \) is the specific internal energy.

These three conservation equations are used to relate the fluid properties on either side of the shock wave.

### Application to a Perfect Gas

For an ideal gas, the specific enthalpy \( h \) can be expressed in terms of the gas constant \( R \) and temperature \( T \) as:
$$
h = c_p T = \frac{\gamma}{\gamma - 1} \frac{p}{\rho}
$$
where:
- \( \gamma = \frac{c_p}{c_v} \) is the ratio of specific heats at constant pressure and constant volume.
- \( c_p \) and \( c_v \) are the specific heats at constant pressure and volume, respectively.

Using these relationships, the Rankine-Hugoniot relations can be expressed as:

1. **Density Ratio**:
   $$
   \frac{\rho_2}{\rho_1} = \frac{(\gamma + 1) M_1^2}{(\gamma - 1) M_1^2 + 2}
   $$
   This equation shows that the density ratio depends on the Mach number \( M_1 \) of the incoming flow and the specific heat ratio \( \gamma \).

2. **Pressure Ratio**:
   $$
   \frac{p_2}{p_1} = 1 + \frac{2\gamma}{\gamma + 1} \left(M_1^2 - 1\right)
   $$
   This equation indicates that the pressure behind the shock is always higher than in front of it, with the ratio increasing as the Mach number increases.

3. **Temperature Ratio**:
   $$
   \frac{T_2}{T_1} = \frac{\left[2\gamma M_1^2 - (\gamma - 1)\right] \left[(\gamma - 1) M_1^2 + 2\right]}{(\gamma + 1)^2 M_1^2}
   $$
   The temperature also increases across the shock wave, reflecting the conversion of kinetic energy into internal energy.

4. **Mach Number Relationship**:
   The post-shock Mach number \( M_2 \) can be related to the pre-shock Mach number \( M_1 \) as:
   $$
   M_2^2 = \frac{(\gamma - 1) M_1^2 + 2}{2\gamma M_1^2 - (\gamma - 1)}
   $$
   This equation shows that the flow behind a normal shock is always subsonic (\( M_2 < 1 \)) if the flow ahead of the shock is supersonic (\( M_1 > 1 \)).

### Example: Normal Shock Wave

Consider a normal shock wave, where the flow is perpendicular to the shock front:

- **Given**: Upstream Mach number \( M_1 \), upstream pressure \( p_1 \), and upstream temperature \( T_1 \).
- **Find**: Downstream properties \( M_2 \), \( p_2 \), \( T_2 \), and \( \rho_2 \).

1. **Calculate the density ratio** using the density ratio equation.
2. **Calculate the pressure ratio** using the pressure ratio equation.
3. **Calculate the temperature ratio** using the temperature ratio equation.
4. **Determine the downstream Mach number** using the Mach number relationship.

### Applications

The Rankine-Hugoniot relations are vital in many areas of fluid dynamics and engineering:

1. **Aerospace Engineering**:
   - Design and analysis of supersonic and hypersonic vehicles, where [[shock waves]] are a critical factor in determining aerodynamic forces, heating, and stability.

2. **Combustion and Explosives**:
   - Understanding [[shock waves]] generated in explosive detonations and high-speed combustion processes.

3. **Astrophysics**:
   - Analysis of [[shock waves]] in astrophysical phenomena, such as supernovae and stellar winds, where rapid changes in temperature, density, and pressure occur.

4. **Fluid Machinery**:
   - Design of turbines, compressors, and nozzles, where [[shock waves]] can impact performance and efficiency.

### Conclusion

The **Rankine-Hugoniot relations** provide a powerful set of tools for analyzing the behavior of compressible fluids across [[shock waves]]. They allow engineers and scientists to predict how critical fluid properties—such as pressure, density, temperature, and velocity—change across a shock front, helping to design and optimize systems that involve high-speed fluid flows. These relations are fundamental to understanding the physics of [[shock waves]] and are applied across a wide range of disciplines, from aerospace engineering to astrophysics.


---

preceding: [[detached shock]]  


following: [[types of discontinuities in a compressible fluid]]

See also: [[gas constant]]


See also: [[specific heat]]


See also: [[kinetic energy]]