Type: #atom
Atom: [[Prob & Markets (JS)]]
Subtopic: Classical Statistics
Topic: Statistics
Understanding: #Exploratory Intuition

----
# Jane Street - Probability & Markets

## Counting - Dice

*Q: What's the probability that when we roll 2 d6s and add up the results, we get 7?*
A: The guide uses a **contingency table** via multiplication rule. Simply eumerate all outcomes and use naive probability to get the result. There are 6/36 outcomes.

*Q: What's the probability of getting a sum of 10 when you roll 2 d6s?*
A: Using the same method as above, its 3/36. Note 5-5 is on the diagonal - it only happens once. But 4-6 and 6-4 are **distinct**.

*Q: What’s the probability that the product of 2 rolls of a d6 is odd? 3 rolls?*
A: We can either use multiplication rule to enumerate again or use **independence**. First we must realize an odd number can be multiplicatively decomposed (or factored) into only odd factors. So we simply use independence to multiply p(odd) x p(odd).

*Q: Suppose you fip a coin until you see heads. How many flips do you expect to need?*
A: The solution is detailed here at [CS Cornell - Tosses Till N Heads](https://www.cs.cornell.edu/~ginsparg/physics/INFO295/mh.pdf). For a single head, the answer is $1/p$. This is because $x = (1-p)(1+x) + p^1$. This is like a Markov chain or some kind of branching process.
The formula is $(p^{-n}-1) / (1-p)$. Note $x$ is expected number of flips till $n$ consecutive heads with probability $p$.

## Conditional Probability - Dice & Coins

*Q: If I flip 3 coins, what’s the probability that I get exactly 2 heads given that I get at least 1 tail?*
A: First, the list is 8 elements long (A,B,C), each element is a triple. The expanded formula is p( 2h | >1t) = p(2h & 1t) / p(>1t).  The denominator can be worked out via a list constructed from multiplication rule: It's 7/8. The numerator is 3/8. So its 3/7.

# Blitzstein

*Q: Suppose that 10 people are running a race. How many possibilities are there for the first, second, and third place winners?*
A:  This uses multiplication rule. However, due to sampling with replacement, it's 10 x 9 x 8 possibilities. The list is thus 720 elements long.

*Q: Birthday problem. Probability that at least two people share same bday (365 days) in a room of k people?*
A: Trick is to complement s.t no two people share same birthday. Then it becomes multiplication rule with sampling with replacement, so $365 \times 364 \times \cdots \times (365 - k + 1)/365^k$. The veridical paradox is that you get 0.5 if k=23.
