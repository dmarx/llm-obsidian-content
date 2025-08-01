---
date: 1718162429.517923
tags:
- autogenerated
- source__oai
- conversation_id__18aef735-d044-4209-927f-ec249ab3595f
- msg_aaa22a07-1ee0-48ad-94fe-757447a392aa
- msg_c30e9916-87ed-4256-9806-573d123acc73
- colorclass/system-dynamics
title: nyquist stability criterion
---

**USER**

Nyquist Stability Criterion


**ASSISTANT**

### Nyquist Stability Criterion

The Nyquist Stability Criterion is a graphical method used in control theory to determine the stability of a closed-loop system by examining its open-loop frequency response. It provides a way to assess the stability of a feedback system by mapping the contour of the [[open-loop transfer function]] in the complex plane.

### Key Concepts

1. **Open-Loop Transfer Function**: The product of the plant transfer function \( G(s) \) and the controller transfer function \( H(s) \), denoted as \( L(s) = G(s)H(s) \).
2. **Nyquist Plot**: A plot of the complex values of the [[open-loop transfer function]] \( L(j\omega) \) as the frequency \( \omega \) varies from \(-\infty\) to \( \infty \).
3. **Encirclements**: The Nyquist plot's encirclements of the critical point \(-1 + j0\) in the complex plane are crucial for determining stability.

### Nyquist Stability Criterion

The Nyquist Stability Criterion states that the stability of the closed-loop system can be determined by the number of clockwise and counterclockwise encirclements of the point \(-1 + j0\) on the Nyquist plot.

#### Mathematical Formulation

Let \( P \) be the number of poles of \( L(s) \) in the right half-plane (RHP), and \( N \) be the number of clockwise encirclements of the point \(-1 + j0\) by the Nyquist plot of \( L(j\omega) \). The number of zeros \( Z \) of the characteristic equation in the RHP (which correspond to the closed-loop poles) is given by:

$$
Z = N + P.
$$

For the system to be stable, all the closed-loop poles must lie in the left half-plane (LHP). Therefore, for stability:

$$
Z = 0.
$$

This implies that the number of clockwise encirclements of \(-1 + j0\) must equal the number of poles of \( L(s) \) in the RHP, but with opposite signs:

$$
N = -P.
$$

### Steps for Applying the Nyquist Stability Criterion

1. **Determine the Open-Loop Transfer Function**:
   Identify the [[open-loop transfer function]] \( L(s) = G(s)H(s) \).

2. **Construct the Nyquist Plot**:
   Plot \( L(j\omega) \) in the complex plane for \( \omega \) varying from \(-\infty\) to \( \infty \).

3. **Identify Encirclements**:
   Count the number of clockwise and counterclockwise encirclements of the critical point \(-1 + j0\).

4. **Determine Stability**:
   Use the Nyquist Stability Criterion formula \( Z = N + P \) to determine the number of RHP zeros. For stability, \( Z \) must be zero, implying \( N = -P \).

### Example: Nyquist Plot for a Simple System

Consider the [[open-loop transfer function]]:

$$
L(s) = \frac{10}{s(s+1)(s+2)}.
$$

#### Step 1: Determine the Open-Loop Transfer Function

The transfer function is already given as \( L(s) = \frac{10}{s(s+1)(s+2)} \).

#### Step 2: Construct the Nyquist Plot

To construct the Nyquist plot, evaluate \( L(j\omega) \) over a range of frequencies:

$$
L(j\omega) = \frac{10}{j\omega (j\omega + 1)(j\omega + 2)}.
$$

Evaluate at key points:
- At \( \omega = 0 \), \( L(j0) = \infty \).
- As \( \omega \to \infty \), \( L(j\omega) \to 0 \).
- At intermediate frequencies, compute \( L(j\omega) \) and plot the points in the complex plane.

#### Step 3: Identify Encirclements

Examine the Nyquist plot and count the number of times it encircles \(-1 + j0\):
- If the plot encircles \(-1 + j0\) in a clockwise direction, count as positive encirclements.
- If the plot encircles \(-1 + j0\) in a counterclockwise direction, count as negative encirclements.

#### Step 4: Determine Stability

For the given transfer function, there are no poles in the RHP (\( P = 0 \)). Therefore, for stability, the Nyquist plot should not encircle \(-1 + j0\) (\( N = 0 \)).

### Nyquist Plot Analysis: Detailed Example

Consider the [[open-loop transfer function]]:

$$
L(s) = \frac{K}{s(s+1)(s+2)},
$$

where \( K \) is a gain to be determined.

#### Step 1: Constructing the Nyquist Plot

1. **Frequency Response**:
   - Evaluate \( L(j\omega) \) for various frequencies \( \omega \).

2. **Low-Frequency Behavior**:
   - As \( \omega \to 0 \), \( L(j\omega) \approx \frac{K}{0} = \infty \).

3. **High-Frequency Behavior**:
   - As \( \omega \to \infty \), \( L(j\omega) \to 0 \).

4. **Intermediate Frequencies**:
   - Calculate \( L(j\omega) \) at several points to trace the Nyquist plot.

#### Step 2: Plotting

1. **Plot \( L(j\omega) \) for \( \omega \geq 0 \)**:
   - Plot the real and imaginary parts of \( L(j\omega) \) on the complex plane.

2. **Symmetry for \( \omega < 0 \)**:
   - The Nyquist plot for negative frequencies is the mirror image (with respect to the real axis) of the plot for positive frequencies.

#### Step 3: Counting Encirclements

1. **Identify Encirclements of \(-1 + j0\)**:
   - Count how many times the Nyquist plot encircles \(-1 + j0\).

2. **Determine the Direction of Encirclements**:
   - Clockwise encirclements are positive; counterclockwise encirclements are negative.

#### Step 4: Stability Criterion

1. **Poles in the RHP (\( P \))**:
   - For the given transfer function, \( L(s) \) has no poles in the RHP (\( P = 0 \)).

2. **Encirclements (\( N \))**:
   - Ensure that the number of encirclements \( N \) of \(-1 + j0\) by the Nyquist plot is zero.

### Conclusion

The Nyquist Stability Criterion provides a powerful graphical tool for determining the stability of closed-loop control systems by analyzing their open-loop frequency response. By constructing the Nyquist plot and examining encirclements of the critical point \(-1 + j0\), engineers can assess system stability and design robust control systems. For further exploration, see topics such as [[Bode Plot Analysis]], [[Root Locus Analysis]], and [[Stability Analysis in Control Systems]].


---

preceding: [[bode plot analysis]]  


following: [[root locus analysis]]

See also: [[transfer function]]


See also: [[control theory]]