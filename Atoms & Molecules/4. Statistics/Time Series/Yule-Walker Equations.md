Type: #atom 
Subsubtopic: [[AR & MA Model Fitting]]
Subtopic: Time Series
Topic: Statistics

----
The form of the AR or MA model problem converted to OLS matrix style is in the form of the Yule-Walker equations which must be solved to yield the model coefficients - notice how the predictors are simply lagged versions of the $y$ variable.

![[yule_walker_eqns.jpg | 400]]

Then, we can use **OLS normal equations** to solve this. But what about the full rank condition? Not sure ...