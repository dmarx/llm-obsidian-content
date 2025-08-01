---
date: '2025-05-12T05:23:33.763246Z'
tags:
- autogenerated
- source__claude
- conversation_id__1c050a53-3939-42dc-b630-9126ce05d464
- msg_c524cf4f-46f8-4f48-934f-a1e7ab2d11a0
- msg_4586510b-3c10-449e-a1a5-1516cf389000
- colorclass/philosophy-of-language
title: sum rules
---

**USER**

sum rules


**ASSISTANT**

# Sum Rules

Sum rules in physics represent integral constraints on physical quantities that arise from fundamental conservation laws, symmetry principles, or analytical properties of response functions. These mathematical relationships serve as powerful tools for deriving exact results, constraining theoretical models, and validating experimental data across diverse fields including quantum mechanics, condensed matter physics, nuclear physics, and optics.

## Mathematical Foundation

### General Formulation

A sum rule typically takes the form of an integral constraint:

$$\int_{-\infty}^{\infty} f(x) g(x) dx = C$$

where $f(x)$ and $g(x)$ are physical quantities and $C$ is a constant determined by fundamental principles. The domain of integration may be over frequency, energy, momentum, or other relevant variables.

### Derivation from Analytical Properties

Many sum rules emerge from the [[analyticity]] of response functions combined with their asymptotic behavior. Consider a response function $\chi(\omega)$ that is analytic in the upper half-plane. By Cauchy's residue theorem:

$$\oint_C \chi(z) dz = 2\pi i \sum \text{Res}[\chi(z)]$$

For appropriate contours and assuming $\chi(\omega) \to 0$ as $|\omega| \to \infty$, this leads to sum rules relating the integral of $\chi(\omega)$ over the real axis to physical quantities.

### Connection to Kramers-Kronig Relations

Sum rules are intimately connected to the [[Kramers-Kronig relations]]. Evaluating these relations at specific frequencies or taking appropriate limits often yields sum rules. For instance, if $\chi(\omega) = \chi'(\omega) + i\chi''(\omega)$ satisfies the Kramers-Kronig relations:

$$\chi'(0) = \frac{2}{\pi} \mathcal{P} \int_{0}^{\infty} \frac{\chi''(\omega')}{\omega'} d\omega'$$

This is a sum rule relating the static response to the integral over all frequencies.

## Classical Sum Rules in Physics

### f-Sum Rule (Oscillator Strength Sum Rule)

The [[f-sum rule]] in quantum mechanics states that the sum of oscillator strengths for all transitions from a given state equals the number of electrons:

$$\sum_n f_{0n} = N$$

where $f_{0n}$ is the oscillator strength for the transition from the ground state to state $n$, and $N$ is the total number of electrons.

In the continuum limit for optical transitions:

$$\int_{0}^{\infty} \omega \sigma(\omega) d\omega = \frac{\pi N e^2}{2m}$$

where $\sigma(\omega)$ is the optical absorption cross-section.

### Thomas-Reiche-Kuhn Sum Rule

A special case of the f-sum rule, the [[Thomas-Reiche-Kuhn sum rule]] for a single electron states:

$$\sum_{n} (E_n - E_0) |\langle n | \hat{x} | 0 \rangle|^2 = \frac{\hbar^2}{2m}$$

This connects dipole matrix elements to fundamental constants.

### Optical Sum Rules

For the complex dielectric function $\epsilon(\omega) = \epsilon_1(\omega) + i\epsilon_2(\omega)$:

$$\int_{0}^{\infty} \omega \epsilon_2(\omega) d\omega = \frac{\pi}{2} \omega_p^2$$

where $\omega_p = \sqrt{4\pi n e^2/m}$ is the [[plasma frequency]].

This relates the integral of the imaginary part of the dielectric function to the electron density.

### Conductivity Sum Rules

For the optical conductivity $\sigma(\omega) = \sigma_1(\omega) + i\sigma_2(\omega)$:

$$\int_{0}^{\infty} \sigma_1(\omega) d\omega = \frac{\pi n e^2}{2m}$$

This connects the frequency-integrated conductivity to the charge carrier density.

For systems with a [[Drude weight]] $D$:

$$\int_{0}^{\infty} \sigma_1(\omega) d\omega = \frac{\pi n e^2}{2m^*} + \pi D \delta(\omega)$$

where $m^*$ is the effective mass.

## Quantum Mechanical Sum Rules

### Energy-Weighted Sum Rules

In nuclear physics, energy-weighted sum rules constrain collective excitations:

$$\sum_n (E_n - E_0)^k |\langle n | \hat{O} | 0 \rangle|^2 = \langle 0 | [\hat{O}, [\hat{H}, [...[\hat{H}, \hat{O}]...]]] | 0 \rangle$$

where the commutator is nested $k$ times.

For $k = 1$ (Energy-Weighted Sum Rule, EWSR):

$$\sum_n (E_n - E_0) |\langle n | \hat{O} | 0 \rangle|^2 = \frac{1}{2}\langle 0 | [\hat{O}, [\hat{H}, \hat{O}]] | 0 \rangle$$

### Spin Sum Rules

For magnetic systems, spin sum rules relate integrals of magnetic circular dichroism to orbital and spin magnetic moments:

$$\int_{edge} (\mu_+ - \mu_-) d\omega = -\frac{2}{3} n_h \langle L_z \rangle$$

$$\int_{edge} (\mu_+ + \mu_- - 2\mu_0) d\omega = -n_h \langle S_z \rangle$$

where $\mu_\pm$ are X-ray absorption coefficients for different polarizations, and $n_h$ is the number of holes.

### Pauli Sum Rule

In scattering theory, the [[Pauli sum rule]] constrains the neutron-nucleus scattering length:

$$a = a_p + a_c$$

where $a_p$ is the potential scattering length and $a_c$ is the resonance contribution.

## Applications in Specific Fields

### Condensed Matter Physics

#### Spectral Weight Conservation

In strongly correlated systems, spectral weight transfer is constrained by sum rules:

$$\int_{-\infty}^{\infty} A(\omega) d\omega = 1$$

where $A(\omega)$ is the single-particle spectral function.

For the [[Hubbard model]], additional sum rules emerge:

$$\int_{-\infty}^{\infty} \omega A(\omega) d\omega = \langle \hat{H} \rangle / N$$

#### Superconductivity

The [[Ferrell-Glover-Tinkham sum rule]] relates the missing spectral weight in the optical conductivity to the superfluid density:

$$\int_{0}^{\omega_c} [\sigma_n(\omega) - \sigma_s(\omega)] d\omega = \frac{\pi}{2} \rho_s$$

where $\sigma_n$ and $\sigma_s$ are normal and superconducting state conductivities, and $\rho_s$ is the superfluid density.

### Nuclear Physics

#### Giant Resonance Sum Rules

The energy-weighted sum rule for isovector dipole resonances:

$$\sum_n (E_n - E_0) B(E1; 0 \to n) = \frac{9\hbar^2}{8\pi m} \frac{NZ}{A} = 60 \frac{NZ}{A} \text{ MeV fm}^2$$

This relates the total E1 strength to fundamental nuclear properties.

#### Gamow-Teller Sum Rule

For Gamow-Teller transitions:

$$S_+ - S_- = 3(N - Z)$$

where $S_\pm$ are the total GT transition strengths in the $\beta^\pm$ directions.

### Particle Physics

#### Adler Sum Rule

In deep inelastic scattering, the [[Adler sum rule]] relates structure functions:

$$\int_{0}^{1} \frac{dx}{x} [F_2^{\nu p}(x,Q^2) - F_2^{\bar{\nu} p}(x,Q^2)] = 2$$

This is independent of $Q^2$ (momentum transfer) and tests fundamental aspects of QCD.

#### Bjorken Sum Rule

For polarized deep inelastic scattering:

$$\int_{0}^{1} dx [g_1^p(x) - g_1^n(x)] = \frac{1}{6}|g_A/g_V|$$

where $g_1^{p,n}$ are proton and neutron spin structure functions, and $g_A/g_V$ is the axial-vector coupling ratio.

## Derivation Techniques

### Method of Moments

Sum rules often emerge from calculating moments of distributions:

$$\mu_n = \int_{-\infty}^{\infty} x^n f(x) dx$$

The $n$-th moment relates to the $n$-th derivative of the characteristic function at zero.

### Commutator Methods

In quantum mechanics, nested commutators generate sum rules:

$$\langle [A, [H, B]] \rangle = \sum_n (E_n - E_0)^2 |\langle n | A | 0 \rangle|^2 |\langle 0 | B | n \rangle|^2$$

This technique systematically produces higher-order sum rules.

### Asymptotic Analysis

Analyzing the high-frequency behavior of response functions yields sum rules:

$$\lim_{\omega \to \infty} \omega^2 \chi(\omega) = -n$$

Combined with Kramers-Kronig relations, this constrains the entire frequency dependence.

## Computational Methods

### Numerical Verification

```python
def verify_f_sum_rule(energies, oscillator_strengths, n_electrons, tolerance=1e-6):
    """
    Verify the f-sum rule for a discrete spectrum.
    
    Parameters:
    -----------
    energies : array
        Transition energies
    oscillator_strengths : array
        Oscillator strengths for each transition
    n_electrons : int
        Number of electrons in the system
    tolerance : float
        Acceptable deviation from the exact sum rule
    
    Returns:
    --------
    is_satisfied : bool
        Whether the sum rule is satisfied within tolerance
    deviation : float
        Actual deviation from the sum rule
    """
    total_strength = np.sum(oscillator_strengths)
    deviation = abs(total_strength - n_electrons)
    is_satisfied = deviation < tolerance
    
    return is_satisfied, deviation
```

### Spectral Weight Analysis

```python
def compute_spectral_weight_transfer(omega, sigma_normal, sigma_sc, omega_cutoff):
    """
    Compute spectral weight transfer in superconductors using the FGT sum rule.
    
    Parameters:
    -----------
    omega : array
        Frequency array
    sigma_normal : array
        Normal state optical conductivity
    sigma_sc : array
        Superconducting state optical conductivity
    omega_cutoff : float
        Cutoff frequency for integration
    
    Returns:
    --------
    missing_weight : float
        Missing spectral weight in the superconducting state
    superfluid_density : float
        Inferred superfluid density
    """
    # Find indices up to cutoff frequency
    cutoff_idx = np.argmax(omega > omega_cutoff)
    
    # Compute missing spectral weight
    missing_weight = np.trapz(sigma_normal[:cutoff_idx] - sigma_sc[:cutoff_idx], 
                              omega[:cutoff_idx])
    
    # Infer superfluid density using FGT sum rule
    superfluid_density = 2 * missing_weight / np.pi
    
    return missing_weight, superfluid_density
```

### Sum Rule Fitting

```python
def fit_with_sum_rule_constraint(data, model_func, sum_rule_value):
    """
    Fit a model to data while enforcing a sum rule constraint.
    
    Parameters:
    -----------
    data : tuple (x, y)
        Input data points
    model_func : function
        Model function to fit
    sum_rule_value : float
        Value the integral of the model must equal
    
    Returns:
    --------
    params : array
        Fitted parameters
    """
    x, y = data
    
    def objective(params):
        # Usual least-squares term
        y_model = model_func(x, params)
        chi_squared = np.sum((y - y_model)**2)
        
        # Sum rule constraint term
        integral = np.trapz(y_model, x)
        constraint_violation = (integral - sum_rule_value)**2
        
        # Weight the constraint appropriately
        weight = len(y)  # Scale with data size
        
        return chi_squared + weight * constraint_violation
    
    # Initial parameter guess
    initial_params = np.ones(model_func.num_params)
    
    # Optimize with constraint
    result = minimize(objective, initial_params, method='Nelder-Mead')
    
    return result.x
```

## Advanced Topics

### Non-Local Sum Rules

For systems with long-range interactions, non-local sum rules emerge:

$$\int \int K(x,y) \rho(x) \rho(y) dx dy = C$$

where $K(x,y)$ is an interaction kernel and $\rho(x)$ is a density distribution.

### Finite-Size Effects

In finite systems, sum rules require corrections:

$$\sum_{n} f_{0n} = N - \Delta N(L)$$

where $\Delta N(L)$ accounts for finite-size effects in a system of size $L$.

### Temperature-Dependent Sum Rules

At finite temperature, sum rules incorporate thermal factors:

$$\int_{0}^{\infty} \sigma_1(\omega) \tanh\left(\frac{\hbar\omega}{2k_B T}\right) d\omega = \frac{\pi n e^2}{2m}$$

This reduces to the zero-temperature form as $T \to 0$.

### Quantum Hall Sum Rules

In the quantum Hall regime, topological sum rules emerge:

$$\int_{-\infty}^{\infty} \frac{d\sigma_{xy}}{d\mu} d\mu = \frac{e^2}{h} \Delta \nu$$

where $\sigma_{xy}$ is the Hall conductivity and $\Delta \nu$ is the change in filling factor.

## Symbolic Notation and Formalism

We can establish a comprehensive notation for sum rule analysis:

- Let $\mathcal{S}_n[f]$ denote the $n$-th moment sum rule for function $f$
- Let $\mathcal{W}[A,B]$ represent the spectral weight between frequencies $A$ and $B$
- Let $\mathcal{O}_k$ be the $k$-th order response operator

The general sum rule can be written as:

$$\mathcal{S}_n[\mathcal{O}_k] = \mathcal{C}_n^k$$

where $\mathcal{C}_n^k$ is a constant determined by commutators and system properties.

## Modern Developments

### Machine Learning Applications

Sum rules serve as physics-informed constraints in machine learning models:
- Ensuring physical consistency in neural network predictions
- Constraining generative models for spectral functions
- Validating data-driven models against fundamental principles

### Many-Body Localization

In disordered systems, modified sum rules characterize localization:

$$\lim_{t \to \infty} \frac{1}{t} \int_0^t \langle \hat{O}(t') \hat{O}(0) \rangle dt' = \sum_{\alpha} |O_{\alpha}|^2 \rho_{\alpha}$$

where the sum runs over localized eigenstates $\alpha$ with occupation $\rho_{\alpha}$.

### Strongly Correlated Systems

Novel sum rules emerge in systems with strong correlations:
- Modified f-sum rules in high-temperature superconductors
- Spectral weight transfer in Mott transitions
- Holographic sum rules from AdS/CFT correspondence

## Applications Beyond Traditional Physics

### Complex Networks

Sum rules constrain properties of complex networks:
- Degree distribution moments
- Centrality measures
- Community structure indicators

### Economics and Finance

Market sum rules relate:
- Price volatility to trading volume
- Option prices across strike prices
- Risk measures across portfolios

### Biological Systems

Conservation principles yield biological sum rules:
- Mass balance in metabolic networks
- Energy conservation in ecological systems
- Information-theoretic constraints on neural coding

## Related Concepts

- [[Kramers-Kronig Relations]]: Causality constraints on response functions
- [[Conservation Laws]]: Fundamental principles underlying sum rules
- [[Oscillator Strength]]: Key quantity in optical sum rules
- [[Spectral Function]]: Object of study in many sum rules
- [[Ward-Takahashi Identities]]: Gauge theory analogs of sum rules
- [[Causality]]: Physical principle constraining response functions
- [[Linear Response Theory]]: Framework generating many sum rules
- [[Moment Problems]]: Mathematical theory of moment constraints


---

preceding: [[kramers-kronig relations]]  


following: [[ward-takahashi identities]]

See also: [[condensed matter physics]]


See also: [[generative models]]