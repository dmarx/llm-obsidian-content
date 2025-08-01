---
date: 1722089627.222636
tags:
- autogenerated
- source__oai
- conversation_id__7d45b320-298e-47b7-9441-dbf4e42574d4
- msg_aaa2f645-34cd-4109-8e36-3e0c15e0e86c
- msg_ee1cf3b2-2fe9-4c68-af45-9591407a1c80
- colorclass/philosophy-of-language
title: structural causal models (scms)
---

**USER**

Structural Causal Models


**ASSISTANT**

### Structural Causal Models (SCMs)

Structural Causal Models (SCMs), developed and popularized by Judea Pearl and his collaborators, provide a rigorous framework for causal inference by combining graphical models with probabilistic and structural equations. SCMs enable the identification, estimation, and interpretation of causal relationships from observational and experimental data.

#### 1. **Basic Concepts of Structural Causal Models**

- **Causal Graphs**: Directed acyclic graphs (DAGs) represent the causal relationships among variables. Nodes represent variables, and directed edges (arrows) represent causal effects.
  - **Example**: In a simple model where smoking causes lung cancer, the graph would have an arrow from "Smoking" to "Lung Cancer."

- **Structural Equations**: Each node (variable) in the DAG is associated with a structural equation that describes how the variable is determined by its parent variables (the variables with arrows pointing to it).
  - **Example**: The equation for lung cancer might be \( \text{Lung Cancer} = f(\text{Smoking}) + U \), where \( U \) represents unobserved factors.

- **Exogenous and Endogenous Variables**:
  - **Exogenous Variables**: Variables that are determined outside the model and not influenced by other variables within the model.
  - **Endogenous Variables**: Variables that are determined by other variables within the model.

#### 2. **Key Components of SCMs**

- **Directed Acyclic Graph (DAG)**: A graph with directed edges and no cycles, used to represent causal relationships.
- **Structural Equations**: Mathematical equations specifying how each variable is generated from its direct causes (parents) and a random error term.
- **Interventions**: Actions that change the value of a variable, used to analyze causal effects by simulating changes in the DAG.

#### 3. **Causal Inference with SCMs**

SCMs provide tools to perform various causal inference tasks, including:

- **Identification of Causal Effects**: Determining whether a causal effect can be estimated from the available data and how it can be computed.
  - **Back-Door Criterion**: A set of variables \( Z \) satisfies the back-door criterion for a causal effect of \( X \) on \( Y \) if \( Z \) blocks all back-door paths from \( X \) to \( Y \) (paths that end at \( X \)).
  - **Front-Door Criterion**: A set of variables \( Z \) satisfies the [[front-door criterion]] if \( Z \) mediates the causal effect from \( X \) to \( Y \) and controls for all confounding between \( Z \) and \( Y \).

- **Do-Calculus**: A set of rules developed by Pearl for transforming expressions with interventions (denoted by \( do(X) \)) into expressions involving observed data.
  - **Example**: To estimate the causal effect of \( X \) on \( Y \), we use \( P(Y \mid do(X)) \), which represents the distribution of \( Y \) after setting \( X \) to a specific value through intervention.

#### 4. **Methods for Estimating Causal Effects**

- **Back-Door Adjustment**: If \( Z \) satisfies the back-door criterion, the causal effect of \( X \) on \( Y \) can be estimated by adjusting for \( Z \):
  $$ P(Y \mid do(X)) = \sum_{z} P(Y \mid X, Z=z)P(Z=z) $$
- **Front-Door Adjustment**: If \( Z \) satisfies the [[front-door criterion]], the causal effect of \( X \) on \( Y \) can be estimated using:
  $$ P(Y \mid do(X)) = \sum_{z} P(Z=z \mid X) \sum_{x} P(Y \mid X=x, Z=z)P(X=x) $$

#### 5. **Examples and Applications**

- **Example 1: Smoking and Lung Cancer**
  - **Problem**: Estimating the causal effect of smoking on lung cancer incidence.
  - **Model**: A DAG with nodes for Smoking, Lung Cancer, and possible confounders like Genetic Factors.
  - **Adjustment**: If Genetic Factors are identified as a back-door path, we adjust for them to estimate the causal effect of Smoking on Lung Cancer.

- **Example 2: Education and Earnings**
  - **Problem**: Assessing the causal impact of education on earnings.
  - **Model**: A DAG with nodes for Education, Earnings, and confounders like Socioeconomic Background.
  - **Adjustment**: Controlling for Socioeconomic Background using back-door adjustment to estimate the causal effect of Education on Earnings.

#### 6. **Advantages of SCMs**

- **Clarity**: SCMs provide a clear and visual representation of causal assumptions through DAGs.
- **Formal Framework**: SCMs offer a formal mathematical framework for causal inference, allowing for rigorous analysis and proof.
- **Flexibility**: SCMs can incorporate both observational and experimental data, making them versatile for various types of studies.

#### 7. **Limitations and Challenges**

- **Assumption Validity**: The accuracy of causal inferences depends on the correctness of the assumed causal graph and structural equations.
- **Data Requirements**: Adequate data on all relevant variables is needed for reliable causal inference.
- **Complexity**: Constructing and analyzing SCMs can be complex, especially for large models with many variables and intricate relationships.

#### 8. **Philosophical Considerations**

- **Causal Realism**: SCMs are grounded in the belief that causal relationships reflect real mechanisms in the world, and these can be represented and analyzed using formal tools.
- **Interventionism**: SCMs align with interventionist theories of causation, where causal relationships are understood in terms of the effects of interventions.

### Conclusion

Structural Causal Models provide a powerful and rigorous framework for understanding and estimating causal relationships. By combining graphical representations with structural equations, SCMs offer a comprehensive approach to causal inference that can handle both observational and experimental data. Despite their complexity and the need for strong assumptions, SCMs are invaluable tools in fields ranging from epidemiology and social sciences to economics and artificial intelligence. Understanding SCMs enhances our ability to make informed decisions based on causal relationships and to develop effective interventions.


---

preceding: [[bradford hill criteria]]  


following: [[back-door criterion]]

See also: [[informed decision]]


See also: [[causal effect]]


See also: [[interventionist theories of causation]]