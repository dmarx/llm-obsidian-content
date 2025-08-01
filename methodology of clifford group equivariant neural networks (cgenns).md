---
date: 1713153585.273253
tags:
- autogenerated
- source__oai
- conversation_id__5fa9dfe5-a59e-4ed4-a2e9-ff745c9a6df9
- msg_aaa2cf41-a645-465f-8634-a9280ed298c6
- msg_bc1cf0e3-db4c-4bd2-b285-0718e52e6e68
- colorclass/vector-space
title: methodology of clifford group equivariant neural networks (cgenns)
---

**USER**

4 Methodology
We restrict our layers to use F := R. Our method is most similar to steerable methods such as
[BHP+22]. However, unlike these works, we do not require an alternative basis representation
based on spherical harmonics, nor do we need to worry about Clebsch-Gordan coefficients. Instead,
we consider simply a steerable vector basis for V , which then automatically induces a steerable
multivector basis for Cl(V, q) and its transformation kernels. By steerability, we mean that this
basis can be transformed in a predictable way under an action from the Clifford group, which acts
orthogonally on both V and Cl(V, q) (see Figure 1).
We present layers yielding Clifford group-equivariant optimizable transformations. All the main ideas
are based on Corollary 3.3 and Corollary 3.4. It is worth mentioning that the methods presented here
form a first exploration of applying our theoretical results, making future optimizations rather likely.
Linear Layers Let x1, . . . , xℓ ∈ Cl(V, q) be a tuple of multivectors expressed in a steerable basis,
where ℓ represents the number of input channels. Using the fact that a polynomial restricted to the
first order constitutes a linear map, we can construct a linear layer by setting
y
(k)
cout
:= T
lin
ϕcout
(x1, . . . , xℓ)
(k)
:= X
ℓ
cin=1
ϕcoutcink x
(k)
cin
, (13)
where ϕcoutcink ∈ R are optimizable coefficients and cin, cout denote the input and output channel,
respectively. As such, Tϕ : Cl(V, q)
ℓ → Cl(V, q) is a linear transformation in each algebra subspace
5Here we restrict (V, q) to be non-degenerate as we never consider degenerate quadratic forms in our
experiments. However, in the supplementary material we generalize this also to the degenerate case by carefully
taking the radical subspace R of (V, q) into account on both sides of the isomorphism.
6We discuss in Appendix E.6 a general definition of these groups.
6
k. Recall that this is possible due to the result that ρ(w) respects the multivector subspaces. This
computes a transformation for the output channel cout; the map can be repeated (using different sets of
parameters) for other output channels, similar to classical neural network linear layers. For y
(0)
cout ∈ R
(the scalar part of the Clifford algebra), we can additionally learn an invariant bias parameter.
Geometric Product Layers A core strength of our method comes from the fact that we can also
parameterize interaction terms. In this work, we only consider layers up to second order. Higher-order
interactions are indirectly modeled via multiple successive layers. As an example, we take the pair
x1, x2. Their interaction terms take the form 
x
(i)
1 x
(j)
2
(k)
, i, j, k = 0, . . . , n; where we again make
use of the fact that ρ(w) respects grade projections. As such, all the grade-k terms resulting from the
interaction of x1 and x2 are parameterized with
Pϕ(x1, x2)
(k)
:= Xn
i=0
Xn
j=0
ϕijk 
x
(i)
1 x
(j)
2
(k)
, (14)
where Pϕ : Cl(V, q) × Cl(V, q) → Cl(V, q). This means that we get (n + 1)3 parameters for every
geometric product between a pair of multivectors7
. Parameterizing and computing all second-order
terms amounts to ℓ
2
such operations, which can be computationally expensive given a reasonable
number of channels ℓ. Instead, we first apply a linear map to obtain y1, . . . , yℓ ∈ Cl(V, q). Through
this map, the mixing (i.e., the terms that will get multiplied) gets learned. That is, we only get ℓ
pairs (x1, y1), . . . ,(xℓ, yℓ) from which we then compute z
(k)
cout := Pϕcout
(xcin , ycin )
(k)
. Note that here
we have cin = cout, i.e., the number of channels does not change. Hence, we refer to this layer as
the element-wise geometric product layer. We can obtain a more expressive (yet more expensive)
parameterization by linearly combining such products by computing
z
(k)
cout
:= T
prod
ϕcout
(x1, . . . , xℓ, y1, . . . , yℓ)
(k)
:= X
ℓ
cin=1
Pϕcoutcin
(xcin , ycin )
(k)
, (15)
which we call the fully-connected geometric product layer. Computational feasibility and experimental
verification should determine which parameterization is preferred.
Normalization and Nonlinearities Since our layers involve quadratic and potentially higher-order
interaction terms, we need to ensure numerical stability. In order to do so, we use a normalization
operating on each multivector subspace before computing geometric products by putting
x
(m)
7→
x
(m)
σ(am)

¯q(x
(m)) − 1

+ 1
, (16)
where x
(m) ∈ Cl(m)
(V, q). Here, σ denotes the logistic sigmoid function, and am ∈ R is a learned
scalar. The denominator interpolates between 1 and the quadratic form ¯q

x
(m)

, normalizing the
magnitude of x
(m)
. This ensures that the geometric products do not cause numerical instabilities
without losing information about the magnitude of x
(m)
, where a learned scalar interpolates between
both regimes. Note that by Theorem 3.2, ¯q(x
(m)
) is invariant under the action of the Clifford group,
rendering Equation (16) an equivariant map.
Next, we use the layer-wide normalization scheme proposed by [RGdK+23], which, since it is also
based on the extended quadratic form, is also equivariant with respect to the twisted conjugation.
Regarding nonlinearities, we use a slightly adjusted version of the units proposed by [RGdK+23].
Since the scalar subspace Cl(0)(V, q) is always invariant with respect to the twisted conjugation,
we can apply x
(m)
7→ ReLU
x
(m)

when m = 0 and x
(m)
7→ σϕ

¯q

x
(m)
 x
(m) otherwise. We
can replace ReLU with any common scalar activation function. Here, σϕ represents a potentially
parameterized nonlinear function. Usually, however, we restrict it to be the sigmoid function. Since
we modify x
(m) with an invariant scalar quantity, we retain equivariance. Such gating activations are
commonly used in the equivariance literature [WGW+18, GS22].
7
In practice, we use fewer parameters due to the sparsity of the geometric product, implying that many
interactions will invariably be zero, thereby making their parameterization redundan
10
3 10
4
O(3) Signed Volumes
10
1
10
3
10
5
10
7
MSE ( )
10
3 10
4
O(5) Convex Hulls
0
10
20
30
10
2 10
3 10
4
O(5) Regression
10
4
10
2
10
0
10
2
E(n)-MLP
VN
GVP
MLP
MLP+Aug
EMLP SO(5)
EMLP O(5)
CGENN (Ours)
Figure 3: Left: Test mean-squared errors on the O(3) signed volume
task as functions of the number of training data. Note that due to
identical performance, some baselines are not clearly visible. Right:
same, but for the O(5) convex hull task.
Figure 4: Test meansquared-errors on the O(5)
regression task.
Embedding Data in the Clifford Algebra In this work, we consider data only from the vector
space V or the scalars R, although generally one might also encounter, e.g., bivector data. That is,
we have some scalar features h1, . . . , hk ∈ R and some vector features hk+1, . . . , hℓ ∈ V . Typical
examples of scalar features include properties like mass, charge, temperature, and so on. Additionally,
one-hot encoded categorical features are also included because {0, 1} ⊂ R and they also transform
trivially. Vector features include positions, velocities, and the like. Then, using the identifications
Cl(0)(V, q) ∼= R and Cl(1)(V, q) ∼= V , we can embed the data into the scalar and vector subspaces of
the Clifford algebra to obtain Clifford features x1, . . . , xℓ ∈ Cl(V, q).
Similarly, we can predict scalar- or vector-valued data as output of our model by grade-projecting onto
the scalar or vector parts, respectively. We can then directly compare these quantities with groundtruth vector- or scalar-valued data through a loss function and use standard automatic differentiation
techniques to optimize the model. Note that invariant predictions are obtained by predicting scalar
quantities.


**ASSISTANT**

### Methodology of Clifford Group Equivariant Neural Networks (CGENNs)

The methodology behind CGENNs involves leveraging the algebraic structure of Clifford algebras to create neural network layers that inherently respect geometric transformations. This section discusses how the layers are constructed, focusing on the nature of the operations, the steerability of bases, and the types of transformations that can be applied.

#### 1. **Steerable Basis and Multivector Basis**

The concept of a steerable basis in CGENNs means that the basis can be predictably transformed under the action of the Clifford group, which maintains orthogonality both in the vector space $V$ and the Clifford algebra $\text{Cl}(V, q)$. This property is crucial for ensuring that the network's operations remain consistent under geometric transformations such as rotations and reflections.

- **Advantage over Spherical Harmonics**: Unlike methods that require spherical harmonics and Clebsch-Gordan coefficients, CGENNs simplify the computational framework by using a steerable vector basis that directly induces a corresponding basis in the Clifford algebra. This reduces complexity and avoids the need for additional transformations or coefficient calculations.

#### 2. **Linear and Geometric Product Layers**

CGENNs employ two main types of layers, both derived from the properties of Clifford algebras:

- **Linear Layers**: These are formed by utilizing the linearity of polynomials restricted to the first order. For example, a transformation for an output channel can be computed using optimizable coefficients that linearly combine inputs from multiple channels. This approach is analogous to traditional neural network linear layers but adapted to handle multivectors.
  
- **Geometric Product Layers**: These layers leverage the Clifford algebra's geometric product to parameterize interactions between multivectors. By respecting grade projections, the network can handle complex interactions up to the second order directly, without losing the inherent geometric properties of the data.

#### 3. **Normalization and Nonlinearities**

To ensure stability and effectiveness in operations involving higher-order terms:
- **Normalization**: Each multivector component is normalized using a form that considers both the scalar magnitude and the extended quadratic form. This prevents numerical instabilities while maintaining important information about the magnitude.
- **Nonlinearities**: Nonlinear transformations are carefully applied to maintain equivariance. For scalar components, standard activation functions like ReLU can be used, while other components might use sigmoid functions adjusted to preserve the algebraic structure.

#### 4. **Embedding Data into the Clifford Algebra**

Data from the vector space $V$ and scalar field $R$ can be directly embedded into the appropriate scalar and vector components of the Clifford algebra. This allows the network to process and produce outputs that are directly comparable to traditional vector or scalar data, facilitating integration with existing data formats and applications.

- **Data Interpretation**: By embedding data into different grades of the Clifford algebra, CGENNs can interpret and manipulate geometric properties inherent in the data, such as orientations and magnitudes, directly through algebraic operations.

### Implications for Advanced Applications

The methodologies employed in CGENNs provide a robust framework for addressing complex problems in physics, robotics, computer vision, and other fields where data's geometric and structural properties are paramount. The ability to operate directly with data encoded as multivectors in a Clifford algebra allows these networks to perform tasks that involve intricate geometric transformations and symmetries more naturally and efficiently than traditional neural networks.

This approach not only enhances the capabilities of neural networks in handling complex geometries and transformations but also opens up new avenues for research and application in areas where understanding the underlying geometric structure of data is crucial.


---

preceding: [[why is this useful]]

See also: [[vector space]]


See also: [[clifford group equivariant neural networks]]


See also: [[quadratic forms]]


See also: [[convex hull]]


See also: [[spherical harmonics]]