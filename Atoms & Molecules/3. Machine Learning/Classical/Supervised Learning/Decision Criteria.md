Type: #atom 
Subsubtopic: [[Decision Rule]]
Subsubtopic: Supervised Learning
Level: #Exploratory Intuition

----
The decision criteria evaluates all the samples in the current node to determine the optimal feature and threshold to set the decision rule. In general, it must iterate through all different thresholds and features for all samples to find the optimal parameters for the decision rule (the chosen feature and threshold). To improve computational speed (reduce total iterations), certain shortcuts can be used.

## Discrete Case

The thresholds are class labels. The The processor iterates through all data in the sample and picks the feature and thresholds that minimizes the weighted average of Gini impurity or entropy for the child nodes (minimum entropy!!) until the nodes are pure (each node contains only a single class).


**Continuous Case**

The thresholds are a certain target value. The processor iterates through all data in the sample and picks the feature and thresholds that minimizes total S.S.E for the child nodes.




---
Source: Probabilistic Machine Learning - An Introduction (Murphy)