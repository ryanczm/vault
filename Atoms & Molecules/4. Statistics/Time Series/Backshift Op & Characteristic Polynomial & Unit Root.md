Type: #atom 
Atom: [[AR(p) Process]] 
Subtopic: Time Series
Topic: Statistics

----
# Backshift Operator

The lag operator is defined as $L(y_t)=y_{t-1}$. Applying this operator on a realization returns the lagged realization (behind it). It can be recursed: $L^2(y_t)=L(L(y_t))=y_{t-2}$. Generally it is defined as  $$L^ky_t=y_{t-k}$$
# Characteristic Polynomial

We can rewrite our AR(p) process from $x_t=\varphi_1y_{t-1}+\varphi_2y_{t-2}+\cdots + \varphi_p y_{t-p}+\epsilon_t$ using the lag operator: $$x_t=\varphi_1Ly_t+\cdots \varphi_pL^py_{t}+\epsilon_t$$
Shifting the lag coefficients to LHS leaving the innovations on the right and factoring out the common $x_t$ $$(1-\varphi_1L-\varphi_2L^2-\cdots-\varphi_pL^p)x_t=\epsilon_t$$
Then we have our **characteristic polynomial** $f(L)$ with coefficient (parameter) vector $\varphi$.

## Unit Roots

The root is simply solving for the value of $L$. So, simply fit the coefficients to the data using Yule-Walker OLS, then plug these coefficients in to get the c.p. Then, solve for the root of c.p and check for unity.

----
Source: [Duke Stats AR and MA Models](http://www2.stat.duke.edu/~cr173/Sta444_Fa18/slides/Lec08/Lec08.pdf)
