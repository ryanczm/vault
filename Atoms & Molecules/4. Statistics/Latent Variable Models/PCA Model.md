Type: #atom
Atom: [[PCA Fundamentals]] 
Subsubtopic: Latent Variable Models
Understanding: #Exploratory 

----
# Definition

Principal components analysis is a popular technique for dimensionality reduction. The idea is to compute principal components from the covariance matrix $\Sigma$ of the data, then using the p.c matrix to perform a change of basis on the data. 

# Principal Components

**Principal components** are the eigenvectors of the data's covariance matrix, pointing in **direction of largest projected variance** in the data (**minimizes projection error**), the length (**eigenvalues**) is the amount of variance explained. The largest projected variance is the data projected onto the line, then computing the variance of the projected data.

![[pca_axis.png | 300]]

Each P.C is orthogonal to each other (**symmetric matrix, spectral theorem**). Remember, any symmetric matrix of dimension $D$ has $D$ orthonormal eigenvectors and is diagonalizable (something about spectral theorem). Diagonalization transforms a matrix into two matrices of eigenvectors multiplied by a diagonal eigenvalue matrix. There is an algorithm for this.

# Why is the Eigenvector of the Covariance Matrix the Direction of Largest (Projected) Variance?

The **covariance matrix** can be seen as a linear transformation of white data into the original data. White data has identity covariance, which when applied to the white data returns itself. Just think of how the covariance matrix scales white data along different principal axes.

# Dimensionality Reduction

The formula is $$P=X \cdot U'$$where $U$ is $D \times D$ (complete eigenvector matrix), $U'$ is $D \times d$ (select first $d$ p.c) and $X$ is $n \times D$. Note the prime is not transpose here. This is projecting the data onto the new p.c bases.



