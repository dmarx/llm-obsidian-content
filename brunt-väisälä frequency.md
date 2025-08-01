---
date: 1715905105.895943
tags:
- autogenerated
- source__oai
- conversation_id__52aae4ae-b3d5-40cc-864e-7b7e8219356c
- msg_aaa2fa60-d483-4ffb-b289-86807cbc2456
- msg_3c494563-e985-4312-9819-4f67a9b2dc42
- colorclass/energy-dissipation
title: brunt-väisälä frequency
---

**USER**

Brunt-Väisälä Frequency


**ASSISTANT**

### Brunt-Väisälä Frequency

The **Brunt-Väisälä frequency (N)**, also known as the buoyancy frequency, is a fundamental parameter in atmospheric and oceanic sciences that quantifies the stability of a stratified fluid. It describes the frequency at which a displaced parcel of air or water will oscillate vertically within a stably stratified environment.

#### Definition and Formula

The Brunt-Väisälä frequency is defined as:

$$
N = \sqrt{\frac{g}{\theta} \frac{d\theta}{dz}}
$$

where:
- \( N \) is the Brunt-Väisälä frequency,
- \( g \) is the acceleration due to gravity (approximately \( 9.81 \, \text{m/s}^2 \)),
- \( \theta \) is the potential temperature,
- \( \frac{d\theta}{dz} \) is the vertical gradient of potential temperature,
- \( z \) is the height above the surface.

#### Potential Temperature (\(\theta\))

The potential temperature is the temperature that an air parcel would have if it were brought adiabatically to a standard reference pressure (\( p_0 \), typically 1000 hPa):

$$
\theta = T \left( \frac{p_0}{p} \right)^{R/c_p}
$$

where:
- \( T \) is the actual temperature,
- \( p \) is the actual pressure,
- \( R \) is the specific gas constant for dry air (\( R \approx 287 \, \text{J/(kg·K)} \)),
- \( c_p \) is the specific heat capacity at constant pressure (\( c_p \approx 1004 \, \text{J/(kg·K)} \)).

#### Interpretation

- **Stable Stratification**: If \( N^2 > 0 \), the atmosphere is stably stratified. A displaced parcel will oscillate vertically, returning toward its equilibrium position.
- **Neutral Stratification**: If \( N^2 = 0 \), the atmosphere is neutrally stratified, and a displaced parcel will remain in its new position.
- **Unstable Stratification**: If \( N^2 < 0 \), the atmosphere is unstably stratified (convectively unstable), and a displaced parcel will continue to move away from its original position.

#### Oscillations and Vertical Motions

In a stably stratified atmosphere, a vertically displaced air parcel will experience a restoring force due to buoyancy, causing it to oscillate at the Brunt-Väisälä frequency. The oscillation period is given by:

$$
T = \frac{2\pi}{N}
$$

#### Derivation from the Equations of Motion

Consider the linearized equations of motion for vertical displacements in a stably stratified atmosphere:

1. **Vertical Momentum Equation**:
   $$
   \frac{d^2 z'}{dt^2} = -\frac{g}{\theta} \frac{d\theta}{dz} z'
   $$

where \( z' \) is the vertical displacement.

2. **Restoring Force**:
   The restoring buoyancy force acting on the displaced parcel is proportional to the displacement and the vertical gradient of potential temperature.

Combining these, we get a simple harmonic oscillator equation:

$$
\frac{d^2 z'}{dt^2} + N^2 z' = 0
$$

This describes oscillatory motion with angular frequency \( N \), the Brunt-Väisälä frequency.

#### Applications

1. **Atmospheric Stability Analysis**:
   - The Brunt-Väisälä frequency is used to assess atmospheric stability. High values of \( N \) indicate strong stability, while low values suggest weak stability.

2. **Weather Prediction**:
   - Understanding stability helps meteorologists predict phenomena like turbulence, convection, and cloud formation.

3. **Climate Studies**:
   - Stability profiles are crucial for climate models that simulate vertical mixing and energy transport in the atmosphere and oceans.

4. **Oceanography**:
   - In the ocean, the Brunt-Väisälä frequency indicates the stability of the water column, affecting vertical mixing, nutrient transport, and internal wave dynamics.

#### Example Calculation

Consider a layer of the atmosphere with the following properties:
- Temperature (\( T \)) at a height (\( z \)) of 1000 m: 280 K
- Temperature at the surface (0 m): 290 K
- Pressure (\( p \)) at 1000 m: 900 hPa
- Pressure at the surface: 1000 hPa

1. **Calculate Potential Temperature Gradient**:
   - Potential temperature at the surface (\( \theta_0 \)):
     $$
     \theta_0 = 290 \left( \frac{1000}{1000} \right)^{287/1004} = 290 \, \text{K}
     $$
   - Potential temperature at 1000 m (\( \theta_{1000} \)):
     $$
     \theta_{1000} = 280 \left( \frac{1000}{900} \right)^{287/1004} \approx 288.8 \, \text{K}
     $$
   - Potential temperature gradient (\( \frac{d\theta}{dz} \)):
     $$
     \frac{d\theta}{dz} = \frac{288.8 - 290}{1000} = -0.0012 \, \text{K/m}
     $$

2. **Calculate Brunt-Väisälä Frequency**:
   $$
   N = \sqrt{\frac{9.81}{290} \times (-0.0012)} = \sqrt{-0.00004062} = 0 \, \text{s}^{-1}
   $$

In this case, since \( N^2 < 0 \), the atmosphere is convectively unstable at this location.

### Conclusion

The Brunt-Väisälä frequency is a vital parameter for understanding atmospheric and oceanic stability. It quantifies the stability of a stratified fluid and predicts the oscillatory behavior of displaced parcels. By analyzing \( N \), meteorologists and oceanographers can gain insights into vertical motions, turbulence, and the overall dynamical state of the atmosphere and oceans.


---

preceding: [[atmospheric gravity waves]]  


following: [[inversion ([[meteorology]])]]

See also: [[climate models]]


See also: [[gas constant]]


See also: [[energy transport]]


See also: [[specific heat]]


See also: [[specific heat capacity]]


See also: [[gravity waves]]