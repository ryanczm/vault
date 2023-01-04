Type: #atom
Atom: [[Stochastic Processes Qns (Z)]]
Topic: Quant 
Status: #inprogress
Level: #Exploratory 

----
# Overview

These questions use martingale machinery, which I have not learnt yet.

# Drunk Man (Symmetric RW)
 
Q: A drunk man is on the 17th step of a 100 step bridge. He either goes forward or backwards with equal probability. What is the expected number of steps he takes to reach the beginning or end of the bridge?
A: First, set the position to $[-17,0,83]$. Then $S_n$ and $S^2_N - N$ are martingales where $N$ is the stopping time.

We find $E[S_n]=p \cdot 83 + (1-p)\cdot (-17)=0$ and so $p=0.17$. He has a $0.17$ chance of reaching the 100th step. Then the expected stopping time is $E[N]=83\cdot 17=1441$. Why? I have no idea. It seems the expected stopping time of a symmetric r.w (martingale) is the product of the normalized boundaries.

# Dice Game

# Ticket Line

# Coin Sequence
