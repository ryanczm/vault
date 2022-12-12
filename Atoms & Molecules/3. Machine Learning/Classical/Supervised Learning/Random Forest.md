Type: #atom 
Subsubtopic: [[Bagging]]
Topic: Machine Learning
Status: #incomplete 
Level: #Exploratory Intuition

----
# Definition

Random forests are an ensemble learning method for classification and regression. Invented by 1995 by Tim Kam Ho and improved by Leo Breiman in 2006. 

# Bagging - Bootstrap Aggregation

Bagging involves bootstrapping (random sample with replacement) and aggregating votes.

## OOB Score

Out-of-bag score refers to using the trained model to predict the labels of the out-of-bag samples (not bootstrapped) across each estimator.