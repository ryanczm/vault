Type: #atom 
Subsubtopic: [[Stationarity-Based (AR, MA)]]
Subtopic: Time Series
Topic: Statistics

----
It's important to remember both AR and MA models have a form that is **basically a linear regression of backshifted observations across a rolling window**. Then, each feature or independent predictor is simply a lagged value of the current target or dependent variable.

Then, the **equations are a form of linear regression** and the task is to estimate or find the $\beta$ vector of size lag $n$ that minimizes the error. Consider expanding each equation into a matrix form (simultaneous equations). Then we can use **OLS fitting methods** to solve for the coefficients of AR-MA models.