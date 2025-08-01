---
date: 1719364828.586677
tags:
- autogenerated
- source__oai
- conversation_id__6f1d24d2-55b6-4293-9053-5e032beac8dc
- msg_aaa2bbdc-86fb-4b1e-963c-e8c61327e7c7
- msg_1372aefc-3822-4c20-8243-dc7b5312de6c
- colorclass/game-theory
title: cooperative game theory
---

**USER**

cooperative game theory


**ASSISTANT**

### Cooperative Game Theory

Cooperative game theory is a branch of game theory that focuses on the analysis of cooperative behavior among a group of players. Unlike non-cooperative game theory, which deals with how rational players make decisions independently, cooperative game theory examines how players can form coalitions and how the collective payoff can be distributed among the members of these coalitions.

#### Key Concepts

1. **Players and Coalitions**:
   - **Players**: The individuals or entities participating in the game.
   - **Coalitions**: Subsets of players who agree to cooperate and share their resources to achieve a common goal. The grand coalition includes all players.

2. **Characteristic Function**:
   - A function $v: 2^N \rightarrow \mathbb{R}$, where $N$ is the set of all players and $2^N$ is the power set of $N$. The characteristic function $v(S)$ gives the value (or worth) of coalition $S \subseteq N$.
   - For any coalition $S$, $v(S)$ represents the total payoff that the members of $S$ can achieve by working together.

3. **Imputation**:
   - An imputation is a vector $x = (x_1, x_2, \ldots, x_n)$ where $x_i$ represents the payoff to player $i$.
   - An imputation must satisfy two conditions:
     1. **Efficiency**: The total payoff is distributed among the players, i.e., $\sum_{i \in N} x_i = v(N)$.
     2. **Individual Rationality**: No player receives less than they could achieve on their own, i.e., $x_i \geq v(\{i\})$ for all $i \in N$.

4. **Core**:
   - The core is the set of imputations where no coalition has an incentive to deviate. Formally, the core $C(v)$ is defined as:
     $$ C(v) = \{ x \in \mathbb{R}^n \mid \sum_{i \in N} x_i = v(N) \text{ and } \sum_{i \in S} x_i \geq v(S) \text{ for all } S \subseteq N \}. $$

5. **Shapley Value**:
   - The Shapley value is a solution concept that provides a unique distribution of the total payoff that considers each player's marginal contribution to every possible coalition.
   - The Shapley value $\phi_i(v)$ for player $i$ is given by:
     $$ \phi_i(v) = \sum_{S \subseteq N \setminus \{i\}} \frac{|S|!(|N| - |S| - 1)!}{|N|!} \left( v(S \cup \{i\}) - v(S) \right), $$
     where $|S|$ is the number of players in coalition $S$.

6. **Nucleolus**:
   - The nucleolus is a solution concept that seeks to minimize the maximum dissatisfaction among the coalitions. It is found by solving a series of linear programming problems to ensure that the excess of the worst-off coalition is minimized.
   - The excess of coalition $S$ for an imputation $x$ is defined as $e(S, x) = v(S) - \sum_{i \in S} x_i$.

#### Example: Simple Cooperative Game

Consider a cooperative game with three players $N = \{1, 2, 3\}$ and a characteristic function defined as follows:
$$
\begin{align*}
v(\{1\}) & = 0, \\
v(\{2\}) & = 0, \\
v(\{3\}) & = 0, \\
v(\{1, 2\}) & = 100, \\
v(\{1, 3\}) & = 100, \\
v(\{2, 3\}) & = 100, \\
v(\{1, 2, 3\}) & = 120.
\end{align*}
$$

- **Core**: We need to find $(x_1, x_2, x_3)$ such that:
  $$ x_1 + x_2 + x_3 = 120, $$
  $$ x_1 + x_2 \geq 100, \quad x_1 + x_3 \geq 100, \quad x_2 + x_3 \geq 100. $$

- **Shapley Value**:
  \begin{align*}
  \phi_1(v) & = \frac{1}{3}(v(\{1\}) - v(\emptyset)) + \frac{1}{3}(v(\{1, 2\}) - v(\{2\})) + \frac{1}{3}(v(\{1, 3\}) - v(\{3\})) \\
  & = \frac{1}{3}(0 - 0) + \frac{1}{3}(100 - 0) + \frac{1}{3}(100 - 0) = \frac{200}{3} \approx 66.67, \\
  \phi_2(v) & = \frac{1}{3}(0 - 0) + \frac{1}{3}(100 - 0) + \frac{1}{3}(100 - 0) = \frac{200}{3} \approx 66.67, \\
  \phi_3(v) & = 120 - \phi_1(v) - \phi_2(v) = 120 - 66.67 - 66.67 \approx -13.34.
  \end{align*}

  This example highlights that the Shapley value distribution needs to be carefully analyzed for its feasibility, especially when characteristic function values create scenarios where individual contributions seem to exceed the total.

### Further Reading
For a more in-depth understanding of these concepts, refer to the following topics:
- [[Characteristic Function|Characteristic Function in Cooperative Games]]
- [[Shapley Value|Shapley Value Calculation]]
- [[Core of a Cooperative Game|Core and its Properties]]
- [[Nucleolus|Nucleolus in Cooperative Games]]


---


following: [[core of a cooperative game]]

See also: [[friendly competition]]


See also: [[power set]]


See also: [[game theory]]


See also: [[dark forest hypothesis]]