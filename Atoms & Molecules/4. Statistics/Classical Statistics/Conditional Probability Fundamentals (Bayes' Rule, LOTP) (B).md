Type: #atom
Atom: [[Conditional Probability (B)]]
Subtopic: Classical Statistics
Topic: Statistics
Understanding: #Exploratory Intuition

----
# The Formula

The conditional probability of A given B is the probability that both A and B occur divided by the probability B occurs. Confusing the two is called *prosecutor's fallacy*. Remember, the numerator of A and B happening can be constructed from *multiplication rule or independence*, and must capture their inter-relatedness. $$P(A|B)=\frac{P(A \&B)}{P(B)}$$
# Bayes' Rule

We can restate the numerator in terms of conditional probabilities: $P(A\&B)=P(B)P(A|B)=P(A)P(B|A)$. Now we can have Bayes' rule by substituting: $$P(A|B)=\frac{P(B|A)P(A)}{P(B)}$$
# Law of Total Probability

Now the law of total probability states the denominator can be decomposed into several conditional probabilities: $$P(B)=\sum_{i=1}^n P(B|A_i)P(A_i)$$
It says, to get unconditional probability of B, we divide the sample space into disjoint slices $A_i$, find the conditional probability of B within each slice and take their weighted sum.