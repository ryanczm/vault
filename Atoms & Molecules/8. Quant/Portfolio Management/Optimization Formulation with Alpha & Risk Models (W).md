Type: #atom 
Subsubtopic: [[Portfolio Optimization (W)]]
Topic: Quant 
Understanding: #Exploratory Intuition

----
# Definition

In portfolio optimization, at each time step, the **alpha model** goes into the **objective function** and the **risk model** goes into the **constraints** and rebalancing occurs. Then any convex optimization algorithm/routine is used to output the weights. We only need to **formulate the problem**. Does this apply/generalize to other instruments like a bond portfolio?

# Optimization Timeline

Realistically, one would receive data on day $t$, run the optimization on day $t+1$, then execute trades on day $t+2$. Hence, we are using at most recent 2-day lagged data. However, this means **on any given day**, we are **executing trades throughout the day** (incurring transaction costs) and doing an **optimization** for the next day.

# Objective Function - Alpha 

For a single alpha factor (e.g composite), the objective function is to maximize the portfolio alpha, simply the **sum of alpha scaled by weights** - by **adjusting weights** and a **regularization parameter**:$$\min_x: - \alpha ^T x +\lambda||x||_2$$
# Constraints - Risk

The risk constraint is to **restrict historical portfolio variance** below some **arbitrary value** (with the covariance matrix expressed in terms of a risk factor model):  $$x^T(B^TFB+S)x < c$$
# Other Constraints

**Standard constraints** - Position types include a **long-only portfolio** ($x \succeq 0$) or **dollar-neutral** $\sum_i x_i=0$ (this constraint is for weights, not alphas) which is needed even if alphas are demeaned (dollar-neutral). Why? Apaprently, alpha preprocessing is to introduce risk control to the alphas as early as possible, to ensure a high transfer coefficient.

**Leverage constraints** - To restrict a portfolio weights according to a leverage ratio: $\sum_i |x_i| < k$. If the absolute sum of weights is $>1$, then leverage is used, e.g absolute sum of 4 means the position size is 4x the capital base of 1.

**Factor exposure constraints** - We can restrict the factor exposure for each factor in a portfolio using the factor exposure matrix via $B^Tx \preceq \textbf{k}$ which limits the portfolio exposure to each factor to the constraints $\textbf{k}$.

**Position constraints** - We can also limit individual position constraints $x \succeq k_{min}$ and $x \preceq k_{max}$ .

**Turnover constraints** - We can consider using the previous position vector to implement a turnover constraint. However, this could lead to infeasible solutions. Rather, we can put the turnover into the objective function with a regularization parameter.


