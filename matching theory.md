---
date: 1717417563.807023
tags:
- autogenerated
- source__oai
- conversation_id__5db31b97-3350-434f-b9ff-ff27f3096e81
- msg_aaa28191-b2e3-4baa-870e-7376afc95eb0
- msg_3b34182c-11ba-4c90-af02-304baa92c981
- colorclass/systems-theory
title: matching theory
---

**USER**

matching theory


**ASSISTANT**

Matching theory is a branch of graph theory that deals with the problem of finding a set of edges without common vertices in a graph. This set is called a matching. The study of matchings is essential in various fields such as combinatorics, optimization, and theoretical computer science. Let's delve into some of the key concepts and results in matching theory.

## Key Concepts

### Matching

A **matching** in a graph $G = (V, E)$ is a set of edges $M \subseteq E$ such that no two edges in $M$ share a common vertex. 

### Maximum Matching

A **maximum matching** is a matching that contains the largest possible number of edges. The size of a maximum matching in $G$ is denoted by $\nu(G)$.

### Perfect Matching

A **perfect matching** is a matching that covers every vertex of the graph. In other words, every vertex in $V$ is incident to exactly one edge in the matching. A perfect matching only exists if the graph has an even number of vertices.

### Bipartite Graphs and Hall's Theorem

A **bipartite graph** is a graph whose vertices can be divided into two disjoint sets $U$ and $W$ such that every edge connects a vertex in $U$ to one in $W$. Hall's Theorem provides a criterion for the existence of a perfect matching in bipartite graphs.

**Hall's Theorem**: Let $G = (U \cup W, E)$ be a bipartite graph. There exists a matching that covers every vertex in $U$ if and only if for every subset $S \subseteq U$, the neighborhood $N(S)$ (the set of all vertices in $W$ adjacent to at least one vertex in $S$) satisfies $|N(S)| \geq |S|$.

### Tutte's Theorem

For general graphs, Tutte's Theorem provides a necessary and sufficient condition for the existence of a perfect matching.

**Tutte's Theorem**: A graph $G$ has a perfect matching if and only if for every subset $S \subseteq V$, the number of odd components (components with an odd number of vertices) of $G - S$ is at most $|S|$.

## Algorithms

### Hungarian Algorithm

The **Hungarian algorithm**, also known as the **Kuhn-Munkres algorithm**, is a combinatorial optimization algorithm that solves the assignment problem in polynomial time and is used to find maximum matchings in bipartite graphs.

### Edmonds' Blossom Algorithm

The **Blossom algorithm** (Edmonds' algorithm) extends the ability to find maximum matchings to non-bipartite graphs. It efficiently handles the detection of odd-length cycles (blossoms) and contracts them, transforming the problem into a bipartite matching problem.

## Mathematical Formalism

Consider a graph $G = (V, E)$. Define a matching $M \subseteq E$ such that for any two edges $(u, v)$ and $(x, y)$ in $M$, we have $\{u, v\} \cap \{x, y\} = \emptyset$.

### Maximum Matching

The size of a maximum matching, $\nu(G)$, is defined as:

$$
\nu(G) = \max \{|M| : M \text{ is a matching in } G\}
$$

### Perfect Matching

A perfect matching $M$ satisfies:

$$
|M| = \frac{|V|}{2} \quad \text{and} \quad \forall v \in V, \exists! e \in M \text{ such that } v \in e
$$

### Hall's Condition

For bipartite graph $G = (U \cup W, E)$, Hall's condition states:

$$
|N(S)| \geq |S| \quad \forall S \subseteq U
$$

### Tutte's Condition

For general graph $G$, Tutte's condition states:

$$
o(G - S) \leq |S| \quad \forall S \subseteq V
$$

where $o(G - S)$ denotes the number of odd components of the subgraph induced by $V \setminus S$.

## Applications

Matching theory finds applications in numerous fields, including:

- **Market Design**: Used in matching markets like the job market, college admissions, and organ transplant allocations (see the [[Gale-Shapley Algorithm|Gale-Shapley algorithm]]).
- **Network Theory**: Used in network flow problems and internet data routing.
- **Optimization**: Used in solving integer programming problems and various optimization tasks.

Understanding matching theory provides a foundation for tackling complex problems in both theoretical and applied mathematics, providing tools to solve practical issues in various domains.


---


following: [[hall's theorem]]

See also: [[combinatorial optimization]]


See also: [[graph theory]]