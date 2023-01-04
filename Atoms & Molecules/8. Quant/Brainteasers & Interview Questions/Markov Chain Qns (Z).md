Type: #atom
Atom: [[Probability & Stats Qns (CZ)]]]
Topic: Quant 
Level: #Exploratory 

----
# Overview

These questions involve setting up the state space and Markov chain, the transition matrix and calculating some probabilities. We always start from $(S)$ - the starting state.

# Gambler's Ruin Problem

Q: Player M has 1 and N has 2. Each game gives the winner 1 from the other. M wins 2/3 games. They play someone runs out of money. What is the probability M wins?
A: We simply need to set up the transition graph from M's perspective: $(0,1,2,3)$ which starts at $1$ and calculate $a_1$ using absorption probability equations.

# Dice Question [!]

# Coin Triplets

**Absorption Time to Subsequence**

Q: Tossing a fair coin, what is expected number of tosses to see $HHH$? What about $THH$?
A: We simply need to set up the Markov chain graph, and calculate absorption time to either state. This is much more elegant than recursion.

**Absorption Probabilities of Subsequences**

Q: What is the probability you get $HHH$ before $THH$?
A: Here is an example of the graph:

![[markov_graph.png | 500]]

# Color Balls [!]
