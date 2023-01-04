Type: #atom
Atom: [[Markov Chains (J)]]
Subtopic: Classical Statistics
Topic: Statistics
Understanding: #Exploratory Intuition

----
# Overview

In this note, we cover **absorption probabilities**, **absorption time** and **stationarity distribution** ideas. The first two are used in quant brainteaser questions, especially seen in the form of coin toss sequences or games. We are often asked the expected number of tosses (time) to a specific state in which the game ends (absorption) or the probability of winning (absorption probability).

# Absorption Probability

This is the probability, from one state, to enter an absorbing (cannot exit) state. To $j$, this is $a_i=P(j|X_0=i)$, the probability of absorbing into $j$ with an initial state $i$. We can use the LOTP:

**Absorption Probability Equations**

Examples are given [here (probability course)](https://www.probabilitycourse.com/chapter11/11_2_5_using_the_law_of_total_probability_with_recursion.php). Using LOTP, we write $a_i=\sum_k a_k p_{ik}$ for each state. Notably, the absorbing states are $a_0=a_0$, either 1 (itself) or 0 (another absorbing state). Then we solve for **probability**.

# Absorption Time

This is the expected number of transitions, from one state, to enter the absorbing state. This is different from the above! We use $\mu_i$ to denote time. The equations are derived [here (MIT RES 6.012 L26.7)](https://www.youtube.com/watch?v=iUF135CGTeI&ab_channel=MITOpenCourseWare).

For $\mu_i$ we have $\mu_i=1 + \sum_j p_{ij}\cdot \mu_j$. Why $1$? It is 1 (a transition time) and the expectation (transition probabilities) multiplied by the absorption time for that state.

Then the absorbing states have $\mu=0$ - why? Because if the chain is in that state, the expected time to absorption is instant - it is 0.


