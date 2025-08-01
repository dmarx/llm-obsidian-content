---
date: 1717868279.489673
tags:
- autogenerated
- source__oai
- conversation_id__56255cdd-bab3-489a-ad3a-b9c02d166fcf
- msg_aaa20095-4ae4-4e2c-ab87-a54127cddd7c
- msg_65ae4be7-68bf-404b-ade2-59b2ea2cb1f6
- colorclass/vector-space
title: lemniscate of bernoulli
---

**USER**

lemniscate of Bernoulli


**ASSISTANT**

The Lemniscate of Bernoulli is a special case of the Cassini oval where the product of the distances to the two fixed points (foci) is equal to the square of the distance between the foci. This specific curve resembles a figure-eight or an infinity symbol.

### Definition and Equation

For the Lemniscate of Bernoulli, the defining condition is:

$$
|PF_1| \cdot |PF_2| = c^2
$$

where \( F_1 \) and \( F_2 \) are the foci located at \( (-c, 0) \) and \( (c, 0) \), respectively. 

The Cartesian equation of the Lemniscate of Bernoulli can be derived similarly to that of a Cassini oval with \( a = c \):

$$
\left( (x + c)^2 + y^2 \right) \left( (x - c)^2 + y^2 \right) = c^4
$$

Expanding and simplifying:

$$
(x^2 + y^2 + c^2 + 2cx)(x^2 + y^2 + c^2 - 2cx) = c^4
$$

Using the identity \((A + B)(A - B) = A^2 - B^2\):

$$
(x^2 + y^2 + c^2)^2 - (2cx)^2 = c^4
$$

$$
(x^2 + y^2 + c^2)^2 - 4c^2x^2 = c^4
$$

Expanding and combining terms:

$$
(x^2 + y^2)^2 + 2c^2(x^2 + y^2) + c^4 - 4c^2x^2 = c^4
$$

Subtracting \( c^4 \) from both sides:

$$
(x^2 + y^2)^2 + 2c^2(x^2 + y^2 - 2x^2) = 0
$$

Simplifying:

$$
(x^2 + y^2)^2 = 2c^2(x^2 - y^2)
$$

This is the standard form of the Lemniscate of Bernoulli.

### Polar Coordinates

The equation in polar coordinates, with the origin at the midpoint between the foci, is:

$$
r^2 = 2c^2 \cos(2\theta)
$$

where \( r \) is the radial distance from the origin and \( \theta \) is the polar angle.

### Properties

#### Symmetry

The Lemniscate of Bernoulli is symmetric with respect to both the x-axis and the y-axis.

#### Self-Intersection

The curve intersects itself at the origin, which is the midpoint between the two foci.

#### Area

The area enclosed by the Lemniscate of Bernoulli can be computed using elliptic integrals. The total area \( A \) of the lemniscate is:

$$
A = 2c^2 \int_{-1}^{1} \sqrt{1 - u^2} \, du
$$

Substituting \( u = \sin \phi \), \( du = \cos \phi \, d\phi \):

$$
A = 2c^2 \int_{-\frac{\pi}{2}}^{\frac{\pi}{2}} \cos^2 \phi \, d\phi
$$

Using the double-angle identity for cosine:

$$
\cos^2 \phi = \frac{1 + \cos(2\phi)}{2}
$$

The integral becomes:

$$
A = 2c^2 \int_{-\frac{\pi}{2}}^{\frac{\pi}{2}} \frac{1 + \cos(2\phi)}{2} \, d\phi
$$

$$
A = c^2 \int_{-\frac{\pi}{2}}^{\frac{\pi}{2}} (1 + \cos(2\phi)) \, d\phi
$$

Evaluating the integrals separately:

$$
A = c^2 \left[ \phi + \frac{\sin(2\phi)}{2} \right]_{-\frac{\pi}{2}}^{\frac{\pi}{2}}
$$

Since \( \sin(2\phi) \) is zero at both \( \frac{\pi}{2} \) and \( -\frac{\pi}{2} \):

$$
A = c^2 \left[ \phi \right]_{-\frac{\pi}{2}}^{\frac{\pi}{2}} = c^2 \left( \frac{\pi}{2} - (-\frac{\pi}{2}) \right) = c^2 \pi
$$

Therefore, the area enclosed by the Lemniscate of Bernoulli is:

$$
A = \pi c^2
$$

### Applications

#### Elliptic Integrals

Elliptic integrals often arise in the context of calculating arc lengths and areas of the Lemniscate of Bernoulli. These integrals are more general functions that cannot be expressed in terms of elementary functions.

#### Physics and Engineering

In physics and engineering, the lemniscate appears in problems involving potential fields and the study of stability regions in dynamical systems.

#### Complex Analysis

In complex analysis, the lemniscate is related to the loci of points equidistant from two fixed points in the complex plane, providing insight into conformal mappings and potential theory.

### Visual Representation

To visualize the Lemniscate of Bernoulli, one can use various software tools. Here’s an example using Python and matplotlib:

```python
import numpy as np
import matplotlib.pyplot as plt

# Parameters
c = 1  # Adjust for different lemniscates

# Polar coordinates for the lemniscate
theta = np.linspace(0, 2 * np.pi, 1000)
r = c * np.sqrt(2 * np.cos(2 * theta))

# Convert to Cartesian coordinates
x = r * np.cos(theta)
y = r * np.sin(theta)

# Plot
plt.plot(x, y)
plt.title("Lemniscate of Bernoulli")
plt.xlabel("x")
plt.ylabel("y")
plt.axis("equal")
plt.grid(True)
plt.show()
```

This code generates a plot of the Lemniscate of Bernoulli for \( c = 1 \).

---

This detailed exploration of the Lemniscate of Bernoulli covers its definition, derivations, properties, and applications, providing a comprehensive understanding suitable for advanced mathematical studies.


---

preceding: [[by all means, please elaborate]]  


following: [[elliptic integrals]]

See also: [[complex analysis]]