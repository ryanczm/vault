Type: #atom
Atom: [[Logic Qns (C)]]
Topic: Quant 
Level: #Exploratory 

----
# Overview

These require you to do a low-dim simulation, then notice a pattern. E.g for screwy pirates, simply start with the 2 pirate case and increase by 1 to generalize to the $n$ pirate case. This is like induction. 

Seems to be numerical reasoning + induction step.

# Screwy Pirates Question

Q: 5 pirates loot 100 coins. Most senior pirate propose coin distribution. Then all pirates vote. If at least 1/2 accept, distribute. Else, kill most senior pirate, then repeat with the next most senior pirate. Repeat until approval. Pirates are rational. What kind of distribution will result?

A: If 2 pirates, senior can keep all the coins. At 3, pirate 1 will get nothing. So he offers pirate 1 a single coin and keep 99, so he can buy his vote. At 4, pirate 2 will get nothing, so he offers pirate 2 a coin and keep remaining. At 5, pirate 3 and 1 will get nothing. 

So, if 10 pirates, then 8, 6, 4, 2 will get coins. If 11, then 9, 7, 5, 3, 1 get coins. Increments of 2.

# Tigers & Sheep Question

Q: One hundred tigers and one sheep are put on a magic island that only has grass. Tigers can eat grass, but they would rather eat sheep. Assume: A. Each time only one tiger can eat one sheep, and that tiger itself will become a sheep after it eats the sheep. B. All tigers are smart and perfectly rational and they want to survive. So will the sheep be eaten? Assume tigers are ok with being a sheep, but just don't want to get eaten.

A: If there are 3 tigers, 1 sheep, if T3 eats sheep, T3 becomes sheep. Then, if T2 eats sheep, T2 becomes sheep and gets eaten by T1.

Therefore, if odd tigers, sheep will be eaten, if even, sheep will not. Just consider trivial case.