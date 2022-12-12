Type: #atom
Atom: [[Probability & Stats Qns (C)]]
Topic: Quant 
Status: #inprogress  
Level: #Exploratory 

----
# Overview

Coin toss - use **recursion** + **tree drawing**. Recursion involves setting up a recursive expression for EV which accumulates. In coin toss, it is something like EV = success case + failure case. In the failure case, you often add the existing number of coin tosses to the expectation.

# Expected Trials to Get Distinct Number of Items (4.1)

Q: Company gives away free toy in each box. 4 different toys. Expected number of boxes to buy to get all 4 toys?
A: We set up a recursion relation. $N_t$ is the number of draws required to obtain the $t^{th}$ toy having found $t-1$ toys. There is probability $p_t$ to draw it next and $1-p_t$ to not draw it. So it is $$E(N_t)=p_t \cdot 1 + (1-p_t)\cdot (1+E(N_t))$$
So we either draw it, or we have to draw again which adds to the existing draw count. Solve for $E(N_t)=1/p$. Now $E(N)=E(N_1+\cdots + N_t)=E(N_1) + \cdots + E(N_t) = 1/p_1 + \cdots + 1/p_T$. The expected number of draws is the sum of expected number of draws at each stage. This sums to $T/T + T/(T-1) + \cdots + T/2 + T/1=T \cdot \sum 1/t$  So the answer is $4 \cdot (1 + 1/2 + 1/3 + 1/4)=4+2+4/3+1=8 \frac{1}{3}$.

# 5-4 ($n, n+1$) Coin Toss More Heads Qn (4.7)

Q: A tosses 4 coins. Then B tosses 5 coins. If B gets more heads, he wins. If both get same heads, A wins. What is probability of B winning?
A: This is a trick question. The first $n$ coins have equal probability. Then the last (fifth) coin is symmetric, so both A and B have $1/2$ chance of winning. The trick is if both same heads, A wins.

# Using Coins Flips to Simulate Non-Binary Ooutcome.  (4.12, 4.13, 4.14)

Q: You have 3 children and 1 apple. Using only a fair coin to simulate which child has an equal chance of the apple, how do you do it?
A: The trick is to artificially shrink/cutoff outcomes to reduce the sample space. Simply assign $HT, TH, HH$ to the outcomes. Then, remove $TT$ from the sample space (if $TT$ is rolled, ignore it). This makes $1/3$ probability. 

Q: What is the expected number of coin tosses to complete this strategy?
A: Using recursion, $N$ is number of coin tosses. Then $E(N)= 3/4 \cdot 2 + 1/4 \cdot (2 + E(N))$. If you get $TT$ with chance quarter, you toss again, incurring $E(N)$. Anything else is 3/4. Solving to get $E(N)=2 \frac{2}{3}$.

Q: How to simulate an event with probability $1/3$ and $2/3$ with coins? 
A: If $HT, TH$ then $2/3$, if $HH$ then $1/3$. If $TT$, ignore. Sample space restriction.

# Expected Number of Coin Tosses to get N Heads in a Row Qn (4.15)

Q: What is the expected number of tosses for $N$ heads in a row with probability $p$?
A: This is a recursion question. The expected number of tosses given $X$ heads is $E(N|1H)= p \cdot 1 + (1-p)\cdot(1 + E(N|1H))$, solving this recursion gives $E(N|1H)=1/p$. Then we can solve for the 2 coin case. This is $$E(N|2H)=p \cdot (E(N|1H) +1) + (1-p)(E(N|1H+1+E(N|2H))=\frac{1+p}{p^2}$$
# Repeated Coin Toss Subsequence HHT vs HTH (Triplet) Qn (4.16)

Q: In a series of coin tosses, what is the probability you will see $HHT$ before $HTH$?
A: This is a trick question, you have to draw the tree. Start from a single $H$, you can either get $H$, in which case  $HHT$ will occur with 1/2, or get $T$, in which you need another $H$ with 1/4. So the relative probabilities are $2/3$ for $HHT$ and $1/3$ for $HTH$ (rescaling the probabilities).

# Expected Number of Tosses to see HTH Qn (4.17)

Q: What is the expected number of tosses to get HTH?
A: First, let $E(N)$ be expected number of tosses. Let $E(X|H)$ be extra tosses after a head to get HTH. Then draw the tree. $$E[N]=(1-p)(1+E[N])+p(1+E[X|H])$$
Now, we must find an expression for $E[X|H]$. We either draw heads (failure), or tails. If tails, we draw heads (success) or tails (failure - go back to start). Thus, $$E[X|H]=\frac{1}{2}(1+E[X|H])+ \frac{1}{4}(2)+\frac{1}{4}(2+E[N])$$
# Fair Die Game Stopping Payoff Qn (4.39)

Q: You roll a fair die till the game stops (if you get a 4,5,6). For every number 1,2,3, your score increases by 1. If game stops at 4 or 5 you get the score paid to you, if 6 you get nothing. What is the EV of this game?
A: $E(N)=(1/2)(0)+(1/2)(E(N)+1)$ so $E(N)=1$. Now this is $2/3 \cdot 1=2/3$.

# Box and Pebbles Game Qn (4.42)

Q: You have 4 boxes, 1,2,3,4. Pebble in box 1. You toss coin. If heads, P to B2. If tails, P to B3. Toss again. If heads, P to B1 (reset), if tails, P to B4. Reach B4 is game over. Expected number of coin toss?
A: Simple recursion. The success case takes 2 flips with probability $1/2$, the reset case takes $2+E(N)$ with probability half: $x = 0.5(2) + 0.5(2+x)$ so $E(N)=4$ 