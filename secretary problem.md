---
date: 1721880129.271958
tags:
- autogenerated
- source__oai
- conversation_id__91d0b461-37b0-4e34-904d-d5ee935d61bb
- msg_aaa2de71-af13-4aa4-9698-d4d8e0f04303
- msg_b7b2bca3-983f-421b-9569-297390541acd
- colorclass/decision-making-processes
title: secretary problem
---

**USER**

Secretary Problem


**ASSISTANT**

### Secretary Problem

The **Secretary Problem**, also known as the "Marriage Problem" or the "Best Choice Problem," is a classic example of an optimal stopping problem. The objective is to select the best candidate (secretary, spouse, etc.) from a sequentially presented set of candidates under specific rules and constraints.

### Problem Setup

1. **Candidates**: There are \( n \) candidates for a position.
2. **Sequential Interviews**: Candidates are interviewed one at a time in random order.
3. **Immediate Decision**: After each interview, a decision must be made to either accept or reject the candidate.
4. **No Recall**: Once rejected, a candidate cannot be recalled or reconsidered.

The goal is to maximize the probability of selecting the best candidate.

### Optimal Strategy

The optimal strategy for the Secretary Problem involves two main phases:
1. **Observation Phase**: Interview and reject the first \( r \) candidates, where \( r \) is the number of candidates to be observed without making a selection.
2. **Selection Phase**: After the observation phase, select the next candidate who is better than all the previous candidates.

### Determining the Optimal \( r \)

The value of \( r \) that maximizes the probability of selecting the best candidate is approximately \( n/e \), where \( e \) is the base of the natural logarithm (approximately 2.718).

### Probability of Success

The probability of successfully selecting the best candidate using the optimal stopping rule can be calculated as follows:

1. **Observation Phase**: Reject the first \( r \) candidates.
2. **Selection Phase**: Select the next candidate who is better than all previously interviewed candidates.

The probability of selecting the best candidate is given by:

$$
P(\text{success}) \approx \frac{1}{e} \approx 0.3679
$$

This means that by following the optimal strategy, there is approximately a 37% chance of selecting the best candidate.

### Mathematical Derivation

1. **Probability Function**: Let \( X_i \) denote the rank of the \( i \)-th candidate among the first \( i \) candidates. The probability that the best candidate is selected is:

   $$
   P(\text{success}) = \sum_{k=r+1}^{n} P(\text{select the best candidate at position } k)
   $$

2. **Best Candidate**: The best candidate appears at position \( k \) with probability \( \frac{1}{n} \).

3. **Selection Condition**: The candidate at position \( k \) is selected if they are better than all the first \( k-1 \) candidates. The probability of this happening given that the candidate at position \( k \) is the best is \( \frac{r}{k-1} \).

Therefore, the total probability of selecting the best candidate is:

$$
P(\text{success}) = \sum_{k=r+1}^{n} \frac{1}{n} \cdot \frac{r}{k-1}
$$

Approximating this sum for large \( n \), we get:

$$
P(\text{success}) \approx \frac{1}{e}
$$

### Implementation Example

Let's consider an example with \( n = 100 \) candidates.

1. **Optimal \( r \)**: \( r \approx \frac{100}{e} \approx 37 \).
2. **Observation Phase**: Interview and reject the first 37 candidates.
3. **Selection Phase**: Select the next candidate who is better than all the previous 37 candidates.

### Applications

The Secretary Problem has applications beyond the hiring process, including:
1. **Real Estate**: Deciding when to accept an offer on a house.
2. **Online Dating**: Choosing a potential partner based on sequential encounters.
3. **Auction Bidding**: Determining when to place a bid in a sequential auction.

### Variants and Extensions

1. **Unknown \( n \)**: Variants where the total number of candidates \( n \) is unknown, leading to adaptive strategies.
2. **Multiple Selections**: Extensions where multiple selections can be made, requiring more complex strategies.
3. **Ranked Payoffs**: Variants where candidates have different payoffs, and the goal is to maximize the expected payoff rather than just selecting the best candidate.

### Conclusion

The Secretary Problem illustrates a fundamental optimal stopping problem with a clear and elegant solution. By using the optimal strategy of observing and then selecting, decision-makers can maximize their chances of making the best choice. This problem and its extensions have practical applications in various fields, showcasing the power of mathematical optimization in decision-making processes.


---

preceding: [[optimal stopping theory]]  


following: [[american option pricing]]

See also: [[decision-making processes]]