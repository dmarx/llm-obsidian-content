---
date: '2025-03-30T16:32:17.217234Z'
tags:
- autogenerated
- source__claude
- conversation_id__5bc9b365-0860-4497-97af-f4450c7ada27
- msg_c85385cb-4e55-4c92-81f7-3ef485e7de50
- msg_b289affc-5cd1-49f0-b5b4-c8b6b77ba546
- colorclass/philosophy-of-language
title: doctrine of double effect
---

**USER**

Doctrine of Double Effect


**ASSISTANT**

# Doctrine of Double Effect

The [[Doctrine of Double Effect]] (DDE) is a principle in [[moral philosophy]] that distinguishes between intended consequences and merely foreseen consequences of an action. This doctrine provides an ethical framework for evaluating actions that have both good and bad effects, positing that under certain conditions, it may be permissible to cause harm as a side effect of bringing about a good result, even when it would be impermissible to cause that same harm as a means to the good result.

## Formal Characterization

The DDE can be formalized as follows:

An action $\alpha$ with both good effect $G$ and harmful effect $H$ is permissible if and only if:

1. $\text{Intrinsically}(\alpha) \neq \text{Wrong}$ (The act is not inherently impermissible)
2. $\text{Intends}(\text{agent}, G) \land \neg\text{Intends}(\text{agent}, H)$ (Only the good effect is intended)
3. $H \neq \text{MeansTo}(G)$ (The harm is not a means to the good)
4. $\text{Proportional}(G, H)$ (The good outweighs the harm)

## Historical Development

The doctrine has its origins in [[Thomas Aquinas]]'s discussion of self-defense in the [[Summa Theologica]]:

$$\begin{align}
\text{Permissible}(\alpha) \iff \exists e_1, e_2 (\text{Effect}(e_1, \alpha) \land \text{Effect}(e_2, \alpha) \land \text{Good}(e_1) \land \text{Bad}(e_2) \land \text{Intended}(e_1) \land \neg\text{Intended}(e_2))
\end{align}$$

Aquinas argued that killing an attacker could be justified if the intention was self-preservation rather than the death of the attacker.

## Philosophical Framework

### The Intention/Foresight Distinction

Central to the DDE is the distinction between what is intended and what is merely foreseen:

$$\text{Intended}(e) \neq \text{Foreseen}(e)$$

This distinction can be characterized in terms of practical reasoning:

$$\text{Intended}(e) \iff e \text{ appears in the agent's practical syllogism}$$

$$\text{Foreseen}(e) \iff \text{Believes}(\text{agent}, \text{Causes}(\alpha, e)) \land \neg\text{Intended}(e)$$

### The Means/Side-Effect Distinction

The DDE also relies on a distinction between means and side effects:

$$\text{MeansTo}(e_1, e_2) \iff \text{Causally necessary for }(e_1, e_2)$$

$$\text{SideEffect}(e_1, e_2) \iff \text{CausallyConnected}(e_1, e_2) \land \neg\text{MeansTo}(e_1, e_2)$$

## Classic Applications

### The Trolley Problem

In the classic [[trolley problem]], the DDE is used to distinguish between:

- **Switch Case**: Diverting a trolley from five people to one (permissible according to DDE)
  $$\text{Intends}(\text{DivertTrolley}) \land \text{Foresees}(\text{DeathOfOne}) \land \neg\text{MeansTo}(\text{DeathOfOne}, \text{SavingFive})$$

- **Footbridge Case**: Pushing a person onto the tracks to stop the trolley (impermissible according to DDE)
  $$\text{Intends}(\text{PushPerson}) \land \text{Intends}(\text{DeathOfOne}) \land \text{MeansTo}(\text{DeathOfOne}, \text{SavingFive})$$

### Medical Ethics

In medical contexts, the DDE distinguishes between:

- **Palliative Care**: Administering pain relief that may hasten death (permissible)
  $$\text{Intends}(\text{PainRelief}) \land \text{Foresees}(\text{HastenedDeath}) \land \neg\text{MeansTo}(\text{HastenedDeath}, \text{PainRelief})$$

- **Euthanasia**: Administering drugs to cause death (impermissible under DDE)
  $$\text{Intends}(\text{Death}) \land \text{MeansTo}(\text{LethalDose}, \text{Death})$$

### Military Ethics

In [[just war theory]], the DDE underlies the principle of non-combatant immunity:

- **Strategic Bombing**: Bombing military targets with foreseen civilian casualties (potentially permissible)
  $$\text{Intends}(\text{DestroyMilitaryTarget}) \land \text{Foresees}(\text{CivilianDeaths}) \land \neg\text{MeansTo}(\text{CivilianDeaths}, \text{MilitaryAdvantage})$$

- **Terror Bombing**: Bombing civilians to demoralize the enemy (impermissible)
  $$\text{Intends}(\text{CivilianDeaths}) \land \text{MeansTo}(\text{CivilianDeaths}, \text{Demoralization})$$

## Theoretical Challenges

### The Closeness Problem

How do we determine when one effect is a means to another?

$$\text{Closeness}(e_1, e_2) = f(\text{CausalProximity}, \text{Necessity}, \text{Sufficiency})$$

### The Individuation Problem

The [[problem of action individuation]] affects how we apply the DDE:

$$\text{If } \alpha_1 = \alpha_2 \text{ and } \text{Permissible}(\alpha_1) \text{ by DDE, then } \text{Permissible}(\alpha_2) \text{ by DDE?}$$

### The Intending/Foreseeing Boundary

The boundary between intending and foreseeing is not always clear:

$$\exists e \text{ such that } (\text{Intended}(e) \lor \text{Foreseen}(e)) \land \neg\text{Clear}(\text{IntentionStatus}(e))$$

## Philosophical Critiques

### Consequentialist Critique

[[Consequentialism]] rejects the moral relevance of the intention/foresight distinction:

$$\text{MoralValue}(\alpha) = f(\text{Consequences}(\alpha)) \text{ only}$$

### Empirical Critique

Some critics argue that the DDE conflates moral intuitions with principled distinctions:

$$\text{DDEIntuitions} = g(\text{PsychologicalDistance}, \text{EmotionalSalience}, \text{CognitiveFraming})$$

### Deontological Defense

[[Deontological ethics]] often defends the DDE as reflecting the principle that persons should not be treated merely as means:

$$\text{Wrong}(\alpha) \iff \exists p(\text{Person}(p) \land \text{TreatedMerelyAsMeans}(p, \alpha))$$

## Contemporary Applications

### Algorithmic Decision-Making

The DDE has implications for programming autonomous systems:

$$\text{EthicalAlgorithm}(\alpha) \stackrel{?}{\implies} \text{ImplementsDDE}(\alpha)$$

### Cognitive Neuroscience

Research examines the neural basis of DDE judgments:

$$\text{DDEJudgment} = h(\text{vmPFCActivation}, \text{dlPFCActivation}, \text{AmygdalaResponse})$$

## Research Frontiers

Current research explores:
- The role of [[agent-relativity]] in DDE judgments
- Cross-cultural validity of DDE intuitions
- Applications to emerging technologies like autonomous weapons
- Integration with [[virtue ethics]] approaches
- Connections to [[legal doctrine]] and criminal intent

## Formal Extensions

Recent work has attempted to formalize the DDE using:
- [[Causal Bayes nets]] to clarify causal structure
- [[Deontic logic]] to represent permissibility conditions
- [[Decision theory]] to model intention and foresight
- [[Action theory]] to address problems of individuation

## Philosophical Significance

The DDE connects to fundamental questions in ethics including:
- The role of [[intention]] in moral evaluation
- The [[demandingness]] of moral theories
- The [[agent-centered restrictions]] of deontological ethics
- The nature of [[moral luck]] and responsibility


---

preceding: [[problem of action individuation]]  


following: [[metaphysics of events]]

See also: [[side effects]]