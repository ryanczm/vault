Type: #atom
Atom: [[Probability & Stats Qns (CZ)]]
Topic: Quant 
Level: #Exploratory 

----
# Overview

General probability questions are any questions that do not fall into the other categories. These cross into boundaries of brainteasers/logic questions. These are just pure brute force numerical simulation questions. There is some combinatorics too, but manually, without use of the binomial coefficient.

# Card Game - Card that is Larger Wins.

Q: A casino offers this game with a standard deck. You pick up a card from the deck then the dealer picks another one without replacement. If you have a larger number, you win. If equal or smaller than dealer, dealer wins. What is probability of you winning? Assume 9 < J < Q < K < A.
A: There are 3 outcomes, your card > dealer | = dealer | < dealer. By symmetry, the first and last are the same. Using complement, $p(>)=(1-p(==))/2$ and $p(==)=3/51$. So, $(1-3/51)/2=8/17$. 
R: Symmetry

# Drunk Passenger - Seat Replacement Problem

Q: 100 passengers board airline. Each hold ticket to their seat. The drunk first passenger picks a random seat. The other passengers are sober and will go to their seat unless occupied, else randomly choose a seat. What is the probability the last person (100) ends up in his seat?
A: This process is similar to ants on a ruler. Re-imagine it as every time someone finds a squatter, they evict the squatter. So the first passenger keeps getting evicted and chooses a random empty seat until by the time everyone else has boarded, he has been forced into a correct seat. When the last boarder boards, he is either in his seat 1 or the 100 (last empty seat). So 50%.
R: Symmetry.

# N Points on a Circle - Semicircle Probability

Q: Given $N$ points randomly on the circumference of a circle, what is the probability they are all within a semicircle?
A: The trick is to consider the first point, then all other points, then shuffle through all possible first points. The lead point is set. Then, the probability all other points fall in a clockwise semicircle is $1/2^{n-1}$. Repeat this for $n$ points and we have $n/2^{n-1}$. 
 
# Chance of Child Being Girl Given Girl (4.43)

Q: I have two children, at least one is a girl. What's the probability I have two girls?
A: Trick question. Wordplay is at least one is a girl. The pickpocket answer is 1/2. But realize girl could be first or second child. GG, GB, BG, BB. Exclude BB so 1/3. BG is not GB because order of the child matters.

# Expected Number of Longest Consecutive Run of Heads or Tails Qn (4.48)

Q: Let $L(N)$ be length of consecutive heads or tails in N tosses of a coin. What is $E[L(5)]-E[L(4)]?$
A: The solution is to manually enumerate through each outcome, e.g $HHTT$, then calculate expectation. E.g for 4 runs, we have 2 runs of length 1 - HTHT x 2 (transpose H and T), 8 runs of length 2. Remember symmetry.



# Probability of Maximum of 3 Dice Rolls Being a 4 Qn (4.52)

Q: You toss 3 dice. What is the probability the max of the rolls is exactly 4?
A: $P(M = 4)-P(M \leq 3)=(4/6)^3-(3/6)^3=37/216$. 
