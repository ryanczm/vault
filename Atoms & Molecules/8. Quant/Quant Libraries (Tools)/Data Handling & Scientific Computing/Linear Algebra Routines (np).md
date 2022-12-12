Type: #atom
Atom: [[Math-Based Routines (np)]]
Topic: Quant
Understanding: #Exploratory 

----
# Overview

**Dual Namespace** - From docs, linear algebra operations are accessed directly, like `np.dot(a,b)`, or under `linalg` submodule, so `np.linalg.svd(a)`. 

**Overlap with SciPy** `linalg` - NumPy's `linalg` has lots of overlap with Scipy's `linalg`, many same functions.

# Matrix and Vector Multiplication

For simplicity, simply use the general purpose `@` operator. It works between vectors, matrix-vector and matrix-matrix cases. 

# Decompositions

Offeres `np.linalg.cholesky(a)`, `np.linalg.qr(a)`, `np.linalg.svd(a)`.

# Eigenvalues

Offers `np.eig(a)`, which returns eigenvalues and (normalized) eigenvectors.

# Misc

Important ones are `np.linalg.norm(x)` (vector norms), determinants via `np.linalg.det(a)`, rank via `np.linalg.matrix_rank(a)`, and trace `np.linalg.trace(a)`.

# Solving & Inversion

We have inverse, `np.linalg.inv(a)`, Moore-Penrose pseudoinverse `np.linalg.pinv(a)` and `np.linalg.solve(a,b)`.