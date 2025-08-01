---
date: 1720988739.883585
tags:
- autogenerated
- source__oai
- conversation_id__061738c3-69c1-49e6-9274-bc50cd27a92d
- msg_aaa268ce-ac8a-4582-85fc-4fb11be8425a
- msg_a17f64ee-75b0-4a42-8133-fac98de15bd2
- colorclass/decision-making-processes
title: computational models of working attention, motivation, and decision making
---

**USER**

computational models of working attention, motivation, and decision making


**ASSISTANT**

Computational models of working attention, motivation, and decision-making are crucial for understanding complex cognitive processes. These models often integrate insights from cognitive psychology, neuroscience, and artificial intelligence to simulate how humans allocate attention, remain motivated, and make decisions. Here are some prominent models in each area:

### Working Attention

#### 1. **Biased Competition Model**

**Overview:**
The Biased Competition Model posits that attention is the result of competition among multiple stimuli, where the competition is biased by both bottom-up sensory inputs and top-down cognitive factors such as goals and expectations.

**Key Features:**
- **Competition:** Multiple stimuli compete for limited processing resources.
- **Biasing Mechanisms:** Top-down signals (e.g., goals, expectations) bias the competition, making certain stimuli more likely to win.
- **Neural Basis:** The model is supported by evidence from neurophysiological studies showing competition and biasing in visual cortex neurons.

**Mathematical Formalism:**
Let $R_i$ be the response of neuron $i$ to stimulus $S_i$, influenced by bottom-up sensory input $I_i$ and top-down bias $B_i$:
$$
R_i = \frac{I_i + B_i}{\sum_{j} (I_j + B_j)}
$$

**Applications:**
This model is used to explain phenomena such as selective attention, attentional blindness, and the effects of expectations on perception.

#### 2. **Feature Integration Theory (FIT)**

**Overview:**
Feature Integration Theory suggests that attention works by binding features (such as color, shape, and orientation) of objects together to form a coherent perception.

**Key Features:**
- **Pre-Attentive Stage:** Features are processed in parallel and independently.
- **Focused Attention Stage:** Attention is required to bind features together into a unified object.

**Mathematical Formalism:**
The model can be formalized using a two-stage process where features are first detected in parallel and then combined through attention. This process can be described using probability theory and Bayesian inference.

**Applications:**
FIT explains visual search tasks, feature binding, and the impact of attention on perception.

### Motivation

#### 1. **Temporal Difference (TD) Learning Model**

**Overview:**
The Temporal Difference Learning Model, often used in reinforcement learning, explains how agents learn to predict and maximize future rewards based on their actions. It has been applied to model the dopaminergic reward system in the brain.

**Key Features:**
- **Prediction Error:** Learning is driven by the difference between expected and received rewards.
- **Value Function:** The agent learns a value function that estimates the expected reward for each state.

**Mathematical Formalism:**
The value function $V(s)$ for state $s$ is updated as:
$$
V(s) \leftarrow V(s) + \alpha [r + \gamma V(s') - V(s)]
$$
where:
- $\alpha$ is the learning rate.
- $r$ is the received reward.
- $\gamma$ is the discount factor.
- $s'$ is the next state.

**Applications:**
TD learning is used to model decision-making under uncertainty, habit formation, and the role of dopamine in reinforcement learning.

#### 2. **Maslow's Hierarchy of Needs Model**

**Overview:**
Maslow's model is a motivational theory comprising a five-tier model of human needs, often depicted as hierarchical levels within a pyramid.

**Key Features:**
- **Physiological Needs:** Basic survival needs such as food and water.
- **Safety Needs:** Protection and security.
- **Social Needs:** Belonging and love.
- **Esteem Needs:** Respect and recognition.
- **Self-Actualization:** Realizing personal potential.

**Mathematical Formalism:**
While not originally mathematical, this model can be quantified using utility functions, where the utility $U_i$ for need $i$ is a function of the satisfaction level:
$$
U_i = f(s_i)
$$
The overall motivation can be modeled as a weighted sum of individual utilities.

**Applications:**
This model is used in psychology, business, and education to understand and enhance motivation.

### Decision Making

#### 1. **Drift Diffusion Model (DDM)**

**Overview:**
The Drift Diffusion Model describes the process of decision-making as the accumulation of evidence over time until a threshold is reached.

**Key Features:**
- **Evidence Accumulation:** Continuous collection of information favoring one decision over another.
- **Decision Threshold:** The point at which enough evidence has been accumulated to make a decision.
- **Noise:** Random fluctuations in the accumulation process.

**Mathematical Formalism:**
The process is modeled by a stochastic differential equation:
$$
dX(t) = v \, dt + \sigma \, dW(t)
$$
where:
- $X(t)$ is the accumulated evidence.
- $v$ is the drift rate.
- $\sigma$ is the diffusion coefficient.
- $W(t)$ is a Wiener process.

**Applications:**
The DDM is applied to model reaction times, accuracy in perceptual decision-making, and neural correlates of decision processes.

#### 2. **Prospect Theory**

**Overview:**
Prospect Theory describes how people make decisions under risk and uncertainty, emphasizing psychological factors such as loss aversion and probability weighting.

**Key Features:**
- **Value Function:** Defined on deviations from a reference point, concave for gains and convex for losses, and steeper for losses.
- **Probability Weighting:** People overweigh small probabilities and underweigh large probabilities.

**Mathematical Formalism:**
The value function $v(x)$ and probability weighting function $w(p)$ are given by:
$$
v(x) = \begin{cases} 
(x - r)^\alpha & \text{if } x \geq r \\
-\lambda (r - x)^\beta & \text{if } x < r 
\end{cases}
$$
$$
w(p) = \frac{p^\gamma}{(p^\gamma + (1-p)^\gamma)^{1/\gamma}}
$$
where:
- $r$ is the reference point.
- $\alpha, \beta, \gamma$ are parameters.
- $\lambda$ is the loss aversion coefficient.

**Applications:**
Prospect Theory is used in economics, finance, and behavioral decision research to explain choices involving risk and uncertainty.

### Conclusion

These computational models provide a comprehensive framework for understanding the cognitive processes involved in working attention, motivation, and decision-making. Each model has its strengths and specific applications, offering valuable insights into human behavior and cognition. By integrating these models, researchers can develop more robust theories and simulations of complex cognitive tasks.


---

preceding: [[leaky competing accumulator model]]  


following: [[connectionist learning with adaptive rule induction on-line]]

See also: [[reinforcement learning]]


See also: [[probability theory]]


See also: [[cognitive psychology]]


See also: [[decision-making under uncertainty]]


See also: [[utility functions]]


See also: [[selective attention]]