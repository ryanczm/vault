Type: #atom
Atom: [[Prob & Markets (JS)]]
Subtopic: Classical Statistics
Topic: Statistics
Understanding: #Exploratory Intuition

----
# Overview

This happens when we solve a problem that involves a (potentially) infinite series, where each term is smaller than the previous. A series of coin flips is i.i.d or memoryless. It is not Markovian!

*Q: Suppose you fip a coin until you see heads. How many flips do you expect to need?*
A: The solution is detailed here at [CS Cornell - Tosses Till N Heads](https://www.cs.cornell.edu/~ginsparg/physics/INFO295/mh.pdf). For a single head, the answer is $1/p$. This is because $x = (1-p)(1+x) + p^1$. This is like a Markov chain or some kind of branching process.
The formula is $(p^{-n}-1) / (1-p)$. Note $x$ is expected number of flips till $n$ consecutive heads with probability $p$.

