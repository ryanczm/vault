Type: #atom  
Atom: [[Estimation (OLS)]]]
Subsubtopic: OLS
Topic: Statistics

----
The linear regression model specifies the setup predicting the response (outcome) variable from regressors. Suppose the data consists of $n$ observations $\{\textbf{x}_i,y_i\}^n_{i=1}$. The $i^{th}$ observation is a scalar response $y_i$ as a linear function of the regressors:$$y_i=\beta_1x_{i1}+\beta_2x_{i2}+\cdots+\beta_px_{ip}+\epsilon_i \quad \quad \leftrightarrow \quad \quad y_i=\textbf{x}_i^T\beta+\epsilon_i=\hat{y}_i+\epsilon_i$$
Expanding to the entire dataset in matrix notation: with $\textbf{y}$ and $\epsilon$ are both $n\times 1$ vectors and $X$ is an $n \times p$ design matrix with $p$ independent variables.

$$\textbf{y}=X\beta+\epsilon \quad\quad \epsilon=\textbf{y}-X\beta$$
Then the task is to find the "best" $\beta$. This is the vector that minimizes the r.s.s (if we define minimizing r.s.s as best).

