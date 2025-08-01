---
date: 1725228167.529736
tags:
- autogenerated
- source__oai
- conversation_id__65bf2a1a-22a0-495b-982c-1897e45253b5
- msg_aaa2d50c-0b82-4558-bb28-5e0fd603c7a0
- msg_6ff06383-b1b6-43b5-b825-bd02e0b18c3b
- colorclass/information-theory
title: no-cloning theorem
---

**USER**

the no-cloning theorem


**ASSISTANT**

The **no-cloning theorem** is a fundamental result in quantum mechanics that states it is impossible to create an exact copy of an arbitrary unknown quantum state. This theorem has profound implications for quantum information theory and quantum computing, as it distinguishes quantum information from classical information, where perfect copying is possible.

### Formal Statement of the No-Cloning Theorem

Given an arbitrary quantum state $\ket{\psi}$, there is no quantum operation (unitary or otherwise) that can produce two copies of this state, $\ket{\psi} \otimes \ket{\psi}$, from a single instance of the state $\ket{\psi}$. In other words, there is no universal unitary transformation $U$ such that for any arbitrary quantum state $\ket{\psi}$ and an initial blank state $\ket{0}$, the following holds:

$$
U (\ket{\psi} \otimes \ket{0}) = \ket{\psi} \otimes \ket{\psi}.
$$

This result applies to all quantum states $\ket{\psi}$ in a Hilbert space, making it a general and powerful statement about the nature of quantum information.

### Proof of the No-Cloning Theorem

The proof of the no-cloning theorem relies on the linearity of quantum mechanics, specifically the fact that all physical transformations of quantum states must be represented by unitary operators (or more generally, by completely positive trace-preserving maps).

#### Proof by Contradiction

Let's assume that there exists a unitary operator $U$ that can clone an arbitrary quantum state. Then for any two arbitrary quantum states $\ket{\psi}$ and $\ket{\phi}$, we would have:

1. $U (\ket{\psi} \otimes \ket{0}) = \ket{\psi} \otimes \ket{\psi}$,
2. $U (\ket{\phi} \otimes \ket{0}) = \ket{\phi} \otimes \ket{\phi}$.

Now, consider the inner product between these two results:

$$
\langle \psi \otimes 0 | U^\dagger U | \phi \otimes 0 \rangle = \langle \psi \otimes \psi | \phi \otimes \phi \rangle.
$$

Since $U$ is unitary, $U^\dagger U = I$, so the inner product simplifies to:

$$
\langle \psi | \phi \rangle \langle 0 | 0 \rangle = \langle \psi | \phi \rangle^2.
$$

Because $\langle 0 | 0 \rangle = 1$, this equation further reduces to:

$$
\langle \psi | \phi \rangle = (\langle \psi | \phi \rangle)^2.
$$

Let $\alpha = \langle \psi | \phi \rangle$. The equation becomes:

$$
\alpha = \alpha^2.
$$

The solutions to this equation are $\alpha = 0$ or $\alpha = 1$. 

- **$\alpha = 1$** corresponds to $\ket{\psi} = \ket{\phi}$, meaning the states are identical.
- **$\alpha = 0$** corresponds to $\ket{\psi}$ and $\ket{\phi}$ being orthogonal (perfectly distinguishable).

For any general pair of non-orthogonal and distinct quantum states $\ket{\psi}$ and $\ket{\phi}$, the inner product $\alpha = \langle \psi | \phi \rangle$ would not be exactly 0 or 1 but some value in between, which contradicts the requirement $\alpha = \alpha^2$. This contradiction shows that no such universal cloning unitary $U$ exists.

### Implications of the No-Cloning Theorem

The no-cloning theorem has several significant implications for quantum information theory, quantum computing, and cryptography:

1. **Quantum Cryptography**: The no-cloning theorem is fundamental to the security of quantum cryptographic protocols, such as [[Quantum Key Distribution|Quantum Key Distribution (QKD)]]. In QKD protocols like BB84, the inability to clone arbitrary quantum states prevents an eavesdropper from copying and measuring quantum states without introducing detectable disturbances.

2. **Quantum Communication**: The theorem limits how information can be transmitted and copied in quantum networks. It ensures that quantum entanglement and superposition states cannot be cloned, which is crucial for the fidelity of quantum teleportation and other quantum communication protocols.

3. **Quantum Error Correction**: In classical computing, error correction often relies on copying data multiple times to ensure redundancy. However, due to the no-cloning theorem, quantum error correction must use different strategies that do not rely on copying quantum states directly but instead use entangled states and syndrome measurements to detect and correct errors without cloning.

4. **Distinguishability of Quantum States**: The theorem underlines a fundamental difference between classical and quantum information: quantum states that are not orthogonal cannot be perfectly distinguished. Thus, any attempt to clone an unknown quantum state would fail, as it would require distinguishing between non-orthogonal states.

5. **Quantum Mechanics vs. Classical Mechanics**: The no-cloning theorem highlights a key distinction between quantum mechanics and classical mechanics. In the classical world, information can be duplicated freely without restriction. However, the quantum world’s restriction on cloning is a direct consequence of the superposition principle and the linearity of quantum mechanics.

### Generalizations and Related Concepts

1. **No-Broadcasting Theorem**: Extends the no-cloning theorem to mixed quantum states. It states that it is impossible to broadcast an arbitrary mixed quantum state, meaning a general mixed state cannot be copied to multiple locations.

2. **No-Deleting Theorem**: Another theorem related to quantum information, stating that it is impossible to delete an unknown quantum state, further illustrating the uniqueness of quantum information.

3. **No-Signaling Theorem**: This theorem is related to the principle of causality in quantum mechanics. It states that quantum entanglement cannot be used to transmit information faster than the speed of light, preserving relativistic causality.

4. **Unitary Evolution and Information Preservation**: Quantum mechanics preserves information through unitary evolution, which means the total quantum information in a closed system remains constant over time. The no-cloning theorem is a direct consequence of this conservation of information.

### Conclusion

The **no-cloning theorem** is a cornerstone of quantum mechanics and quantum information theory, setting a clear boundary between classical and quantum realms. It shows that quantum information cannot be copied perfectly, which has profound consequences for how information is processed, transmitted, and protected in quantum systems. The theorem provides a foundation for various quantum technologies, such as quantum cryptography, quantum computing, and quantum communication, and continues to be a subject of deep theoretical exploration and practical application. For further exploration, you might look into related topics like [[Quantum Key Distribution]], [[Quantum Error Correction]], and [[Entanglement]].


---

preceding: [[constructor theory]]  


following: [[no-deleting theorem]]

See also: [[information conservation laws]]


See also: [[information theory]]