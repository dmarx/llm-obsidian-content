---
date: '2025-06-27T04:36:02.692946Z'
tags:
- autogenerated
- source__claude
- conversation_id__62e42488-8b00-4ba8-9cb1-6059b8548954
- msg_ee9b4760-531f-4af1-909f-0d7f7629a526
- msg_47b84226-8d30-460c-bdf9-3ea31b8a4e1b
- colorclass/ecology
title: biogeographic patterns
---

**USER**

biogeographic patterns


**ASSISTANT**

The user is asking about biogeographic patterns. This should be a comprehensive technical wiki entry covering various patterns in biogeography, their mathematical descriptions, and underlying mechanisms. I need to provide detailed mathematical formalisms, as requested in the initial instructions, while maintaining the wiki format and including many internal links to related concepts.

Key topics to cover:
1. Species-area relationships
2. Distance-decay relationships
3. Latitudinal diversity gradients
4. Island biogeography
5. Range size distributions
6. Nested biotas
7. Endemism patterns
8. Phylogeographic patterns
9. Beta diversity patterns
10. Turnover and nestedness
11. Spatial autocorrelation
12. Scaling relationships
13. Geographic range limits
14. Migration patterns
15. Dispersal limitation effects
16. Environmental gradients
17. Climate-diversity relationships
18. Continental patterns
19. Marine biogeography
20. Applied biogeography

I should include mathematical models, statistical frameworks, and computational approaches for each pattern type.# Biogeographic Patterns

## Theoretical Foundation

[[Biogeographic patterns]] represent systematic spatial and temporal variations in [[species diversity]], [[community composition]], and [[phylogenetic structure]] across geographic gradients. These patterns emerge from the interplay between [[ecological processes]], [[evolutionary dynamics]], [[dispersal limitations]], and [[environmental heterogeneity]] operating across multiple spatial and temporal scales.

The fundamental [[biogeographic state]] can be characterized by the [[species-by-site matrix]]:

$$\mathbf{X} = \begin{pmatrix}
x_{11} & x_{12} & \cdots & x_{1n} \\
x_{21} & x_{22} & \cdots & x_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
x_{m1} & x_{m2} & \cdots & x_{mn}
\end{pmatrix}$$

where $x_{ij}$ represents the [[abundance]] or [[presence]] of species $i$ at site $j$, with $m$ species and $n$ sites.

## Species-Area Relationships

### Power-Law Scaling

The [[species-area relationship]] (SAR) represents one of the most fundamental patterns in biogeography:

$$S = cA^z$$

where $S$ is [[species richness]], $A$ is [[area]], $c$ is the [[intercept parameter]], and $z$ is the [[scaling exponent]]. Taking logarithms yields:

$$\log S = \log c + z \log A$$

### Scaling Exponents

Typical values of the [[SAR exponent]] vary by context:
- [[Continental areas]]: $z \approx 0.10-0.25$
- [[Island systems]]: $z \approx 0.20-0.35$  
- [[Habitat fragments]]: $z \approx 0.12-0.50$
- [[Sampling plots]]: $z \approx 0.15-0.30$

### Alternative SAR Models

**[[Arrhenius model]]** (power-law):
$$S = cA^z$$

**[[Gleason model]]** (semi-logarithmic):
$$S = c + z \log A$$

**[[Logarithmic model]]**:
$$S = c \log A$$

**[[Asymptotic models]]**:
$$S = \frac{S_{\max} A}{A + k}$$

where $S_{\max}$ is the [[asymptotic richness]] and $k$ is the [[half-saturation constant]].

### Mechanistic SAR Models

[[Random placement models]] predict:

$$S = S_{\gamma} \left[1 - \left(1 - \frac{A}{A_{\gamma}}\right)^n\right]$$

where $S_{\gamma}$ is [[gamma diversity]], $A_{\gamma}$ is total area, and $n$ represents [[individual density]].

[[Neutral SAR]] under dispersal limitation:

$$S = \theta \ln\left(1 + \frac{A \rho}{\theta}\right)$$

where $\theta$ is the [[fundamental biodiversity number]] and $\rho$ is [[individual density]].

## Distance-Decay Relationships

### Exponential Decay

[[Community similarity]] declines with geographic distance following:

$$S(d) = S_0 e^{-d/D}$$

where $S(d)$ is [[similarity]] at distance $d$, $S_0$ is [[initial similarity]], and $D$ is the [[decay constant]].

### Power-Law Decay

Alternative formulations include [[power-law decay]]:

$$S(d) = S_0 d^{-\alpha}$$

where $\alpha$ is the [[decay exponent]].

### Similarity Indices

Common [[similarity measures]] include:

**[[Jaccard similarity]]:**
$$J = \frac{|A \cap B|}{|A \cup B|}$$

**[[Sørensen similarity]]:**
$$S_{Sor} = \frac{2|A \cap B|}{|A| + |B|}$$

**[[Bray-Curtis similarity]]:**
$$BC = 1 - \frac{\sum_i |x_{i1} - x_{i2}|}{\sum_i (x_{i1} + x_{i2})}$$

### Decay Mechanisms

[[Distance-decay]] emerges from:
- [[Dispersal limitation]]: $p(dispersal) \propto e^{-d/D_i}$
- [[Environmental correlation]]: $r(d) = r_0 e^{-d/D_e}$
- [[Neutral drift]]: [[Isolation by distance]] effects
- [[Historical factors]]: [[Vicariance]] and [[colonization]] patterns

## Latitudinal Diversity Gradients

### Canonical Pattern

[[Species richness]] typically increases toward the equator:

$$S(\phi) = S_0 \exp(-\alpha \phi^2)$$

where $\phi$ is [[absolute latitude]] and $\alpha$ determines [[gradient steepness]].

### Alternative Gradient Models

**[[Exponential decline]]:**
$$S(\phi) = S_{eq} e^{-\lambda \phi}$$

**[[Polynomial models]]:**
$$S(\phi) = \beta_0 + \beta_1 \phi + \beta_2 \phi^2 + \beta_3 \phi^3$$

**[[Sigmoid models]]:**
$$S(\phi) = \frac{S_{max}}{1 + e^{k(\phi - \phi_0)}}$$

### Mechanistic Hypotheses

**[[Temperature hypothesis]]:**
$$S = f(T) = \alpha e^{E_a/(kT)}$$

where $E_a$ is [[activation energy]] and $T$ is [[absolute temperature]].

**[[Productivity hypothesis]]:**
$$S = f(NPP) = c \cdot NPP^{\beta}$$

where $NPP$ is [[net primary productivity]].

**[[Area hypothesis]]:**
$$S = f(A_{tropical}/A_{temperate})$$

accounting for differential [[land area]] across latitudes.

### Evolutionary Hypotheses

**[[Time hypothesis]]:**
$$S_{tropical} = S_0 e^{rt}$$

where $r$ is [[speciation rate]] and $t$ is [[time available]].

**[[Diversification rate]]:**
$$\frac{dS}{dt} = \lambda S - \mu S$$

with latitude-dependent [[speciation]] ($\lambda$) and [[extinction]] ($\mu$) rates.

## Island Biogeography

### MacArthur-Wilson Model

The [[equilibrium theory of island biogeography]] predicts:

$$\frac{dS}{dt} = I(S) - E(S)$$

where $I(S)$ is [[immigration rate]] and $E(S)$ is [[extinction rate]].

**[[Immigration function]]:**
$$I(S) = I_0 \left(1 - \frac{S}{P}\right)$$

where $I_0$ is [[maximum immigration rate]] and $P$ is the [[species pool]].

**[[Extinction function]]:**
$$E(S) = E_0 \frac{S}{K}$$

where $E_0$ is [[extinction coefficient]] and $K$ is [[carrying capacity]].

### Equilibrium Richness

Setting $I(S^*) = E(S^*)$ yields:

$$S^* = \frac{I_0 P K}{I_0 K + E_0 P}$$

### Area and Isolation Effects

**[[Area effect]]** on extinction:
$$E_0 = e_0 A^{-\beta}$$

**[[Isolation effect]]** on immigration:
$$I_0 = i_0 e^{-\gamma d}$$

where $d$ is [[distance to mainland]].

### Island SAR

Combining area and isolation effects:

$$S = c A^z d^{-w}$$

where $w$ is the [[isolation exponent]].

## Range Size Distributions

### Frequency Distributions

[[Geographic range sizes]] often follow [[log-normal distributions]]:

$$f(r) = \frac{1}{r\sigma\sqrt{2\pi}} \exp\left(-\frac{(\ln r - \mu)^2}{2\sigma^2}\right)$$

where $r$ is [[range size]], $\mu$ is the [[log-mean]], and $\sigma$ is the [[log-standard deviation]].

### Rapoport's Rule

[[Range size]] increases with latitude:

$$R(\phi) = R_0 + \alpha \phi$$

where $R(\phi)$ is [[mean range size]] at latitude $\phi$.

### Range Size Rarity

The relationship between [[range size]] and [[local abundance]]:

$$A = \beta R^{\gamma}$$

where $A$ is [[local abundance]] and $\gamma \approx 0.25$ (the [[one-quarter power rule]]).

## Beta Diversity Patterns

### Additive Partitioning

[[Beta diversity]] can be partitioned as:

$$\gamma = \alpha + \beta$$

where $\gamma$ is [[gamma diversity]], $\alpha$ is [[alpha diversity]], and $\beta$ is [[beta diversity]].

### Multiplicative Partitioning

Alternative partitioning:

$$\gamma = \alpha \times \beta$$

with $\beta = \gamma/\alpha$.

### Beta Diversity Components

[[Nestedness]] and [[turnover]] components:

$$\beta_{total} = \beta_{turnover} + \beta_{nestedness}$$

**[[Turnover component]]:**
$$\beta_{turnover} = \frac{2\min(b,c)}{2a + b + c}$$

**[[Nestedness component]]:**
$$\beta_{nestedness} = \frac{|b-c|}{2a + b + c} \times \frac{a}{a + \min(b,c)}$$

where $a$ is [[shared species]], $b$ and $c$ are [[unique species]] in each community.

## Endemism Patterns

### Endemism Indices

**[[Weighted endemism]]:**
$$WE = \sum_{i=1}^S \frac{1}{R_i}$$

where $R_i$ is the [[range size]] of species $i$.

**[[Corrected weighted endemism]]:**
$$CWE = \frac{WE}{S}$$

### Endemic Species-Area Relationships

[[Endemic species]] richness often follows:

$$S_{endemic} = c_{e} A^{z_e}$$

with typically $z_e > z_{total}$.

### Hotspots of Endemism

[[Centers of endemism]] identified using:

$$EI = \frac{S_{endemic}}{S_{total}}$$

where $EI$ is the [[endemism index]].

## Phylogeographic Patterns

### Phylogenetic Diversity

**[[Faith's phylogenetic diversity]]:**
$$PD = \sum_{b \in T} l_b$$

where $T$ is the [[minimum spanning tree]] and $l_b$ are [[branch lengths]].

### Phylogenetic Endemism

**[[Phylogenetic endemism]]:**
$$PE = \sum_{b \in T} \frac{l_b}{R_b}$$

where $R_b$ is the [[range size]] of [[clade]] $b$.

### Phylogenetic Beta Diversity

**[[UniFrac distance]]:**
$$d_{UniFrac} = \frac{\sum_{b \in A \triangle B} l_b}{\sum_{b \in A \cup B} l_b}$$

where $A \triangle B$ represents [[symmetric difference]].

### Molecular Clocks

[[Divergence time]] estimation:

$$t = \frac{d}{2\mu}$$

where $d$ is [[genetic distance]] and $\mu$ is [[mutation rate]].

## Spatial Autocorrelation

### Moran's I

[[Global spatial autocorrelation]]:

$$I = \frac{n \sum_i \sum_j w_{ij}(x_i - \bar{x})(x_j - \bar{x})}{\sum_i \sum_j w_{ij} \sum_i (x_i - \bar{x})^2}$$

where $w_{ij}$ are [[spatial weights]] and $\bar{x}$ is the [[global mean]].

### Geary's C

Alternative autocorrelation measure:

$$C = \frac{(n-1) \sum_i \sum_j w_{ij}(x_i - x_j)^2}{2 \sum_i \sum_j w_{ij} \sum_i (x_i - \bar{x})^2}$$

### Local Indicators

**[[Local Moran's I]]:**
$$I_i = \frac{x_i - \bar{x}}{s^2} \sum_j w_{ij}(x_j - \bar{x})$$

where $s^2$ is the [[sample variance]].

### Spatial Weights

Common [[weight matrices]]:

**[[Contiguity weights]]:**
$$w_{ij} = \begin{cases}
1 & \text{if sites } i \text{ and } j \text{ are adjacent} \\
0 & \text{otherwise}
\end{cases}$$

**[[Distance weights]]:**
$$w_{ij} = \frac{1}{d_{ij}^{\alpha}}$$

**[[Gaussian weights]]:**
$$w_{ij} = \exp\left(-\frac{d_{ij}^2}{2h^2}\right)$$

## Range Limits and Boundaries

### Climate Envelope Models

[[Species distribution models]] predict [[occurrence probability]]:

$$P(presence) = \frac{\exp(\beta_0 + \sum_i \beta_i x_i)}{1 + \exp(\beta_0 + \sum_i \beta_i x_i)}$$

where $x_i$ are [[environmental variables]].

### Thermal Tolerance

[[Temperature-limited distributions]]:

$$P(T) = \exp\left(-\frac{(T - T_{opt})^2}{2\sigma_T^2}\right)$$

where $T_{opt}$ is [[thermal optimum]].

### Dispersal-Limited Ranges

[[Reaction-diffusion models]]:

$$\frac{\partial N}{\partial t} = D \nabla^2 N + rN\left(1 - \frac{N}{K}\right)$$

with [[traveling wave]] solutions:

$$N(x,t) = N^*(x - ct)$$

where $c = 2\sqrt{Dr}$ is [[wave speed]].

## Scaling Relationships

### Nested Hierarchy

[[Hierarchical species-area curves]]:

$$S = c_k A^{z_k}$$

where $k$ indexes [[spatial scales]] and typically $z_1 < z_2 < ... < z_n$.

### Scale Transitions

[[Triphasic SARs]] exhibit three scaling regimes:
1. **Small scales**: $z \approx 0.05-0.15$ (local [[sampling effects]])
2. **Intermediate scales**: $z \approx 0.15-0.35$ (regional [[habitat heterogeneity]])
3. **Large scales**: $z \approx 0.05-0.25$ ([[biogeographic provinces]])

### Fractal Geometry

[[Fractal dimensions]] of species ranges:

$$N(r) \propto r^{-D}$$

where $N(r)$ is the number of [[occupied cells]] at resolution $r$ and $D$ is the [[fractal dimension]].

## Environmental Gradients

### Gradient Analysis

[[Canonical correspondence analysis]] relates species to environment:

$$\mathbf{Y} = \mathbf{X}\mathbf{B} + \mathbf{E}$$

where $\mathbf{Y}$ is the [[species matrix]], $\mathbf{X}$ is the [[environmental matrix]], and $\mathbf{B}$ contains [[regression coefficients]].

### Generalized Linear Models

[[Species-environment relationships]]:

$$\log(\mu_i) = \beta_0 + \sum_j \beta_j x_{ij}$$

for [[Poisson-distributed]] abundances.

### Gaussian Response Models

[[Unimodal species responses]]:

$$y_i = c_i \exp\left(-\frac{(x - u_i)^2}{2t_i^2}\right)$$

where $u_i$ is the [[environmental optimum]] and $t_i$ is [[tolerance]].

## Climate-Diversity Relationships

### Temperature-Richness Models

**[[Metabolic theory]]** predictions:

$$S \propto \exp\left(\frac{-E}{kT}\right)$$

where $E \approx 0.65$ eV is [[activation energy]].

### Water-Energy Dynamics

[[Dual limitation]] models:

$$S = f(\min(W, E))$$

where $W$ represents [[water availability]] and $E$ represents [[energy availability]].

### Climate Velocity

[[Range shift]] requirements:

$$v_{required} = \frac{\partial T/\partial t}{|\nabla T|}$$

where $v_{required}$ is [[required migration velocity]].

## Marine Biogeography

### Pelagic Patterns

[[Marine diversity]] patterns differ from terrestrial:

$$S_{marine}(\phi) = S_0 + \alpha \phi + \beta \phi^2$$

often showing [[bimodal]] latitudinal patterns.

### Ocean Basin Effects

[[Connectivity]] between ocean basins:

$$F_{ij} = k \frac{A_i A_j}{d_{ij}^2}$$

where $F_{ij}$ is [[gene flow]] between basins $i$ and $j$.

### Depth Gradients

[[Bathymetric diversity]]:

$$S(z) = S_0 \exp(-\alpha z)$$

where $z$ is [[depth]].

## Continental Patterns

### Continental SAR

[[Continental species-area relationships]]:

$$S = c A^z$$

with $z \approx 0.12-0.25$ for most taxa.

### Peninsular Effects

[[Species richness]] declines along peninsulas:

$$S(d) = S_0 - \alpha d$$

where $d$ is [[distance from mainland]].

### Mountain Diversity

[[Elevational gradients]]:

$$S(E) = S_0 + \alpha E + \beta E^2$$

often showing [[hump-shaped]] patterns.

## Temporal Biogeography

### Species Accumulation

[[Species accumulation curves]]:

$$S(t) = S_{\infty} \left(1 - e^{-kt}\right)$$

where $k$ is the [[accumulation rate]].

### Colonization Dynamics

[[Time-series SAR]]:

$$S(A,t) = c A^z t^w$$

incorporating [[temporal scaling]].

### Turnover Rates

[[Species turnover]]:

$$T = \frac{C + E}{S_{avg}}$$

where $C$ is [[colonizations]], $E$ is [[extinctions]], and $S_{avg}$ is [[average richness]].

## Statistical Methods

### Spatial Regression

[[Spatial autoregressive models]]:

$$\mathbf{y} = \rho \mathbf{W}\mathbf{y} + \mathbf{X}\boldsymbol{\beta} + \boldsymbol{\epsilon}$$

where $\mathbf{W}$ is the [[spatial weight matrix]] and $\rho$ is the [[autoregression parameter]].

### Geographically Weighted Regression

[[Local regression]] models:

$$y_i = \beta_0(u_i, v_i) + \sum_k \beta_k(u_i, v_i) x_{ik} + \epsilon_i$$

where coefficients vary with [[geographic coordinates]] $(u_i, v_i)$.

### Mantel Tests

[[Matrix correlation]]:

$$r_M = \frac{\sum_i \sum_j (x_{ij} - \bar{x})(y_{ij} - \bar{y})}{\sqrt{\sum_i \sum_j (x_{ij} - \bar{x})^2 \sum_i \sum_j (y_{ij} - \bar{y})^2}}$$

### Eigenvector Mapping

[[Moran's eigenvector maps]]:

$$\mathbf{y} = \mathbf{X}\boldsymbol{\beta} + \mathbf{E}\boldsymbol{\gamma} + \boldsymbol{\epsilon}$$

where $\mathbf{E}$ contains [[spatial eigenvectors]].

## Macroecological Rules

### Bergmann's Rule

[[Body size]] increases with latitude:

$$\log(M) = \alpha + \beta \phi$$

where $M$ is [[body mass]] and $\phi$ is [[latitude]].

### Allen's Rule

[[Appendage size]] decreases with latitude:

$$L/M = \alpha - \beta \phi$$

where $L$ is [[appendage length]].

### Gloger's Rule

[[Pigmentation]] increases in warm, humid climates:

$$P = f(T, H)$$

where $P$ is [[pigmentation intensity]], $T$ is [[temperature]], and $H$ is [[humidity]].

## Network Biogeography

### Habitat Networks

[[Landscape connectivity]]:

$$\mathbf{C} = \exp(-\alpha \mathbf{D})$$

where $\mathbf{D}$ is the [[distance matrix]].

### Bipartite Networks

[[Species-site networks]]:

$$\mathbf{A} = \begin{pmatrix}
\mathbf{0} & \mathbf{B} \\
\mathbf{B}^T & \mathbf{0}
\end{pmatrix}$$

where $\mathbf{B}$ is the [[incidence matrix]].

### Network Metrics

**[[Connectance]]:**
$$C = \frac{L}{S \times N}$$

where $L$ is [[link density]], $S$ is [[species richness]], and $N$ is [[site number]].

**[[Nestedness]]:**
$$NODF = \frac{100}{N_{pairs}} \sum_{pairs} \frac{DF_{ij}}{max(k_i, k_j)}$$

where $DF_{ij}$ is [[decreasing fill]] and $k_i$ is [[degree]].

## Conservation Biogeography

### Reserve Selection

[[Systematic conservation planning]]:

$$\min \sum_i c_i x_i$$

subject to:
$$\sum_i a_{ij} x_i \geq t_j, \quad \forall j$$

where $x_i \in \{0,1\}$ indicates [[reserve selection]], $c_i$ are [[costs]], $a_{ij}$ is [[species representation]], and $t_j$ are [[targets]].

### Gap Analysis

[[Conservation gaps]]:

$$Gap_j = \max(0, t_j - \sum_i a_{ij} p_i)$$

where $p_i$ is [[protection level]].

### Complementarity

[[Complementarity algorithm]]:

$$Score_i = \sum_j w_j \times I(species \, j \, present \, in \, site \, i)$$

where $w_j$ are [[species weights]] based on [[representation shortfalls]].

## Computational Methods

### Species Distribution Modeling

[[MaxEnt]] models use [[maximum entropy]]:

$$\hat{f}(x) = \frac{\exp(\sum_i \lambda_i f_i(x))}{Z}$$

where $f_i$ are [[feature functions]] and $Z$ is the [[partition function]].

### Machine Learning

[[Random Forest]] for biogeographic prediction:

$$\hat{y} = \frac{1}{B} \sum_{b=1}^B T_b(x)$$

where $T_b$ are [[decision trees]].

### Deep Learning

[[Convolutional neural networks]] for spatial patterns:

$$y = f_{CNN}(\mathbf{X}_{spatial}) = \sigma(\mathbf{W} * \mathbf{X} + b)$$

### Bayesian Methods

[[Hierarchical Bayesian models]]:

$$S_i \sim \text{Poisson}(\lambda_i)$$

$$\log(\lambda_i) = \alpha + \boldsymbol{\beta}^T \mathbf{x}_i + \phi_i$$

$$\phi_i | \phi_{-i} \sim \mathcal{N}(\bar{\phi}_i, \tau^2)$$

## Research Frontiers

### Big Data Biogeography

[[Citizen science]] data integration:

$$\mathbf{y}_{obs} = \mathbf{y}_{true} + \boldsymbol{\epsilon}_{detection} + \boldsymbol{\epsilon}_{bias}$$

### Remote Sensing

[[Satellite-based]] diversity monitoring:

$$S = f(\text{NDVI}, \text{EVI}, \text{LAI}, ...)$$

### Environmental DNA

[[eDNA]] biogeography:

$$P(species) = \frac{\text{DNA reads}}{\text{Total reads}} \times \text{correction factors}$$

### Climate Change Biogeography

[[Range shift]] projections:

$$\frac{\partial N}{\partial t} = D \nabla^2 N + rN - \frac{\partial}{\partial x}(v(x,t) N)$$

where $v(x,t)$ is [[climate velocity]].

### Phylogenetic Biogeography

[[Ancestral range reconstruction]]:

$$P(range_A | range_B, range_C) = \frac{e^{Q_{BC \to A} t}}{Z}$$

### Network Biogeography

[[Multilayer networks]]:

$$\mathcal{M} = \{G_\alpha\}$$

where $\alpha$ indexes [[interaction types]].

### Machine Learning Integration

[[Graph neural networks]] for biogeographic prediction:

$$\mathbf{h}_v^{(l+1)} = \sigma\left(\mathbf{W}^{(l)} \text{AGG}\{h_u^{(l)} : u \in \mathcal{N}(v)\}\right)$$

### Quantum Biogeography

[[Quantum superposition]] of [[biogeographic states]]:

$$|\Psi\rangle = \sum_i \alpha_i |S_i\rangle$$

### Information Theory

[[Information-theoretic]] biogeography:

$$I(S; E) = H(S) - H(S|E)$$

measuring [[mutual information]] between [[species]] and [[environment]].

### Causal Biogeography

[[Causal inference]] in biogeographic patterns:

$$S \leftarrow E \rightarrow T \rightarrow S$$

using [[directed acyclic graphs]] for [[mechanistic understanding]].


---

preceding: [[assembly convergence]]  


following: [[microaggregate stability]]

See also: [[correspondence analysis]]


See also: [[diffusion models]]