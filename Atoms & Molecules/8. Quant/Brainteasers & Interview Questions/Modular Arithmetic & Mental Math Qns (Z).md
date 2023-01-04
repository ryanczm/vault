Type: #atom
Atom: [[Nontechnical Math Qns (Z)]]
Topic: Quant 
Status: #inprogress 
Level: #Exploratory 

----

# Prisoner Problem Qn

Q: 100 prisoners in separate rooms. Each is given a red or blue hat (equal probability), so 50R-50B at random. After that, they are ushered into a common area. Then, prisoners are called out at random to guess color of own hat. Can see everyone's hat. If wrong, die, else. set free. How to devise strategy to save them?

A: First prisoner called, looks at remaining 99, if odd number of reds, he calls out red, if even, he calls out blue. Why? Because 100 (even) can be only decomposed into 2 even numbers or 2 odd numbers. He has a 50% chance. Now, the remaining 98 know, say if the previous 99 is even or odd, he can deduce - e.g if the last guy chose red, it implies even reds in the 99, so if they see even reds, they are blue, if they see odd reds, red.

A: Now extend to 3 color hats, R, G, B. Now assign scoring: R=0, G=1, B=2. First prisoner looks at his buddies and counts score and calculates $s\%3$. If remainder is 0, he declares R, 1, G, B, 2. Now the remaining prisoners can work out via the same process. E.g if first guy declares green, then the 99 score mod 3 must have a remainder of 2. If prisoner i in the 99 sees the 98 and scores 103, then he needs to adjust it so the sum mod 3 gives 2. Only 104 mod 3 gives 2 so he knows his own hat is green.

# Division by 9 Qn [!]

# Chameleon Colors Qn

Q: A remote island has 13R, 15G. 17B chameleons. Each time a pair meet, they change their color to the other color. Is it possible for all chameleons to be the same color?
A: We can try using a Markov chain to simulate this. Then, we ask if the state where only 1 color is present exists, e.g $(0,0,x)$. It doesn't because you will always end up with $(1,0,z)$ and the 0 slot will shift.

# Fractions Question (1.26)

Q: What is 13/16 and 9/16 in decimals?
A: The trick is remember a commonly known value: 1/8 = 0.125. Then, we divide this to get 1/16 = 0.0625. Notice 12/16 = 3/4, so we simply add 0.7500 + 0.0625 = 0.8125.  

# Bill Split Question (1.69)

Q: You have bill 132.67. Add 20% tip and split 6 ways. How much does each person pay?
A: The trick is to 1.2/6= 0.2=1/5. The trick is to move the decimal place and multiply by 2, so $13.267 \times 2 = 26.534$.
