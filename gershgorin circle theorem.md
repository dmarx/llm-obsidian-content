---
date: 1717831414.808061
tags:
- autogenerated
- source__oai
- conversation_id__ac8c3253-a669-4989-bf7c-c535d52c8140
- msg_aaa2e1c3-6e9f-423b-933d-7632d986c599
- msg_fda5387b-b98c-453c-a976-85a3a7865552
- colorclass/systems-theory
title: gershgorin circle theorem
---

**USER**

Gershgorin Circle Theorem


**ASSISTANT**

The Gershgorin Circle Theorem is a fundamental result in linear algebra that provides bounds on the location of the eigenvalues of a complex square matrix. Named after the Soviet mathematician Semyon Aranovich Gershgorin, the theorem is useful for estimating the eigenvalues and understanding their distribution without directly computing them.

## Theorem Statement

Let \( A \in \mathbb{C}^{n \times n} \) be a complex square matrix with entries \( a_{ij} \). For each row \( i \) of \( A \), define the Gershgorin disc (or Gershgorin circle) \( D_i \) centered at \( a_{ii} \) with radius \( R_i \) given by:

$$
R_i = \sum_{j \neq i} |a_{ij}|,
$$

where \( R_i \) is the sum of the absolute values of the off-diagonal elements in the \(i\)-th row.

The Gershgorin Circle Theorem states that every eigenvalue \( \lambda \) of \( A \) lies within at least one of the Gershgorin discs \( D_i \):

$$
D_i = \{ z \in \mathbb{C} : |z - a_{ii}| \leq R_i \}.
$$

In other words,

$$
\lambda \in \bigcup_{i=1}^n D_i.
$$

## Interpretation and Implications

### Geometric Visualization

- **Centers and Radii**: The center of each Gershgorin disc \( D_i \) is the diagonal element \( a_{ii} \) of the matrix \( A \), and the radius \( R_i \) is the sum of the absolute values of the off-diagonal elements in the \(i\)-th row.
- **Eigenvalue Localization**: The theorem tells us that all the eigenvalues of the matrix \( A \) are contained within the union of these \( n \) discs in the complex plane.

### Tightness of Bounds

- **Overlap of Discs**: If the Gershgorin discs overlap significantly, the bounds may not be tight, and an eigenvalue could lie in the intersection of multiple discs.
- **Disjoint Discs**: If some Gershgorin discs are disjoint, each of these discs contains exactly one eigenvalue. This can be particularly useful for matrices with well-separated diagonal elements and small off-diagonal elements.

## Example

Consider the matrix:

$$
A = \begin{pmatrix}
4 & 1 & 0 \\
2 & 3 & 1 \\
0 & 1 & 2
\end{pmatrix}.
$$

To apply the Gershgorin Circle Theorem, we compute the centers and radii of the Gershgorin discs:

1. **First Row**:
   - Center: \( a_{11} = 4 \)
   - Radius: \( R_1 = |1| + |0| = 1 \)
   - Disc: \( D_1 = \{ z \in \mathbb{C} : |z - 4| \leq 1 \} \)

2. **Second Row**:
   - Center: \( a_{22} = 3 \)
   - Radius: \( R_2 = |2| + |1| = 3 \)
   - Disc: \( D_2 = \{ z \in \mathbb{C} : |z - 3| \leq 3 \} \)

3. **Third Row**:
   - Center: \( a_{33} = 2 \)
   - Radius: \( R_3 = |1| + |0| = 1 \)
   - Disc: \( D_3 = \{ z \in \mathbb{C} : |z - 2| \leq 1 \} \)

Plotting these discs in the complex plane, we get:

- \( D_1 \): Center at \( 4 \), radius \( 1 \)
- \( D_2 \): Center at \( 3 \), radius \( 3 \)
- \( D_3 \): Center at \( 2 \), radius \( 1 \)

The union of these discs contains all the eigenvalues of \( A \).

## Further Refinements

### Gershgorin Discs for Columns

The Gershgorin Circle Theorem can also be applied to the columns of \( A \). For each column \( j \) of \( A \), define the Gershgorin disc \( D_j' \) centered at \( a_{jj} \) with radius \( R_j' \):

$$
R_j' = \sum_{i \neq j} |a_{ij}|.
$$

Then every eigenvalue of \( A \) lies within at least one of the discs \( D_j' \):

$$
\lambda \in \bigcup_{j=1}^n D_j'.
$$

### Combined Row and Column Discs

Considering both row and column Gershgorin discs can sometimes provide tighter bounds on the locations of the eigenvalues.

## Applications

### Matrix Analysis

- **Stability Analysis**: In control theory, the Gershgorin Circle Theorem helps in determining the stability of a system by locating the eigenvalues of the system matrix.
- **Preconditioning**: In numerical linear algebra, the theorem is used to analyze the effect of preconditioning on the spectrum of a matrix.

### Iterative Methods

- **Convergence Analysis**: Understanding the eigenvalue distribution helps in analyzing the convergence properties of iterative methods for solving linear systems, such as the Jacobi and Gauss-Seidel methods.

## Example: Numerical Computation

Consider the matrix:

$$
A = \begin{pmatrix}
10 & 2 & 3 \\
1 & -7 & 1 \\
2 & 3 & 15
\end{pmatrix}.
$$

To apply the Gershgorin Circle Theorem:

1. **First Row**:
   - Center: \( a_{11} = 10 \)
   - Radius: \( R_1 = |2| + |3| = 5 \)
   - Disc: \( D_1 = \{ z \in \mathbb{C} : |z - 10| \leq 5 \} \)

2. **Second Row**:
   - Center: \( a_{22} = -7 \)
   - Radius: \( R_2 = |1| + |1| = 2 \)
   - Disc: \( D_2 = \{ z \in \mathbb{C} : |z + 7| \leq 2 \} \)

3. **Third Row**:
   - Center: \( a_{33} = 15 \)
   - Radius: \( R_3 = |2| + |3| = 5 \)
   - Disc: \( D_3 = \{ z \in \mathbb{C} : |z - 15| \leq 5 \} \)

Plotting these discs, the eigenvalues of \( A \) are contained within:

- \( D_1 \): Center at \( 10 \), radius \( 5 \)
- \( D_2 \): Center at \( -7 \), radius \( 2 \)
- \( D_3 \): Center at \( 15 \), radius \( 5 \)

## Conclusion

The Gershgorin Circle Theorem provides a simple yet powerful tool for estimating the location of eigenvalues of a complex square matrix. It helps in understanding the spectral properties of matrices, aids in stability analysis, and improves the analysis of numerical methods.


---

preceding: [[transfer matrix method]]

See also: [[stability analysis]]


See also: [[control theory]]