Type: #atom
Atom: [[Probability & Stats Qns (C)]]
Topic: Quant 
Status: #inprogress  
Level: #Exploratory 

----
# Overview

These questions are in similar vein to Jane Street's market making game, whereby we must bet or play some game and we need to value the cost of playing against expected payoff.

# Dollar-Pip Dice Roll Qn (4.6)
Q: How much do you charge a dice roll game where the payoff is a dollar per pip?
A: 3.5 as per expected value games.

# Dice Stopping Game Qn (4.8)

Q: I will roll a d6 no more than 3 times. You can stop at end of first roll or second or wait for third. I will pay number of dollars as pips on last roll. What is the EV and strategy of this game?
A: The trick is to calculate the future EV at each stopping point. If your previous roll awards higher than future EV, then stop. 

Working backwards, at third roll, EV is 3.5. So if you see $1,2,3$ on second roll ($1/2$ probability), you opt to continue, if you see a $4,5,6$ ($1/2$ probability), you stop. So the EV of the second roll (including the third roll option) is: $0.5 \cdot 3.5 + 0.5 \cdot (4+5+6)/3=4.25$. So if you see $1,2,3,4$ on first, you opt for second, if $5,6$, you stop. The overall EV of the game is thus $2/3 \cdot 4.25 + 1/3 \cdot (5+6)/2=4.67$.

# Two Envelopes Problem - Exchange Paradox Qn (4.10) [!]

Q: You and other person are given an envelope each. One contains $m$ and the other contains $2m$ dollars. You have no idea which is which.  Without peeking, what is your & opponents EV to switch envelopes? Should you switch? 
A: The paradox appears when you calculate $E(V)=0.5 \cdot 2m + 0.5 \cdot 0.5m=1.25m$. This means you should switch because, but your opponent calculates the same too!  This calculation is wrong. It is actually $E(V)=0.5 \cdot -m + 0.5 \cdot m=0$. Why? If you have the smaller amount, switching gains you $m$. If you have the larger, switching loses you $m$. So the EV is 0. 

# World Series Qn (4.11)

# Roll Until Number Other Than 1 Appears Qn (4.18)

Q: What is the EV of a game that rolls a die until a number other than 1 appears, with payoff being dollar pips of the last face?
A: Remove one from sample space and take EV: $(2+3+4+5+6)/5=4$

# Marble Swapping Game Qn (4.31)

Q: Two players X and Y, each with 1B 1R marble. Both present marble to each other. If both R, X wins 3. If both B, X wins 1. If different, Y wins 2. Is it better to be X or Y?
A: Well, both players have the same EV of 1. Now the trick is to calculate variance. For X, his variance is $1/2 \cdot (0-1)^2+1/2 \cdot (2-1)^2=1$ and Y variance is $1/4 \cdot (1-1)^2 + 1/4 \cdot (3-1)^2 + 1/2 \cdot (0-1)^2=1.5$. Thus, X has a higher Sharpe ratio.



