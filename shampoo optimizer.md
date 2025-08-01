---
date: 1726423372.813107
tags:
- autogenerated
- source__oai
- conversation_id__66e7206b-8b28-8008-8f8b-bd7793ae3dcc
- msg_0ca4ca39-1d51-4e52-9083-343ab6cd2015
- msg_8e13f8da-1752-4edd-92e6-91b4271f12ec
- colorclass/vector-space
title: shampoo optimizer
---

**USER**

The shampoo optimizer


**ASSISTANT**

The **Shampoo optimizer** is a second-order optimization method designed for large-scale machine learning problems, particularly deep learning. Introduced by Google Research, Shampoo uses the concept of **preconditioning** by approximating second-order information (curvature) in a tractable way, making it suitable for optimizing deep neural networks with large numbers of parameters. Shampoo derives its name from **Sh**ifted **A**ppr**o**ximate Matrices **M**ethod for **P**arallel **O**ptimization, but also as a playful analogy to "conditioning" and "preconditioning."

### Motivation
The primary motivation behind Shampoo is to address the limitations of first-order optimization methods, like [[SGD]] (Stochastic Gradient Descent) and [[Adam]]. These methods rely solely on gradient information to update parameters, which can lead to slow convergence, especially in ill-conditioned problems. First-order methods also struggle when different parameters of a model evolve at different rates due to varying curvatures in the objective function, which can lead to inefficient parameter updates.

Shampoo improves upon this by incorporating second-order information via **block-diagonal approximations** of the Hessian matrix, capturing curvature across parameter groups. This leads to more informed gradient updates and faster convergence.

### Key Concepts and Algorithm
Shampoo introduces a form of **preconditioning** that generalizes second-order updates to matrices of parameters, allowing it to exploit richer geometric information about the optimization landscape. The method can be summarized as follows:

1. **Block-diagonal approximation of the Hessian**: Rather than computing and storing the full Hessian matrix, which is computationally expensive for high-dimensional problems, Shampoo computes second-order statistics on a block-diagonal approximation. The parameters are partitioned into groups (or "blocks"), and separate preconditioners are constructed for each block.
   
2. **Kronecker-factored preconditioning**: Shampoo preconditions the gradient by using Kronecker-factored approximations of the Hessian matrix. For each layer in a neural network, the parameters are often in matrix form (such as the weight matrix of a fully connected or convolutional layer). Shampoo takes advantage of this structure by factoring the Hessian as a Kronecker product of smaller matrices, making the preconditioning computationally efficient.

3. **Efficient Matrix Inversion**: Since Shampoo uses Kronecker-factored approximations, the inversion of the preconditioner (which is necessary to compute the parameter update) becomes more efficient. Instead of inverting large matrices directly, Shampoo inverts smaller matrices corresponding to the Kronecker factors, significantly reducing the computational cost.

4. **Per-parameter matrix updates**: Shampoo maintains a preconditioner for each matrix of parameters in the model, such as the weight matrices in different layers of a neural network. This means that instead of updating parameters using a single global step size or preconditioner, Shampoo adapts the update for each parameter block based on its local curvature.

### Shampoo's Update Rule
Consider the weight matrix $\mathbf{W}_t$ at time step $t$, where $\mathbf{G}_t$ is the gradient of the loss function with respect to $\mathbf{W}_t$. Shampoo applies the following steps:

1. **Gradient accumulation**: Shampoo maintains accumulated gradients to estimate second-order information. For a matrix of parameters $\mathbf{W}$, we can define the gradient at step $t$ as $\mathbf{G}_t$.
   
2. **Kronecker-factored matrices**: The preconditioner is formed by maintaining two separate matrices $\mathbf{A}_t$ and $\mathbf{B}_t$ which are updated as follows:

   $$ \mathbf{A}_t = \mathbf{A}_{t-1} + \mathbf{G}_t^\top \mathbf{G}_t $$
   $$ \mathbf{B}_t = \mathbf{B}_{t-1} + \mathbf{G}_t \mathbf{G}_t^\top $$

   These matrices approximate the Kronecker factors of the Fisher information matrix (or, equivalently, the Hessian in the quadratic approximation).

3. **Preconditioned update**: The parameter update is then computed as:

   $$ \mathbf{W}_{t+1} = \mathbf{W}_t - \alpha \cdot \mathbf{P}_t^{-1} \cdot \mathbf{G}_t $$

   where $\mathbf{P}_t^{-1}$ is the preconditioner obtained by inverting the Kronecker-factored matrices $\mathbf{A}_t$ and $\mathbf{B}_t$. Since $\mathbf{P}_t^{-1}$ is factored as a Kronecker product, the inversion can be computed efficiently.

4. **Scaling and Regularization**: Shampoo introduces damping to ensure numerical stability, typically adding a small regularization term $\lambda$ to the matrices $\mathbf{A}_t$ and $\mathbf{B}_t$ before inversion, as in many second-order methods:

   $$ \mathbf{A}_t = \mathbf{A}_{t-1} + \mathbf{G}_t^\top \mathbf{G}_t + \lambda \mathbf{I} $$
   $$ \mathbf{B}_t = \mathbf{B}_{t-1} + \mathbf{G}_t \mathbf{G}_t^\top + \lambda \mathbf{I} $$

### Advantages of Shampoo
- **Second-order information**: Shampoo uses approximate second-order curvature information, leading to better-aligned gradient steps than first-order methods like [[Adam]] or [[SGD]].
- **Efficient scaling to large models**: Shampoo is specifically designed to handle large matrices of parameters efficiently by leveraging Kronecker-factorization, which dramatically reduces the computational overhead compared to fully explicit Hessian-based methods.
- **Adaptivity**: By maintaining block-specific preconditioners, Shampoo adapts updates to the local curvature of the objective function, which can result in significantly faster convergence, especially for deep networks.

### Computational Challenges
Despite its efficiency improvements over direct second-order methods, Shampoo still incurs more overhead than first-order methods. For each block of parameters, Shampoo needs to store and update two matrices of size $d \times d$, where $d$ is the dimension of the corresponding block. Additionally, computing the inverse of these matrices, even in factored form, can introduce some computational complexity. For very large models, this overhead may become significant, though Shampoo is designed to mitigate this through its Kronecker structure.

### Comparison to Other Optimizers
- **Shampoo vs [[Adam]]**: Adam is a first-order method that adapts learning rates based on the first and second moments of the gradients. While Adam is computationally cheap and works well in many practical cases, it does not take into account second-order information, which can lead to inefficient updates in some optimization landscapes. Shampoo, by contrast, incorporates second-order curvature information and thus can converge faster for certain classes of problems.
  
- **Shampoo vs [[L-BFGS]]**: L-BFGS is a quasi-Newton method that builds an approximation to the inverse Hessian matrix based on gradient information from multiple past iterations. While L-BFGS works well for many problems, it scales poorly for very large deep learning models due to the need to store and manipulate large matrices. Shampoo, on the other hand, is explicitly designed for large-scale optimization with deep neural networks.

### Applications and Practical Use
Shampoo has been successfully applied to large-scale deep learning tasks, such as training neural networks for image classification and natural language processing. Its ability to efficiently incorporate second-order information makes it particularly useful in scenarios where first-order methods struggle, such as when the optimization landscape is highly anisotropic or when different model parameters exhibit widely varying sensitivities.

In practice, Shampoo can be more difficult to tune compared to first-order methods, as it introduces additional hyperparameters (e.g., damping terms, block sizes) that need to be chosen carefully. However, for large-scale models where training time is a significant bottleneck, the potential for faster convergence can outweigh these complexities.

### Conclusion
The Shampoo optimizer is a powerful second-order method designed for modern large-scale machine learning applications. By leveraging Kronecker-factored preconditioners and block-diagonal approximations of the Hessian, Shampoo efficiently incorporates curvature information, enabling faster convergence compared to first-order methods. It represents a balance between the rich geometry captured by second-order methods and the scalability needed for deep learning, making it a promising tool in large-scale optimization.


---

preceding: [[preconditioning in the context of gradient based optimization]]