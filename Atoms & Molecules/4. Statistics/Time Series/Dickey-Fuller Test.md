Type: #atom 
Atom: [[Stationarity Tests]]
Subtopic: Time Series
Topic: Statistics
Understanding: #Exploratory 

----
# Definition 

The Dickey-Fuller test tests the hypothesis that a unit root is present in the characterstic polynomial an AR process - $H_0: |z|=1 \rightarrow \phi=1$. It runs a linear regression of $\Delta x_t = x_t-x_{t-1}$ under this null hypothesis: $$\begin{gathered}X_t=\alpha+\phi x_{t-1}+\epsilon_t \\ \Delta X_t=\alpha +(\phi-1)x_{t-1}+ \epsilon_t\\ \Delta X_t=\alpha+\delta x_{t-1}+\epsilon_t\end{gathered}$$
Regress the differenced series against the 1 lagged series under the assumption that $\theta=1$ and thus $\delta=0$. Then $\delta$ is said to follow a Dickey-Fuller distribution (????) which messers Dickey and Fuller computed a table for.
