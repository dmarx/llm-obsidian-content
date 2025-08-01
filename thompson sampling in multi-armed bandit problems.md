---
date: 1717295594.166197
tags:
- autogenerated
- source__oai
- conversation_id__ca65c423-5293-48ca-a72e-29630dbc5375
- msg_aaa245ff-8ecd-4e09-8f64-35bcdfec38f9
- msg_c070d129-5e3e-4587-bed5-535bb2b106f8
- colorclass/decision-making-processes
title: thompson sampling in multi-armed bandit problems
---

**USER**

Thompson Sampling


**ASSISTANT**

## Thompson Sampling in Multi-Armed Bandit Problems

### Overview

Thompson Sampling is a Bayesian approach to the multi-armed bandit problem. It balances exploration and exploitation by selecting actions based on the probability that they are the best action. This method maintains a probability distribution (posterior distribution) over the expected rewards for each action and updates this distribution based on observed rewards.

### Key Concepts

1. **Posterior Distribution**: A probability distribution that represents the uncertainty about the expected reward of an arm after observing data.
2. **Bayesian Updating**: The process of updating the posterior distribution based on new evidence (observed rewards).
3. **Sampling**: Drawing samples from the posterior distribution to make decisions.

### Problem Definition

In the multi-armed bandit problem, you have:
- **K arms**: \(\{1, 2, \ldots, K\}\).
- **Reward distribution**: Each arm \(i\) provides a reward from a probability distribution \(R_i\) with an unknown mean \(\mu_i\).
- **Objective**: Maximize the cumulative reward over a sequence of trials.

### Thompson Sampling Algorithm

Thompson Sampling maintains and updates a posterior distribution for each arm's expected reward. At each step, it samples from these distributions to decide which arm to pull.

#### Algorithm Steps

1. **Initialization**:
   - Initialize prior distributions for the reward of each arm. For simplicity, assume rewards are Bernoulli-distributed (success/failure), so we can use Beta distributions as priors.

2. **Loop for each trial**:
   - For each arm \(i\), sample \(\theta_i\) from the posterior distribution \(P(\theta_i | \text{data})\).
   - Select the arm \(i\) with the highest sample \(\theta_i\).
   - Observe the reward \(r\) from the selected arm.
   - Update the posterior distribution for the selected arm based on the observed reward.

### Implementation

Below is an implementation of Thompson Sampling for a Bernoulli multi-armed bandit problem.

#### Python Implementation

```python
import numpy as np

class ThompsonSamplingBandit:
    def __init__(self, k):
        self.k = k
        self.successes = np.zeros(k)
        self.failures = np.zeros(k)
    
    def select_arm(self):
        samples = np.random.beta(self.successes + 1, self.failures + 1)
        return np.argmax(samples)
    
    def update(self, arm, reward):
        if reward == 1:
            self.successes[arm] += 1
        else:
            self.failures[arm] += 1

# Example usage
k = 10
bandit = ThompsonSamplingBandit(k)

for t in range(1000):
    arm = bandit.select_arm()
    reward = np.random.binomial(1, 0.5 + 0.1 * (arm == 5))  # Reward with some noise, optimal arm is 5
    bandit.update(arm, reward)

print("Successes:", bandit.successes)
print("Failures:", bandit.failures)
```

### Explanation

1. **Initialization**: 
   - `successes` and `failures` arrays are initialized to zero. They keep track of the number of successes and failures for each arm.

2. **Select Arm**: 
   - For each arm, a sample is drawn from the Beta distribution \( \text{Beta}(\text{successes}[i] + 1, \text{failures}[i] + 1) \). 
   - The arm with the highest sample is selected.

3. **Update**: 
   - The selected arm's posterior distribution is updated based on the observed reward.

### Properties of Thompson Sampling

1. **Optimism in the Face of Uncertainty**: Thompson Sampling naturally balances exploration and exploitation by being optimistic about less tried arms, encouraging exploration.
2. **Bayesian Nature**: Incorporates prior knowledge and updates beliefs based on observed data.
3. **Adaptability**: Can be adapted to various reward distributions beyond the Bernoulli case, such as Gaussian rewards.

### Applications of Thompson Sampling

1. **Online Advertising**: Selecting ads to display to maximize click-through rates.
2. **Recommendation Systems**: Recommending items to users to maximize engagement.
3. **Clinical Trials**: Allocating treatments to patients to maximize health outcomes.
4. **A/B Testing**: Deciding which version of a webpage to show to users to maximize conversions.
5. **Financial Trading**: Selecting financial instruments to trade to maximize returns.

### Conclusion

Thompson Sampling is a powerful Bayesian approach to the multi-armed bandit problem. By maintaining and updating a posterior distribution for each arm's expected reward, it effectively balances exploration and exploitation. Understanding and implementing Thompson Sampling provides a robust method for solving a wide range of decision-making problems under uncertainty.


---

preceding: [[multi-armed bandit problem]]  


following: [[upper confidence bound (ucb) strategy in multi-armed bandit problems]]

See also: [[multi-armed bandit problem]]