Type: #atom
Atom: [[Probability & Stats Qns (C)]]
Topic: Quant 
Status: #inprogress 
Level: #Exploratory 

----
# Overview

These questions often ask for a probability after giving some evidence. The trick is to **identify the events**, setup the **conditional probability formula**, convert numerator to **Bayes' rule**, and apply **LOTP to the denominator**. When using conditional probability, the bar 'given' can be replaced with 'assuming/with'.

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





