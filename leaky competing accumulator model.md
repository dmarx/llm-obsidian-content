---
date: 1720988120.429707
tags:
- autogenerated
- source__oai
- conversation_id__061738c3-69c1-49e6-9274-bc50cd27a92d
- msg_aaa2f522-b64d-4610-8545-3b6c6f9c36f9
- msg_684e04d5-dee1-4017-95cb-098ce5e8ddea
- colorclass/decision-making-processes
title: leaky competing accumulator model
---

**USER**

the leaky competing accumulator model


**ASSISTANT**

The Leaky Competing Accumulator (LCA) Model is a cognitive model used to describe decision-making processes, particularly in scenarios involving multiple alternatives. The LCA model extends traditional accumulator models by incorporating leakage and competition dynamics, providing a more realistic representation of how decisions are made under time pressure and uncertainty.

### Core Components

1. **Evidence Accumulation**: Similar to other accumulator models, the LCA model posits that evidence for each option accumulates over time.
2. **Leakage**: Accumulated evidence decays over time, reflecting the loss of information or the imperfect retention of evidence.
3. **Competition**: Accumulators for different options inhibit each other, modeling the competition between alternatives.

### Mathematical Formalism

The dynamics of the LCA model are typically described using a set of coupled differential equations. For a two-alternative forced-choice task, let $x_1(t)$ and $x_2(t)$ represent the accumulated evidence for options 1 and 2, respectively. The differential equations governing the process are:

$$
\frac{dx_1}{dt} = v_1 - \lambda x_1 - \gamma x_2 + \sigma \eta_1(t)
$$

$$
\frac{dx_2}{dt} = v_2 - \lambda x_2 - \gamma x_1 + \sigma \eta_2(t)
$$

where:
- $v_1$ and $v_2$ are the drift rates (mean rates of evidence accumulation) for options 1 and 2.
- $\lambda$ is the leakage rate, reflecting the decay of accumulated evidence over time.
- $\gamma$ is the competition parameter, representing the inhibitory interaction between the two accumulators.
- $\sigma$ is the noise coefficient, and $\eta_1(t)$ and $\eta_2(t)$ are independent Gaussian white noise processes.

### Decision Process

A decision is made when the accumulated evidence for one of the options reaches a predefined threshold, $a$. Let’s denote the thresholds for options 1 and 2 by $a_1$ and $a_2$ respectively. The process can be described as:

- **Option 1 is chosen** if $x_1(t) \geq a_1$.
- **Option 2 is chosen** if $x_2(t) \geq a_2$.

### Key Equations

The LCA model builds on key equations from other accumulator models but adds terms for leakage and competition:

1. **Evidence Accumulation**:
   $$
   \frac{dx_i}{dt} = v_i - \lambda x_i - \gamma \sum_{j \neq i} x_j + \sigma \eta_i(t), \quad i = 1, 2
   $$

2. **Probability of Choosing Option 1**:
   Given the competitive and leaky nature of the model, the probability distribution of choosing option 1 can be complex and typically requires numerical methods or simulations to solve.

3. **Mean Decision Time**:
   Like the probability of choosing an option, the mean decision time can also be derived through simulations or approximations. The model can predict faster decisions with higher drift rates and slower decisions with higher leakage and competition parameters.

### Applications

The LCA model is versatile and has been applied in various decision-making scenarios, such as:

1. **Perceptual Decision-Making**: Tasks where participants decide between different sensory stimuli under varying levels of noise and ambiguity.
2. **Economic Choices**: Decisions involving selecting between different monetary rewards or consumer products.
3. **Cognitive Control Tasks**: Scenarios where individuals must inhibit automatic responses to make goal-directed decisions, such as the Stroop task.

### Example: Perceptual Decision-Making Task

Consider a task where a participant must decide whether a noisy visual stimulus represents a horizontal or vertical line:

1. **Evidence Accumulation**: The visual information accumulates evidence in favor of either the horizontal or vertical option.
2. **Leakage**: As time progresses, some of the accumulated evidence decays, reflecting the participant's imperfect memory of the stimulus.
3. **Competition**: Evidence for the horizontal line inhibits the accumulation of evidence for the vertical line and vice versa.

The differential equations for this scenario would be:

$$
\frac{dx_H}{dt} = v_H - \lambda x_H - \gamma x_V + \sigma \eta_H(t)
$$

$$
\frac{dx_V}{dt} = v_V - \lambda x_V - \gamma x_H + \sigma \eta_V(t)
$$

where:
- $x_H(t)$ and $x_V(t)$ represent the accumulated evidence for the horizontal and vertical lines.
- $v_H$ and $v_V$ are the drift rates for the horizontal and vertical lines.
- $\lambda$ is the leakage rate.
- $\gamma$ is the competition parameter.
- $\sigma \eta_H(t)$ and $\sigma \eta_V(t)$ are the noise terms.

### Visualization

A typical visualization of the LCA model involves plotting the trajectories of the accumulated evidence over time. The plot might look something like this:

```plaintext
Evidence
  ^
  |                                    * Decision threshold (option 1)
  |                                 *
  |                              *
  |                           *
  |                        *
  |                     *
  |                  *
  |               *
  |            *
  |         *
  |      *
  |   *
  |*
  +-------------------------------------> Time
  *   *   *   *   *   *   *   *   *   *   *   *   *   *  *
- |  * Start
  |
  |
  |
  |
  |
  |
  |
  |  
  *   *   *   *   *   *   *   *   *   *   *   *   *   *  *
  * Decision threshold (option 2)
```

In this diagram, the path represents the stochastic evidence accumulation process starting from the initial point. The decision is made when the path hits either the upper or lower threshold.

### Conclusion

The Leaky Competing Accumulator (LCA) Model offers a sophisticated and biologically plausible framework for understanding decision-making processes. By incorporating elements of leakage and competition, it captures the dynamic and interactive nature of decision-making in real-world scenarios. Its applications span a wide range of fields, making it a valuable tool for researchers studying cognitive processes and decision behavior.


---

preceding: [[drift diffusion model]]  


following: [[computational models of working attention, motivation, and decision making]]

See also: [[decision-making processes]]


See also: [[reframing the model using the leaky competing accumulator model]]


See also: [[proposed constraints on graph topology to represent neuroanatomical functional differentiation]]