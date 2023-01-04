Type: #atom
Atom: [[Randomness & Counting (B)]]
Subtopic: Classical Statistics
Topic: Statistics
Understanding: #Exploratory 

----
# Overview

The inclusion exclusion principle is a principle for finding the probability of a union of events when events are not necessarily disjoint. It runs alternating $-1, 1$ indices for a sum of increasing intersects.

# Two Event Case 

$$P(A \cup B)=P(A)+P(B)-P(A\cap B)$$
# Three Event Case

$$P(A \cup B \cup C)=P(A)+P(B)+P(C) - P(A \cap B) - P(A \cap C) - P(B \cap C) + P(A \cap B \cap C)$$
This can be visualized by a Venn diagram. We subtract the dual intersects, then add the combined intersect.

# N-Element Case

For the n-element case, this results in alternating plus and minus signs in increasing numbers of sums of intersection. Each sum of intersection runs through the various combinations of elements. First, we do the individual sum, subtract off the two-element case, add three-element case, minus four-element case, etc.

# Derangements

The derangement is the number of ways to permutation of elements in a set s.t no element in the set appears in the original (correct) position. The formula is $$!n=n!\sum_{i=0}^n(-1)^n/i!$$
And the probability of a derangement is simply the formula without the $n!$.
