Type: #atom
Subsubtopic: [[Classical ML Alpha Models Setup]]
Topic: Quant 
Understanding: #Exploratory  Understanding

----
# Redefining Labels - Quantile Predictions
	
In the AI4T example, the objective is to **predict quantiles a discrete integer** via winners and losers - not the direct return value itself. Hence, the label should be the forward $n$-day return $q$-quantile, where the $n$-day cross-sectional returns are divided into $q$ quantiles.  We **do not predict direct return value** because of the **low signal-to-noise ratio in financial data**.

How do we decide the number of quantiles $k$ and the lookahead period $n$? No idea ...

# Analogy between Quantile/Direction in Quant ML and Multiclass/Binary in Data Science

We can compare a **quantile forecast** to a **multiclass prediction problem** and a **directional forecast** to a **binary outcome** problem in traditional data science.

# Temporal Nature of Labels

In quant ML, the labels have a foward temporal nature - the model is forecasting/predicting **a future state**. For example, we forecast the 5-day lookahead return quantile - so the **quantized return** of the stock between the current day and 5 days ahead.

# Turning Model Predictions into Alphas

Then, the alpha vector is the **probability of prediction** (`predict_proba`) **multiplied by the quantile prediction**. This can be preprocessed accordingly (e.g rank, z-scoring).

# Overlapping Labels Problem (Temporal Overlap violates i.i.d Assumption) 

### The Problem

Overlapping labels is a problem in the quant ML setup where the labels are generated from **overlapping time periods**. E.g for a given instrument, on a Monday, the label is one week forward return quantile - on a Tuesday, the label contains 4/5 overlapping days in time.

### Simple Approach - Subsetting

One approach is subsetting - simply feed in data points with non-overlapping labels. However, if the forecast horizon is 1 month or year, this greatly reduces the number of data points.

### AFML Approach - Reduce Bag Size or Train on Non-Overlapping Labels

**Reduce Bag Sample Proportion** - MLDP suggests to reduce the bag sample proportion in a bootstrap aggregation method - So labels drawn for a single tree are less likely to overlap.

**NoOverlapVoter**  - The other method is to train separate models on non-overlapping labels then ensemble these models together So one model trains on all the Monday's for an instrument, another on the Tuesday etc. Creating a custom `NoOverlapVoter` class requires some degree of `sklearn` mastery - by building it out of the various custom parts `sklearn` offers.
