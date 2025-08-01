---
date: 1721835335.436528
tags:
- autogenerated
- source__oai
- conversation_id__e0c04838-939b-40d0-922d-224e4bc79bf4
- msg_aaa2b9b9-3ae4-424f-a30e-a0d87404e4e2
- msg_280514ba-1ecb-48fa-926d-6187ee1d70d1
- colorclass/game-theory
title: gibbard-satterthwaite theorem
---

**USER**

Gibbard-Satterthwaite Theorem


**ASSISTANT**

### Gibbard-Satterthwaite Theorem

The Gibbard-Satterthwaite theorem is a fundamental result in social choice theory that highlights the inherent difficulties in designing non-dictatorial [[voting systems]] that are immune to strategic manipulation. It generalizes Arrow's Impossibility Theorem by extending its implications to a broader class of voting mechanisms.

### Formal Statement

The Gibbard-Satterthwaite theorem states that for any voting mechanism with at least three alternatives, if the mechanism is deterministic and non-dictatorial, then it is susceptible to strategic manipulation by the voters.

#### More formally:

Let \( X \) be a set of at least three alternatives, and let \( N \) be a set of voters. A voting rule \( f \) maps the set of preference profiles (one for each voter) to a single alternative in \( X \). If \( f \) is:

1. **Onto**: Every alternative in \( X \) can be the outcome for some preference profile.
2. **Non-dictatorial**: There is no single voter who always determines the outcome regardless of others' preferences.
3. **Deterministic**: The outcome is uniquely determined by the preference profile.

Then, there exists at least one voter who can benefit from misrepresenting their preferences, meaning \( f \) is manipulable.

### Proof Sketch

While the full proof of the Gibbard-Satterthwaite theorem is complex, a sketch of the proof involves the following steps:

1. **Reduction to Single Peaked Preferences**: Show that any voting rule satisfying the theorem's conditions can be reduced to a case involving single-peaked preferences.
2. **Characterization of Dictatorship**: Use properties of single-peaked preferences to demonstrate that any such voting rule must effectively be a dictatorship or be susceptible to manipulation.
3. **Contradiction**: Establish that non-dictatorial, onto, and deterministic voting rules must allow for strategic manipulation by at least one voter.

### Implications

The Gibbard-Satterthwaite theorem has profound implications for the design of [[voting systems]] and collective decision-making processes:

1. **Inevitability of Manipulation**: It shows that strategic manipulation is inevitable in non-dictatorial [[voting systems]] with three or more choices.
2. **Focus on Strategy-Proof Mechanisms**: While perfect strategy-proofness is unattainable, the theorem motivates the search for mechanisms that minimize opportunities for manipulation.
3. **Use of Randomization**: One way to avoid the theorem's implications is to introduce randomization, leading to strategy-proof randomized mechanisms like the Gibbard Random Dictatorship Theorem.

### Related Concepts

#### 1. **Gibbard Random Dictatorship Theorem**

This theorem extends the Gibbard-Satterthwaite theorem to randomized voting rules. It states that the only strategy-proof and onto random mechanisms are random dictatorships.

#### 2. **Arrow's Impossibility Theorem**

Arrow's Impossibility Theorem deals with the impossibility of designing a social welfare function that satisfies unrestricted domain, non-dictatorship, Pareto efficiency, and independence of irrelevant alternatives (IIA). It is closely related to the Gibbard-Satterthwaite theorem in demonstrating the limitations of social choice mechanisms.

#### 3. **Manipulability and Strategy-Proofness**

A voting system is manipulable if voters can achieve a more preferred outcome by misrepresenting their preferences. Strategy-proof mechanisms ensure that truthful reporting is the best strategy for all participants.

### Example

Consider a voting scenario with three alternatives \( A \), \( B \), and \( C \), and three voters with the following preferences:

- Voter 1: \( A > B > C \)
- Voter 2: \( B > C > A \)
- Voter 3: \( C > A > B \)

Using a plurality voting rule (where each voter votes for their top choice):

- Voter 1 votes for \( A \)
- Voter 2 votes for \( B \)
- Voter 3 votes for \( C \)

Each alternative receives one vote, resulting in a tie. Suppose the tie-breaking rule favors \( A \). Voter 3 might realize that by voting strategically for \( B \) instead of \( C \), they can change the outcome to their second preference, \( B \), instead of their least preferred, \( A \).

### Applications and Mitigations

While the Gibbard-Satterthwaite theorem shows the inherent manipulability of [[voting systems]], several approaches attempt to mitigate its effects:

1. **Randomized Mechanisms**: Introducing randomness to break ties or select outcomes can reduce the incentives for [[strategic voting]].
2. **Restricted Domains**: Limiting the set of preferences (e.g., to single-peaked preferences) can make manipulation more difficult or irrelevant.
3. **Design of Practical Voting Systems**: Systems like Single Transferable Vote (STV) and Borda count aim to balance fairness and strategic resistance, even if they cannot completely eliminate manipulation.

### Conclusion

The Gibbard-Satterthwaite theorem is a cornerstone of social choice theory, highlighting the challenges in designing fair and manipulation-resistant [[voting systems]]. While it proves that strategic manipulation is unavoidable in certain contexts, it also drives innovation in the search for more robust and equitable decision-making mechanisms.

For further reading, explore related topics such as [[Arrow's Impossibility Theorem]], [[Strategy-Proofness]], [[Randomized Mechanisms]], and [[Voting Systems]].


---

preceding: [[social choice theory]]  


following: [[myerson-satterthwaite theorem]]

See also: [[decision-making processes]]