---
date: '2025-02-09T22:48:36.828903Z'
tags:
- autogenerated
- source__claude
- conversation_id__8e97c5b7-ebdd-42a1-9658-da2993fb577a
- msg_b8d4bcb6-4137-410f-872e-25a50b5a847f
- msg_233715bd-3ad2-4bb9-a23f-87507fcca915
- colorclass/reference-frame
title: space velocity
---

**USER**

Space Velocity


**ASSISTANT**

# Space Velocity

The [[space velocity]] of a star describes its complete motion through three-dimensional space relative to a specified reference frame, typically the [[Local Standard of Rest]] (LSR) or the [[Solar System Barycenter]] (SSB).

## Mathematical Formalization

Let $\vec{v}$ represent the total space velocity vector. In its most general form:

```
\vec{v} = \vec{v}_r + \vec{v}_t
```
where:
- $\vec{v}_r$ is the [[radial velocity]] component
- $\vec{v}_t$ is the [[transverse velocity]] component

### Component Representation

In [[Galactic coordinates]], space velocity is commonly decomposed into:
```
(U, V, W) = (v_x, v_y, v_z)
```
where:
- U: velocity toward Galactic center
- V: velocity in direction of Galactic rotation
- W: velocity toward North Galactic Pole

## Velocity Transformations

### [[Heliocentric Correction]]

Converting from observed to heliocentric velocities:
```
\vec{v}_{helio} = \vec{v}_{obs} + \vec{v}_{Earth}
```

### [[LSR Correction]]

```
\vec{v}_{LSR} = \vec{v}_{helio} + \vec{v}_{solar}
```
where $\vec{v}_{solar}$ is the [[solar motion]] relative to the LSR.

## Measurement Methods

### Complete Space Motion

Requires three independent measurements:
1. [[Proper Motion]] (μ_α, μ_δ)
2. [[Radial Velocity]] (v_r)
3. [[Parallax]] (π) for distance

### [[Velocity Conversion]]

For proper motion to physical velocity:
```
v_t = 4.74 \frac{μ}{\pi} d
```
where:
- v_t is in km/s
- μ is in arcsec/year
- d is distance in parsecs

## Applications

### [[Stellar Kinematics]]

Analysis using:
- [[Toomre Diagram]]
- [[Bottlinger Diagram]]
- [[UV Velocity Plot]]

### [[Population Analysis]]

Identification of:
- [[Thin Disk]] stars
- [[Thick Disk]] stars
- [[Halo Stars]]
- [[Hypervelocity Stars]]

## Statistical Properties

### [[Velocity Dispersion]]

For a stellar population:
```
σ_i² = \frac{1}{N-1} \sum_{j=1}^N (v_{i,j} - \bar{v}_i)²
```
where i denotes U, V, or W component.

### [[Velocity Ellipsoid]]

Characterized by:
- Principal axes
- [[Vertex Deviation]]
- [[Asymmetric Drift]]

## Modern Applications

### [[Galactic Archaeology]]

Used to study:
- [[Moving Groups]]
- [[Stellar Streams]]
- [[Merger History]]

### [[Dynamical Studies]]

Applications in:
- [[Escape Velocity]] determination
- [[Dark Matter]] distribution
- [[Galactic Potential]] modeling

## Error Analysis

Key considerations:
- [[Covariance Matrix]] of observables
- [[Error Propagation]]
- [[Selection Effects]]
- [[Systematic Biases]]


---

preceding: [[proper motion]]  


following: [[local standard of rest]]

See also: [[dissipation as consumption]]


See also: [[reference frame]]


See also: [[computational thermodynamics]]