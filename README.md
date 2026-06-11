# 70-Hour Linear Algebra Mastery Pipeline

This repository documents an intensive, production-oriented linear algebra study track.

The objective is not to merely finish textbooks or memorize procedures. The goal is to build an operational understanding of linear algebra that can be used in mathematics, numerical computing, artificial intelligence, quantitative finance, and integrated technical projects.

---

## Core Philosophy

This track follows the cycle:

1. Learn the abstract concept.
2. Understand its matrix representation.
3. Study how it is computed numerically.
4. Implement a minimal version from scratch.
5. Measure failure modes and numerical error.
6. Apply it to an AI or finance problem.
7. Defend the result without relying on memorized formulas.

The target is conceptual depth, implementation ability, and cross-domain integration.

---

## Mastery Criteria

A topic is considered complete when I can:

- Explain the main objects and assumptions in my own words.
- Reconstruct the reasoning behind the central results.
- Implement the core algorithm with NumPy.
- Identify numerical stability and conditioning problems.
- Apply the concept to a real problem.
- Explain when the method fails.
- Connect it to at least one AI or finance application.

---

## Main Resources

### Primary Theory

- Sheldon Axler — *Linear Algebra Done Right*, 4th edition

### Primary Numerical Linear Algebra

- Lloyd N. Trefethen and David Bau III — *Numerical Linear Algebra*

### Secondary Theory and Problems

- Kenneth Hoffman and Ray Kunze — *Linear Algebra*
- John M. Erdman — *Exercises and Problems in Linear Algebra*

### Advanced References

- Roger A. Horn and Charles R. Johnson — *Matrix Analysis*
- Gene H. Golub and Charles F. Van Loan — *Matrix Computations*, 4th edition
- Peter Lax — *Linear Algebra and Its Applications*

### Lectures and Notes

- MIT 18.06 — Gilbert Strang
- MIT 18.06 Lecture Notes
- MIT 18.06SC

### Papers and Surveys

- Denton, Parke, Tao, Zhang — *Eigenvectors from Eigenvalues*
- Jun Lu — *Numerical Matrix Decomposition*
- Jun Lu — *Matrix Decomposition and Applications*
- Pearce and Martinsson — *Randomized Algorithms for Low-Rank Matrix and Tensor Decompositions*
- Mataigne and Gallivan — *The Eigenvalue Decomposition of Normal Matrices by the Skew-Symmetric Part*

---

# 70-Hour Study Sequence

## 0. Setup and Matrix Language — 1.5 Hours

### Study

1. Watch the MIT 18.06 section on matrix-vector multiplication and the column picture.
2. Read Trefethen and Bau, Lecture 1: Matrix-Vector Multiplication.
3. Express matrix-vector multiplication as row-wise dot products and a linear combination of columns.
4. Implement a small `matvec()` function without NumPy matrix multiplication.
5. Explain \(Ax=b\) as a system of equations, a column combination, a linear transformation, and a geometric mapping.

### Completion Test

Explain \(Ax=b\) without relying on a memorized formula.

---

# Part I — Abstract Foundations

## 1. Vector Spaces and Subspaces — 3 Hours

### Read

- Axler: 1A, 1B, 1C
- Hoffman and Kunze: selected alternative definitions and examples

### Axler Exercises

- 1A: 7, 8, 9, 12, 15
- 1B: 1, 3, 5
- 1C: 1, 5, 9, 14, 20, 28

### Build

- Three examples of subspaces
- Three examples of sets that are not subspaces
- One direct-sum example
- One sum that is not direct
- A small Python tool that computes the rank of a span

### Completion Test

Explain the difference between a sum and a direct sum with a counterexample.

---

## 2. Span, Linear Independence, Basis, and Dimension — 4 Hours

### Read

- Axler: 2A, 2B, 2C
- Hoffman and Kunze: basis, dimension, and coordinates
- MIT 18.06: independence, basis, and dimension lectures

### Axler Exercises

- 2A: 1, 4, 8, 14, 20
- 2B: 1, 4, 7, 10
- 2C: 1, 5, 9, 14, 20

### Build

- Pivot-based independence checker
- Algorithm that reduces a spanning set to a basis
- Algorithm that extends an independent set to a basis
- Coordinate conversion between two bases

### Completion Test

Explain basis extension and dimension without reading from the book.

---

## 3. Linear Maps, Kernel, Range, and Rank-Nullity — 4 Hours

### Read

- Axler: 3A, 3B
- Hoffman and Kunze: linear transformations and isomorphisms

### Axler Exercises

- 3A: 1, 3, 6, 10, 14
- 3B: 1, 4, 8, 13, 20, 28, 33

### Build

- Linearity tester
- Null-space basis calculator
- Column-space basis calculator
- Rank and nullity checker
- Numerical verification of the rank-nullity theorem

### Completion Test

Explain injectivity through the kernel and surjectivity through the range.

---

## 4. Matrix Representation, Change of Basis, and Invertibility — 4 Hours

### Read

- Axler: 3C, 3D
- Golub and Van Loan: selected sections on matrix multiplication and block matrices
- Hoffman and Kunze: row reduction and matrix multiplication if needed

### Axler Exercises

- 3C: 1, 4, 7, 10, 14, 17
- 3D: 1, 4, 8, 12, 17, 24

### Build

- Change-of-basis matrix calculator
- Rank factorization \(A=CR\)
- Naive matrix multiplication
- Operation-count analysis

### Completion Test

Explain why the same linear map has different matrices in different bases.

---

# Part II — Eigenvalue Theory

## 5. Polynomials, Invariant Subspaces, and Eigenvalues — 4 Hours

### Read

- Axler: selected foundations from Chapter 4 and 5A
- MIT 18.06: eigenvalues and eigenvectors
- Hoffman and Kunze: characteristic values

### Axler Exercises

- Chapter 4: 1, 3, 6, 10, 14
- 5A: 1, 4, 8, 13, 19, 27, 35, 43

### Build

- Early power-iteration prototype
- Visualizations of invariant directions in \(2\times2\) transformations
- Examples of different eigenspaces for the same eigenvalue

### Completion Test

Explain an eigenvector as an invariant direction, not merely as a solution to \(Av=\lambda v\).

---

## 6. Minimal Polynomial, Triangularization, and Diagonalization — 4 Hours

### Read

- Axler: 5B, 5C, 5D, 5E
- Hoffman and Kunze: minimal polynomial and diagonalization

### Axler Exercises

- 5B: 1, 4, 8, 13, 19, 25, 29
- 5C: 1, 4, 8, 12, 16
- 5D: 1, 4, 8, 12, 17, 23
- 5E: 1, 3, 6, 10

### Build

- Diagonalizable and non-diagonalizable matrix examples
- Algebraic versus geometric multiplicity examples
- Gershgorin disk plotter
- Simultaneous diagonalization experiments

### Completion Test

Explain why distinct eigenvalues are sufficient but not necessary for diagonalizability.

---

# Part III — Orthogonality and Least Squares

## 7. Inner Products, Norms, and Gram-Schmidt — 4 Hours

### Read

- Axler: 6A, 6B
- Trefethen and Bau: Lectures 2, 3, and 7
- MIT 18.06: orthogonality and Gram-Schmidt

### Axler Exercises

- 6A: 1, 4, 8, 13, 19, 26, 34
- 6B: 1, 4, 8, 13, 19

### Build

- Classical Gram-Schmidt
- Modified Gram-Schmidt
- Orthogonality error measurement: \(\|Q^TQ-I\|\)
- Comparison on Hilbert matrices

### Completion Test

Explain the chain: inner product → norm → angle → projection → Gram-Schmidt.

---

## 8. Projection, Least Squares, and Pseudoinverse — 4 Hours

### Read

- Axler: 6C
- Trefethen and Bau: QR and least-squares lectures
- Golub and Van Loan: selected sections on orthogonalization and least squares

### Axler Exercises

- 6C: 1, 4, 8, 12, 17, 22

### Project — Least Squares Engine

Implement and compare:

- Normal equations
- QR solution
- SVD pseudoinverse

Measure residual error, solution error, runtime, and condition number.

### Completion Test

Explain why normal equations can square the condition number.

---

# Part IV — Spectral Theory and Matrix Decompositions

## 9. Adjoint, Self-Adjoint, and Normal Operators — 4 Hours

### Read

- Axler: 7A, 7B
- Horn and Johnson: normal and Hermitian matrices
- MIT 18.06: symmetric matrices and positive definiteness

### Axler Exercises

- 7A: 1, 4, 8, 13, 19, 25, 32
- 7B: 1, 4, 8, 13, 19, 25

### Build

- Random symmetric matrices
- Orthogonal eigendecomposition verification: \(A=Q\Lambda Q^T\)
- Spectral computation of matrix powers
- Matrix exponential experiment

### Completion Test

Explain why normal operators admit an orthonormal eigenbasis.

---

## 10. Positive Operators, Quadratic Forms, QR, and Cholesky — 3 Hours

### Read

- Axler: 7C, 7D, selected quadratic-form material
- Golub and Van Loan: Cholesky and Householder QR
- Horn and Johnson: positive-definite matrices and quadratic forms

### Axler Exercises

- 7C: 1, 4, 8, 13, 19, 25
- 7D: 1, 4, 8, 13, 17, 20
- Quadratic forms: 1, 4, 8, 12

### Build

- Householder QR
- Cholesky decomposition
- PSD tests using eigenvalues and Cholesky
- Quadratic-form visualizations
- Covariance-matrix interpretation

### Completion Test

Explain the connection between PSD matrices, covariance, quadratic forms, and convexity.

---

## 11. SVD, Matrix Norms, and Low-Rank Approximation — 5 Hours

### Read

- Axler: 7E, 7F
- Trefethen and Bau: Lectures 4 and 5
- Jun Lu: selected SVD and low-rank sections

### Axler Exercises

- 7E: 1, 4, 8, 12, 16
- 7F: 1, 4, 8, 13, 19, 25, 32

### Project — SVD Image Compression

- Compute SVD of a grayscale image
- Produce rank-5, rank-20, and rank-50 approximations
- Measure Frobenius error, spectral error, and compression ratio
- Plot singular-value decay
- Explain the Eckart-Young theorem

### Completion Test

Explain why SVD exists for every matrix while eigendecomposition does not.

---

# Part V — Numerical Linear Algebra

## 12. Conditioning, Stability, LU, and Pivoting — 3.5 Hours

### Read

- Trefethen and Bau: conditioning, stability, Gaussian elimination, and pivoting
- Golub and Van Loan: Chapter 3 and selected Chapter 4 sections

### Build

- LU decomposition
- Partial pivoting
- Hilbert matrix experiments
- Forward error
- Backward error
- Residual
- Condition-number analysis

### Completion Test

Explain the difference between problem conditioning and algorithmic stability.

---

## 13. Numerical Eigenvalue Algorithms — 4 Hours

### Read

- Trefethen and Bau: power iteration, inverse iteration, Rayleigh quotient iteration, Hessenberg reduction, and QR iteration
- Golub and Van Loan: selected eigenvalue chapters

### Project — Eigenvalue Algorithms Mini Lab

Implement:

- Power iteration
- Inverse iteration
- Rayleigh quotient iteration
- Basic unshifted QR algorithm

Compare convergence against the eigenvalue gap.

### Completion Test

Explain why solving \(\det(A-\lambda I)=0\) is not a practical numerical eigensolver.

---

# Part VI — Non-Diagonalizable Structures and Determinants

## 14. Generalized Eigenvectors and Jordan Form — 2 Hours

### Read

- Axler: 8A, 8B, 8C, 8D
- Hoffman and Kunze: selected canonical-form sections

### Axler Exercises

- 8A: 1, 4, 8, 13, 19, 25
- 8B: 1, 4, 8, 12
- 8C: 1, 4, 8, 12, 14
- 8D: 1, 4, 8, 13

### Build

- Jordan block generator
- Generalized eigenvector chains
- Matrix powers through Jordan form
- Basis-independence of trace

### Completion Test

Explain what generalized eigenvectors recover when diagonalization fails.

---

## 15. Determinants and the Multilinear View — 1.5 Hours

### Read

- Axler: bilinear forms, alternating multilinear forms, and determinants
- Hoffman and Kunze: determinants only if computational gaps remain

### Axler Exercises

- Bilinear forms: 1, 4, 8
- Determinants: 1, 4, 8, 13, 18, 21

### Build

Connect determinant to volume scaling, orientation, invertibility, product of eigenvalues, and row operations.

### Completion Test

Explain determinant as an alternating multilinear map.

---

# Part VII — AI and Finance Integration

## 16. PCA from Scratch and Portfolio Risk — 3.5 Hours

### Project

- Center a dataset
- Construct the covariance matrix
- Implement PCA using eigendecomposition
- Implement PCA using SVD
- Show why both methods agree
- Compute explained variance
- Apply PCA to asset returns
- Extract principal risk factors
- Check whether the covariance matrix is PSD
- Connect the result to minimum-variance portfolios

### Completion Test

Derive PCA as a variance-maximizing orthogonal projection.

---

## 17. PageRank from Scratch — 2.5 Hours

### Project

- Create a directed graph
- Construct a transition matrix
- Handle dangling nodes
- Implement power iteration
- Add a damping factor
- Compute the stationary vector
- Relate convergence to the spectral gap

### Completion Test

Explain how damping affects uniqueness and convergence.

---

## 18. Embedding Geometry Mini Lab — 2.5 Hours

### Project

- Load word or sentence embeddings
- Compute cosine similarity
- Test vector analogies
- Extract semantic directions
- Use orthogonal projection
- Apply PCA or SVD
- Plot the singular spectrum
- Estimate effective rank
- Inspect embedding anisotropy

### Completion Test

Explain what cosine similarity measures and why it can be misleading in high dimensions.

---

## 19. Randomized Low-Rank Methods and Research Window — 2 Hours

### Read

- Pearce and Martinsson: introduction, randomized range finding, and randomized SVD
- Denton, Parke, Tao, Zhang: abstract, main identity, one proof, applications, and generalizations
- Mataigne and Gallivan: abstract and introduction
- Jun Lu: CUR, skeleton, and rank-revealing decompositions

### Build

- Randomized range finder
- Randomized SVD
- Runtime and approximation-error comparison against full SVD

### Completion Test

Explain what randomization gains and what guarantees it may sacrifice.

---

# Part VIII — Final Integration

## 20. Final Integration and Oral Defense — 4 Hours

### Deliverables

- One-page concept map
- Decomposition decision table
- Unified repository containing:
  - Gram-Schmidt
  - Householder QR
  - LU
  - Cholesky
  - least squares
  - SVD image compression
  - PCA
  - power iteration
  - QR eigensolver
  - PageRank
  - portfolio-risk analysis
  - embedding geometry
  - randomized SVD

### Decomposition Decision Table

| Problem | Preferred Method |
|---|---|
| Square linear system | LU |
| Symmetric positive-definite system | Cholesky |
| Full-rank least squares | QR |
| Rank-deficient least squares | SVD |
| Symmetric eigenproblem | Symmetric eigensolver |
| Low-rank approximation | Truncated SVD |
| Large low-rank matrix | Randomized SVD |

### Final Oral Questions

1. Is a linear map the same thing as a matrix?
2. What changes when the basis changes?
3. When does eigendecomposition exist?
4. Why does SVD exist for every matrix?
5. Why can normal equations be dangerous?
6. What is the difference between conditioning and stability?
7. Why does PCA become an eigenvalue problem?
8. Why is a covariance matrix PSD?
9. When does power iteration converge?
10. How do QR, SVD, LU, and Cholesky differ?
11. What does Jordan form reveal?
12. Why is cosine similarity used in embedding spaces?

The track is complete when at least 85% of these questions can be answered clearly without opening a source.

---

# Suggested Repository Structure

```text
linear-algebra/
├── README.md
├── notes/
│   ├── 01-vector-spaces.md
│   ├── 02-basis-dimension.md
│   ├── 03-linear-maps.md
│   ├── 04-eigenvalues.md
│   ├── 05-orthogonality.md
│   ├── 06-spectral-theory.md
│   ├── 07-svd.md
│   └── 08-numerical-stability.md
├── implementations/
│   ├── matvec.py
│   ├── gram_schmidt.py
│   ├── householder_qr.py
│   ├── lu.py
│   ├── cholesky.py
│   ├── least_squares.py
│   ├── power_iteration.py
│   ├── qr_eigensolver.py
│   └── randomized_svd.py
├── projects/
│   ├── svd-image-compression/
│   ├── pca-from-scratch/
│   ├── pagerank/
│   ├── portfolio-risk/
│   └── embedding-geometry/
├── experiments/
│   ├── conditioning/
│   ├── hilbert-matrices/
│   ├── orthogonality-loss/
│   └── eigenvalue-convergence/
└── references/
    └── resource-map.md
```

---

# Current Progress

- [ ] Module 0 — Matrix language
- [ ] Module 1 — Vector spaces and subspaces
- [ ] Module 2 — Basis and dimension
- [ ] Module 3 — Linear maps
- [ ] Module 4 — Matrix representations
- [ ] Module 5 — Eigenvalues
- [ ] Module 6 — Diagonalization
- [ ] Module 7 — Inner products
- [ ] Module 8 — Least squares
- [ ] Module 9 — Spectral theorem
- [ ] Module 10 — Positive operators
- [ ] Module 11 — SVD
- [ ] Module 12 — Conditioning and stability
- [ ] Module 13 — Numerical eigensolvers
- [ ] Module 14 — Jordan form
- [ ] Module 15 — Determinants
- [ ] Module 16 — PCA and portfolio risk
- [ ] Module 17 — PageRank
- [ ] Module 18 — Embedding geometry
- [ ] Module 19 — Randomized methods
- [ ] Module 20 — Final integration

---

## First Active Block

Start with:

1. Axler 1A
2. Axler 1B
3. Axler 1C
4. Exercises:
   - 1A: 7, 8, 9, 12, 15
   - 1B: 1, 3, 5
   - 1C: 1, 5, 9, 14, 20, 28
5. Produce:
   - three subspaces
   - three non-subspaces
   - one direct sum
   - one sum that is not direct
6. Implement `span_rank.py`

Do not move to Module 2 before completing the transition test.
