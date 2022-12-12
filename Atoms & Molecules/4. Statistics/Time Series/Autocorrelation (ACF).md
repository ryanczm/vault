Type: #atom 
Subsubtopic: [[Correlogram]]
Subtopic: Time Series
Topic: Statistics
Understanding: #Exploratory Intuition

----
Autocorrelation is the set of correlation coefficients (covariance) between two time series plotted on a lag plot: the original time series of the last $T-\ell$ realizations against the first $T-\ell$ realizations. $r_k$ represents the autocorrelation at lag $k$ $$r_k=\frac{\sum_{t=k+1}^T(y_t-\bar{y})(y_{t-k}-\bar{y})}{\sum_{t=1}^T(y_t-\bar{y})^2}$$
* E.g at lag 5 and 100 realizations, we rearrange the series by order, then regress the first 95 points against the last 95 points and find the line of best fit.
* Intuitively, if two sets of realizations (original and lagged) of the series are close (in value) or opposite sign, autocorrelation is high (positive or negative).
*  Somehow, an MA(q) Process signature (ideal order) corresponds to a sharp ACF cutoff.