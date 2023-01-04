Type: #atom
Atom: [[Quantitative & Logic Qns (CZ]]
Topic: Quant 
Level: #Exploratory 

----
# Conservation Questions

These involve some underlying quantity that is constant for multiple parties. Then it becomes simultaneous equations. The trick is to identify and estimate the underlying conserved quantity - e.g volume, distance, time, weight. This can be represented by some unknown variable like $X$ or $\gamma$ or whatever symbol.

# Wine-Water Mixing Problem (1.1)

Q: Two jugs, one water and one alcohol of volume $V$. First, $Q$ water is transferred to the alcohol jug. Then, $Q$ water-alcohol is transferred back to the water jug. What is the ratio of concentrations of alcohol in alcohol jug to water in water jug?

A: Identical. Volume is conserved. If volume is conserved and the end volume is equal in both jugs, then both must have the same concentration. Consider 6W and 6A. Then consider 3W and 6A + 3W. We take 2A + 1W and transfer back. 4W + 2A and 4A + 2W. This is the [Wine/Water Mixing Problem](https://en.wikipedia.org/wiki/Wine/water_mixing_problem).

This assumes homogenous mixing (e.g uniform compositon)

# Escalator Steps (1.2)

Q: A and B are climbing on a moving escalator, they start side-by-side. A moves 1.5 times speed of B (3 steps per 2 steps). A counts 25 steps. B counts 20 steps. How many steps are showing on the escalator?

A: The trick is to realize the escalator has the same length $D$ for both people. This distance is linearly broken down into escalator carry and self carry (velocity and distance are linear). Self carry is stated (25 and 20). Escalator carry is a linear function of time spent on the escalator.

So we can solve for $D$ by equating $D=25 + x$ and $D = 25 + kx$. $x$ is A's escalator carry and $kx$ is B's escalator carry. $k$ is the ratio of time $B$ took to $A$ on the escalator.

To find $k$, we have $T_b/T_a=\frac{20}{V_b} / \frac{25}{V_a}=\frac{20}{2} / \frac{25}{3}=1.2$, then substitute to find $D=50$.

# Bell Ringing Problem (1.3)

Q: One bell rings 4 times per minute, the other rings 5 times per minute. They start at the same time and ring at evenly spaced intervals. When will they ring together?

A: The conserved quantity is time. Notice after 1 minute, they ring together. LCD of 12.5 and 15 is 60.

# Clock Pieces Problem (1.5)

Q: Analog clock falls down onto ground and splits into 3 pieces, each piece, the numbers add up.
A: The conserved quantity is 78 (sum from 1 to 12). 78/3=26. Pieces are 5-6-7-8, 11-12-1-2, 10-9-3-4. The trick is also the split can be horizontal, not just pie-shaped.

# Marble Weighing Problem & 90 Coin Problem (1.6)

Q: One marble heavier than the other and law-style weighing scale. 3 times max use. Question extends to larger numbers (e.g 12 instead of 9), then splits are different. 
A: The trick is to realize the weights on either side are conserved. Then it's just binary search: 4-4-4, then 2-2, then 1-1.

Q: In this variant, there are 90 coins with 1 heavy coin inside, and you are asked to find the minimum number of scale use cases. 30-30-30, 10,10,10, 5,5,5, 2,2,2.

# Defective Ball Problem (Zhou) (Harder Marbles)

Q: Marble weighing with one marble heavier OR lighter than the other (defective ball qn, Green book). How to do it in 3 weights? (This is very difficult, many branch out cases)
A: 

# Coincident Clock Hands Problem (1.13)

Q: What is the first time after 3pm when the hour and minute hands of a clock are exactly on top of each other?
A:  This is a conservation question. The conserved quantity is the angle. When the minute hand catches up with hour at marker $n$, the hour hand would have moved $\theta(n)$ degrees. We know minute hand goes at $12 \cdot \theta(n)$. And has covered $30n + \theta(n)$. (E.g at $n=3$, $30n=90 \deg$). So we have $30n + \theta(n)= 12\theta(n)$ and $\theta(n)=30n/11$. Substitute $n=3$ to get 90/11 degrees.

So, the hands are coincident at 90 degrees (3pm) + 90/11 degrees. 1 minute is 6 degrees, so 90/11/6=15/11m. So the hands are coincident at 3.15 + 15/11m = 3.16 and 4/11s of a minute.

# Symmetry Questions

For symmetry questions, there is some symmetric/complement aspect that can be deduced from one aspect of the question that reduces computation.

# Coin Piles Question 

Q: You are blindfolded in room. There are 1000 coins on floor. 980 are tails up and 20 are heads up. You can turn over (flip) coins. How to separate coins into two piles with equal number of heads?
A: Take 20 (number of heads) random coins and flip them. This special 20 have same number as heads as the remaining coins. Why? For any $n$ coin pile with $m$ heads and $n-m$ tails, the remaining pile has $20-m$ heads. So, we need to have $n-m=20-m$ and $n=20$ solves it. So we pick up $n=20$ coins, flip them, and this makes $20-m=20-m$. 

# Mislabelled Bags Question

Q: You have 3 bags of fruit. One bag is all orange, one bag is all apple, one bag is mixed. The labels on bag are all mislabelled. How to identify bags with minimum number of fruits taken out?
A: Take out a fruit from the labelled mixed bag. If apple, the mixed labelled bag is apples and likewise if orange. If apples, the apple labelled bag must be orange and orange labelled bag must be mixed.

# Wise Men Question

Q: 50 wise men and sultan. There is lightbulb with a switch in a room. Every minute, sultan calls a wise man to come in. He can turn on or do nothing. These men are called one at a time infinitely. When one of the men called states correctly to the Sultan that all men have been called at least once, everyone goes free. If not, all die. The men are allowed to communicate together once, before being put into separate rooms. How?
A: Have a designated spokesman who will speak for everyone who has been called. The other 49 will go in, switch on if off , and do nothing if it is off OR he has been called once. The spokesman will turn it off each time it is on. Once he turns it on 49 times, all wise men have been called.