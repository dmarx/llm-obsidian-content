---
date: 1716237406.706989
tags:
- autogenerated
- source__oai
- conversation_id__c7ff2181-2ccd-4e8d-bed4-9da199b2c1bc
- msg_aaa235e5-cb9e-4b89-857c-b47afa59aabe
- msg_96454bb8-243d-4a55-ab9b-79f5a88e9180
- colorclass/game-theory
title: cultural transmission models
---

**USER**

Cultural Transmission Models


**ASSISTANT**

## Cultural Transmission Models

Cultural transmission models are mathematical and computational frameworks used to study how cultural traits, behaviors, and information spread within and between populations. These models help researchers understand the mechanisms behind cultural change and the factors influencing the persistence and evolution of cultural traits.

### Key Concepts

1. **Cultural Traits**: Units of cultural information, such as beliefs, practices, languages, technologies, and social norms, that can be transmitted from one individual to another.

2. **Modes of Transmission**:
   - **Vertical Transmission**: Cultural traits are passed from parents to offspring.
   - **Horizontal Transmission**: Cultural traits are transmitted between individuals of the same generation.
   - **Oblique Transmission**: Cultural traits are transmitted from individuals of one generation to non-descendants of the next generation (e.g., from teachers to students).

3. **Biases in Transmission**:
   - **Content Bias**: Preference for certain traits based on their intrinsic characteristics, such as ease of understanding or memorability.
   - **Model Bias**: Preference for traits based on the characteristics of the person demonstrating the trait, such as their prestige or success.
   - **Frequency-Dependent Bias**: Preference for traits based on their prevalence in the population, which can be either conformist (favoring common traits) or anti-conformist (favoring rare traits).

### Mathematical Models

#### 1. **Neutral Model of Cultural Evolution**

The neutral model assumes that all cultural traits have an equal probability of being transmitted, without any selective bias. This model is often used as a null hypothesis in cultural evolution studies.

$$
\frac{dp_i}{dt} = \mu (1 - p_i) - \nu p_i
$$

where $p_i$ is the frequency of trait $i$, $\mu$ is the innovation rate (rate of new trait introduction), and $\nu$ is the rate of trait loss.

#### 2. **Biased Transmission Model**

Biased transmission models incorporate preferences for certain traits over others. The transmission probability is influenced by the biases mentioned earlier.

$$
\frac{dp_i}{dt} = \sum_{j} p_j T_{ji} - p_i \sum_{j} T_{ij}
$$

where $T_{ij}$ is the transition probability from trait $i$ to trait $j$, reflecting the influence of biases.

#### 3. **Dual Inheritance Model**

This model considers both genetic and cultural inheritance, accounting for the interactions between the two systems. The dynamics of cultural traits are modeled alongside genetic traits.

$$
\frac{dp}{dt} = \mu (1 - p) - \nu p + s p (1 - p)
$$

where $p$ is the frequency of a cultural trait, $\mu$ is the innovation rate, $\nu$ is the loss rate, and $s$ represents the selective advantage of the trait.

#### 4. **Cultural Group Selection Model**

This model examines how cultural traits that benefit groups can spread, even if they are costly to individuals. The model typically involves multi-level selection processes.

$$
\frac{dp_i}{dt} = p_i (1 - p_i) \left[ r_i - \bar{r} + \frac{1}{N} \left( R_i - \bar{R} \right) \right]
$$

where $p_i$ is the frequency of the cultural trait in group $i$, $r_i$ is the individual-level fitness, $\bar{r}$ is the average individual-level fitness, $R_i$ is the group-level fitness, and $\bar{R}$ is the average group-level fitness.

### Applications

- **Anthropology**: Understanding the diffusion of cultural practices and artifacts across different societies.
- **Linguistics**: Studying the spread and evolution of languages.
- **Sociology**: Analyzing the spread of social norms, behaviors, and innovations.
- **Economics**: Modeling the diffusion of technological innovations and consumer behaviors.

### Empirical Studies

Empirical studies of cultural transmission often involve:

- **Field Studies**: Observing and recording cultural practices in natural settings.
- **Experimental Studies**: Conducting controlled experiments to observe cultural transmission processes.
- **Historical Analysis**: Analyzing historical records to trace the diffusion and evolution of cultural traits.
- **Computational Simulations**: Using agent-based models to simulate cultural transmission dynamics.

### Conclusion

Cultural transmission models provide a rigorous framework for understanding the complex processes underlying cultural evolution. By incorporating various modes of transmission and biases, these models help elucidate how cultural traits spread, persist, and evolve over time.

For further exploration, you might refer to related topics such as [[Memetics]], [[Dual Inheritance Theory]], and [[Evolutionary Anthropology]].


---

preceding: [[cultural evolution]]  


following: [[biased transmission model]]

See also: [[consumer behavior]]


See also: [[relate cooperation in evolutionary psychology, the theory of cooperation typonomy, cooperation in game theory, and the theory of morality as cooperation]]


See also: [[cultural transmission]]