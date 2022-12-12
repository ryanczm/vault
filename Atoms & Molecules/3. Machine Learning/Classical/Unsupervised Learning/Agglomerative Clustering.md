Type: #atom 
Atom: [[Hierarchical Clustering]]
Topic: Machine Learning
Understanding: #Exploratory Intuition

----
# Overview

Agglomerative clustering seeks to continuously merge clusters. For each point, compute the distances to all other points. Group two the nearest points into a cluster (shortest distance). Compute the linkage from that cluster to all other points and put it in the distance table. Repeat until everything is clustered.

Visually, we can represent the result as a dendrogram and cut the height of the tree to get our final clusters.

# Affinity (Distance Measures)

E.g Euclidean, L1, L2, Manhattan, cosine, etc. The fundamental building block.

# Linkage

Ward, complete, average, single. This is a composition build from distance metrics.