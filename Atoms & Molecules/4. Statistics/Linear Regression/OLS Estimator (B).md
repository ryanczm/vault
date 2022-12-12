Type: #keyatom
Atom: [[R.S.S]]
Subtopic: Linear Regression
Understanding: #Exploratory Intuition

----
The least squares estimator, $\hat{\beta}$ is the vector of coefficients that minimizes the [[R.S.S]] of the given data. We have $y$ and $\epsilon$ being $n \times 1$, $\beta$ being  $k \times 1$ column vectors and $X$ being $n\times k$. Expand the expression of the squared residuals, noting that $\hat{\beta}'X'y=y'X\hat{\beta}$ - the scalar of a transpose is a scalar: $$\begin{gathered}e'e=(y-X\hat{\beta})'(y-X\hat{\beta})\\=y'y-y'X\hat{\beta}- \hat{\beta}'X'y+\hat{\beta}'X'X\hat{\beta}\\=y'y- 2\hat{\beta}'X'y+\hat{\beta}'X'X\hat{\beta}\end{gathered}$$
Then take the partial derivative of r.s.s w.r.t the estimator. Note the second expression uses the result for the first derivative of a quadratic form:$$\frac{\partial e'e}{\partial\hat{\beta}}=-2X'y+2X'X\hat{\beta}=0$$
The second derivative should be positive (hence a minimum) if $X$ has full rank, then $X'X$ is positive definite. Then shift one term over to get the normal equations (on the left). Take the inverse to get $$ (X'X)\hat{\beta}=X'y \quad\quad \Rightarrow \quad\quad\hat{\beta}=(X'X)^{-1}X'y$$
So far, this is assumption-free! Note it is important to distinguish between the "true" population parameter of coefficients, $\beta$ and the it's estimated value/estimator $\hat{\beta}$.  This will be used in the G-M theorem proof and calculating the covariance matrix of $\epsilon$ for assumptions.
 

------
Source: [Stanford - OLS in Matrix Form](https://web.stanford.edu/~mrosenfe/soc_meth_proj3/matrix_OLS_NYU_notes.pdf)

