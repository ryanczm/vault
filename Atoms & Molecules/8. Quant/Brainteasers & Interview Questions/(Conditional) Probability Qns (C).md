Type: #atom
Atom: [[Probability & Stats Qns (CZ)]]
Topic: Quant 
Level: #Exploratory 

----
# Overview

These questions often ask for a probability after giving some evidence. The trick is to **identify the events**, setup the **conditional probability formula**, convert numerator to **Bayes' rule**, and apply **LOTP to the denominator**. When using conditional probability, the bar 'given' can be replaced with 'assuming/with'.

# Dart Game - Probability of Throwing Farther from Center than First.

Q: I throw darts. D2 lands further from center than D1. If I throw D3, what is the probability D3 is farther from the center than D1? 
A: Assuming we segment the radial distance into even thirds, and assume each third has $1/3$ of being landed it, then the question asks what the chance of landing in the outer two thirds is, which is $2/3$.

# Dice Order - Probability of Strictly Increasing Order 

Q: I throw 3 dice one by one. What is the probability we obtain 3 points in strictly increasing order (same number doesn't count).
A: The answer is p(diff numbers in each throw) x p(increasing order | 3 different numbers) = $1 \cdot 5/6 \cdot 4/6 \cdot 1/6=5/54$. The last $1/6$ represents $1/3!$ for one specific permutation.

# Birthday Line (Augmented Birthday Problem) 

Q: A manager announces she will give free ticket to first person in line whose birthday is same as someone who has bought a ticket. Where to stand in line?
A: This means the $n$ people in front of you all have different birthdays from each other, and you have the same birthday as someone in the $n-1$. This is $p(n)=365 \cdot 364 \cdot (365-n-2) / 365^{n-1} \cdot (n-1)/365$. We must find a $n$ that has higher chance than standing even further back: $p(n)>p(n+1)$. Plug to find $n=20$.

# Amoeba Population  - Probability of Extinction (LOTP) 

Q: There is an amoeba in a pond. Every minute, it either: dies, same, split into 2, split into 3. Each outcome is equal probability. What is the probability it dies out in the next minute?
A: This is a clever application of the LOTP. Let $P(E)$ be the probability the amoeba dies (1). Decompose this into the conditionals: $P(E)=\sum_{i=1}^4 P(E|F_i)\cdot P(F_i)$. This is somewhat a recursion explanation. $P(E|F_1)=1$, $P(E|F_2)=P(E), P(E|F_3)=P(E)^2, P(E|F_4)=P(E)^3$. Solve for roots of a cubic polynomial.

# Candies in Jar [!]

# Coin Toss Game 2 - Subsequence Wins

Q: Two players A and B take turns to toss a fair coin. The person who wins is the last person who tosses a $T$ in a $HT$ sequence. What is the probability $A$ wins?
A: Using LOTP (recursion) - $P(A)=0.5 P(A|H) + 0.5 P(A|T)$. A winning conditional on tails resets the flip, which is equivalent to B's turn: $P(A|T)=P(B)=1-P(A)$. Now $P(A|H)=0.5 \cdot 0 + 0.5 (1-P(A|H))$. So $P(A|H)=1/3$ and $P(A)=4/9$.

# Russian Roulette Series (No Spin, Spin, Random 2, Consecutive 2)

Q: A single bullet is in a 6-chamber revolver. Two players, A and B take turns to shoot themselves. No spinning of barrel is allowed. Should you go first or second. 
A: This is a 6-chamber, 1-bullet, no-reset RR variant. You should have equal probability. If you go first, you lose if the bullet is in an odd position (1,3,5) and if you go second, you lose if the bullet is in even position (2,4,6). So equal, $1/2$.

Q: Now, we spin the barrel after every trigger pull. Who should go first?
A: Let $p$ be the probability of losing. Now we condition: $p=1 \cdot 1/6 + (1-p) \cdot (5/6)$ - we write this as a recursion relation. So $p=6/11$. So you should go second.

Q: 2 bullets are now randomly put. Your opponent is alive after the first pull. Should you spin?
A: If you spin, you have $2/6$ probability of losing. If you don't spin, you have $2/5$ chance (the opponent took up an empty slot).

Q: Exactly the same, but now the 2 bullets are consecutive. Should you spin?
A: This is the Crack variant. There are 4 empty slots the trigger could be at, and only 1 slot leads to losing (the barrel spins in 1 direction, e.g clockwise), $1/4$. If you spin, it is $1/3$ chance of dying. So you should not spin.

# Probability of Each Player Having an Ace

Q: 52 cards are randomly distributed to 4 players (13 each). What is the probability each of them have an ace?
A: First ace must belong in pile. Second ace, conditioned on not being in the first pile, is $39/51$. Following this logic, the answer is $1 \cdot 39/51 \cdot 26/50 \cdot 13/49$.

# Basketball Scores [!]

# Cars on Road in an Interval Probability

Q: If the probability of observing at least 1 car on road in 20m window is $609/625$, what is probability of seeing a car in 5m time window?
A: Trick question. The probability given is for at least one car in 20m, but the question asks for one car. So we use complement. Let the probability of seeing the car in a 5m window be $p$. So the answer is $(1-p)^4=1-609/625$ and $p=3/5$. 

# Chance of Drawing 2 Kings from a Standard Deck (4.19)

Q: What is the probability of drawing 2 kings, when drawing 2 cards from a standard 52 Deck?
A: $P(2K \& 1K)=P(2K|1K) \cdot P(1K)=\frac{3}{51}\cdot \frac{4}{52}=1/17 \cdot 1/13=1/221 \approx 0.5\%$. There is a 1 in 200 chance.

# Basketball Game (4.24)

Q: If you take a 3-pointer, you have 40% of scoring, if you take 2-pointer, you have 70% of scoring. Your team is 2 points down. If overtime, you have a 50% of winning. What should you do?
A: Informally, a 2 pointer has $0.7 \cdot 0.5=0.35$ chance of winning vs $0.40$ for a 3 pointer so you should take the 3-pointer.

# 999 Fair Coin and 1 2-Headed Coin Problem (4.29)

Q: You have jar with 999 fair coins and 1 2-headed coin. You randomly pick a coin from jar and flip it 10 times, and each time it lands heads. What is the probability you picked the 2-headed coin?
A: Let $X$ be the event it is a 2-headed coin. Let $10H$ be the event you got 10 heads from 10 tosses. Then $$\begin{flalign}P(TH |10H)=\frac{P(X \&10H)}{P(10H)}=\frac{P(10H|X)P(X)}{P(10H)}=\frac{P(10H|X)P(X)}{P(10H|X)P(X)+P(10H|X^C)P(X^C)}  \\=\frac{1 \cdot 0.001}{1\cdot 0.001+\frac{1}{2}^{10}\cdot 0.999} \approx \frac{1}{2} \end{flalign}$$
We first expand the top: the conditional probability of getting 10 heads with a 2-headed coin multiplied by the chance it is actually a 2-headed coin. This is divided by this probability itself, and the complement case.

# Water Earth Wind Fire Problem (4.30)

Q: You have 4 cards face down in front of you: water, earth, wind, fire. You turn over cards one at a time till you win or lose. You win if you turn over water or earth. You lose if you turn over fire. Probability of winning?
A: First, sample space exclusion of wind. Why? Turning over a wind changes nothing to the game. You turn over fire, you lose with $1/3$, if not continue with $2/3$. Now you have a $1/2$ chance of fire or something else and win. So it is $2/3 \cdot 1/2=1/3$.

# Coin Making Machine Problem (4.32) [!]

# Classic Disease Bayes' Problem (4.36)

Q: Disease occurs with $0.5\%$ probability. $P(+|D)=1$ and $P(+|ND)=0.07$. A random stranger tests positive. What is the probability he has the disease?
A: $P(D|+)=\frac{P(D \& +)}{P(+)}=\frac{P(+|D)P(D)}{P(+)}=\frac{P(+|D)P(D)}{P(+|D)P(D)+P(+|ND)P(ND)}=6.67\%$





