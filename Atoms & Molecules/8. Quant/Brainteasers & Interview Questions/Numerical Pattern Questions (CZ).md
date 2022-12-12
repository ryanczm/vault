Type: #atom
Atom: [[Logic Qns (C)]]
Topic: Quant 
Level: #Exploratory 

----
# Numerical Pattern Qns

The trick is to realize some numerical pattern that can be captured in a formula. The trick is low-dimensional numerical simulation, simply plug some (extreme, edge case) numbers in and notice a **pattern**, then extrapolate to general case. Try to think in terms of variables, e.g $n$ and $x$.

Variable-lize - Think in terms of variables.
Edge Cases - Plug in edge case numbers (at the extremes).
Low Dim Sim - Plug in for a simpler version of problem (problem simplification) to see a pattern.

# Mulilated Chessboard Question (Tiling Puzzle)

Q: You have 8x8 chessboard with two corner squares removed. Can you fit 31 2x1 bricks to cover chessboard?
A: First, decompose chessboard into 32B 32W. If two corner removed, then 30B 32W. Each brick must cover 1B 1W no matter orientation. So cannot fit (it implies a brick must cover 2W).

# Box Packing Question (3D Tiling Puzzle)

Q: Can you pack 53 bricks of dimensions 1x1x4 into a 6x6x6 box?
A: This is an extension of mutilated chessboard and has tricky logic.

First, 6x6x6 is 27 2x2x2 cubes. Imagine them to be 13B and 14W (or switch order). Then, each mini cube can fit 4 bricks. Each brick fits in a white cube and a black cube (end sticks out). So, for 13B and 13W, that is 13x4=52 bricks. The last brick, will fit 1/4 of the remaining cube.

# Calendar Cubes Question 

Q: You have 2 custom dice. Use two dice to display day of month. Must use both (e.g 09). What numbers to put on the dice faces?
A: 0,1,2 on both dice (11,22) and 0 because 1 dice cannot have 1-9. Then, we have 3 slots per dice left  (6 total). We need to assign 3,4,5,6,7,8,9 - 7 slots. Trick is to use 6 as 9 (upside down). 

# Last Ball Question

Q: A bag has 20B 14R balls. Each turn, randomly draw two balls out. Assume each ball has equal chance of being drawn. If different (1B, 1R), add 1R to bag. If same (BB or RR), add 1B to bag. If we keep drawing, what is color of last ball in bag?
A: Just simulate. The key is that for 1B1R and BB, it is a -1B with 2/3 chance and for RR is a -2R +1B with 1/3 chance. So per 3 draws, the expected value is -1B -2R. If we keep doing this, R balls goes to 0 (if even R at start) and 1 if odd. If R is odd at start, R is last. If R is even, B is last.

# Trailing Zeros Question

Q: How many trailing 0s in 100!
A: Trick is to realize factor pair (2x5) gives trailing 0. We know freq 2 >> freq 5 in prime number decomposition on all numbers in 100!, so freq 5 is limiting. From 1-100, 20 numbers are divisible by 5, and 4 amongst those are divisible by 5^2 (25, 50, 75, 100). So we have 20 + 4 (double count) = 24 trailing zeros.

# Card Game Question

Cards - A standard 52-card deck has 4 suites (club, diamond, hearts and spades). Each suite has numbers (2-9), court cards (Q, J, K), and ace, so 13 cards per suite. 2 suites are red, 2 suites are black.
Q - Dealer offers you game. Turn over 2 cards. If both R, dealer pile. If both B, your pile. If 1R 1B, discard. If you have more cards in pile at end of game, you win $100. What price should you pay for this game?
A - Trick question, you always finish with same number of cards.

# Macro Cube Problem (1.10)

Q: A 10x10x10 cube. The outermost layer falls off. How many cubes fell off?
A: The trick is to realize it is $10^3 - 8^3$. Each side of the inner cube is $8$.

# Boy-Girl Problem (1.9)

Q: 10000 families. Every year, they give birth once, and stop once boy. At year $t$, what percentage of children are boys?
A: The trick is to realize the ratios are constant throughout, each year.

# Lightbulb On-Off Qn (1.14)

Q: 100 lightbulbs in a row. 1st guy walks in, switches all. 2nd guy, switches 2,4,6 ... 3rd guy, switches 3,6,9 etc. After 100 people, what is state of bulb 64?
A: The trick is to realize only brokers that are factors of 64 will interact with the bulb. A bulb is off after even number of interactions and on after odd. 1, 2, 4, 8, 16, 32, 64 interact. This is odd, so bulb is on.

# Number of Lightbulbs On Qn (1.15) [!]

Q: Same as 1.14 but now, how many lightbulbs are on after 100 people walk through the row?
A: The trick is use *factor pairs*. 

# Sock Drawing Qn (1.16, 1.17, 1.18)

Q: Drawer has 8B and 11R socks. Minimum how many socks to draw out (without seeing color) s.t you have matching pair?
A: 3. 

Q: Generalize to $n$ different colors of 50 socks each.
A: N+1. Notice the pattern.

Q:  2 red, 4 yellow, 6 purple, 8 brown, 10 white, 12 green, 14 black, 16 blue, 18 gray, and 20 orange socks. Minimum number for 3 pairs?
A: 47 = 6 + 8 * 5 + 1. First draw the reds and yellows, then 5 sets of 8 distinct colors, then one last sock to match.

# Integer Shouting Game Qn (1.19)

Q: You and opponent call out integers in turn. First to 50 wins. First person calls from 1-10 inclusive, then next person must call out next number that is +1 to 10 greater than current.
A: Working backwards, at 39, opponent can do from 40-49, giving you a win. So working backwards, 39, 28, 17, 6. Then you start at 6. This is akin to plugging in (50-10-1-10-1-10-1-10-1).

# Coin Filling Game Question (1.54)

Q: You have table. Take turns to place coins on table (no overlap). Last person to fill space wins. What is strategy?
A: This is the visual analogue of the integer shouting game. Simply place a coin in the middle of the (radially symmetric) table, then mimic your opponent by placing your coin in the mirror image of his viewed through the central point.

# Safe Combination Qn (Rotating Dial Safe) (1.20)

Q: You have a safe with a dial from 0-40. The passcode is 3 numbers. You must rotate the dial to the right number, then reset to 0, then rotate dial, then reset, then rotate and reset to key in 3 numbers. Maximum number of combinations?
A: This is a trick Qn, answer is 40x40 + 1. Once you dial the first two correctly, you simply rotate the dial one clean rotation to trigger the correct number.

# Snail Climbing Pole Qn (1.25)

Q: Snail climbs 10m pole at 3m/day. At night it sleeps so goes down 1m. How long?
A: Trick question. At the start of the 5th day, it would have covered 8m. So it takes $4 \frac{2}{3}$ days, not $5$.

# Fly and Motorcyclists Qn (1.31)

Q: Two motorcyclists 25km apart, moving towards each other. First guy is 20kmh second is 30kmh. A fly on helmet of first motorcyclist will fly towards second at 40kmh. When it hits the second guys helmet it will reverse. How much distance would fly travel before collide?
A: The trick is in kinematics velocity is a vector so we can rearrange it. We can imagine first motorcyclist stationary while second rides towards him at 50km/h. This takes 0.5h. The fly is going 40km/h (absolute) so it will take 20km/h before collision. Notice if first guy is stationary then we can count total distance by fly.

# Marbles and Jar Blindfolded Draw Qn (4.22)

Q: You have 50W and 50B marbles and 2 empty jars. You are to put the marbles into the 2 jars, any way you want, then blindfolded and the jars rotated. You are allowed a blindfolded draw from a random jar with at most one marble. How do you arrange the marbles to **maximize or minimize the probability** of drawing a W marble?
A: Consider extreme and uniform distributions. The trick is to place 1W in 1 jar and the 99 in the other. This maximizes your probability of $3/4$ of drawing a white marble from the jar. To minimize, simply place 1B in 1 jar and 99 in the other.