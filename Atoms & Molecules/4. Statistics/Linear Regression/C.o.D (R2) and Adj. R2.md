Type: #atom
Atom: [[R.S.S]] 
Subtopic: Linear Regression
Understanding: #Exploratory Intuition

----
# Coefficient of Determination ($R^2$)

The coefficient of determination $R^2$ of a linear regression model on a dataset is the proportion of explained (predicted by regressors) variance of the dependent (target) variable. One definition is $$R^2=1-\frac{R.S.S}{S.S.T}=1-\frac{e'e}{\tilde{y}'\tilde{y}}$$
Where $\tilde{y}$ is the demeaned vector. If r.s.s is minimized (better predictive power) relative to the total variance of the target variable, $R^2$ increases. Adding more predictors always increases the c.o.d - total variance remains the same, but r.s.s will decrease. To penalize this, we can use a modified version - adjusted $R^2$.

# Adjusted $R^2$
