Type: #atom
Atom: [[Quantitative & Logic Qns (CZ]]
Topic: Quant
Level: #Exploratory 

----
# Pure Logic Questions

These involve less complex numerical simulation and more generic simulation.

# Bridge (River) Crossing Question
Q: See https://en.wikipedia.org/wiki/Bridge_and_torch_problem
A: The fastest 2 cross. The fastest returns. The slowest 2 cross. The second fastest returns. Both fastest cross. Begins and ends the same way.

# Birthday Question [!]

# Defective Ball Question [!]

Q: *See Conservation Qns (C)*. This is a more difficult variant of marbles.

# Horse Race

Q: This is an interesting variant of the marbles problem. 25 horses of diff speed. 5 lane race track (5 horses per round). How many times to race to identifty top 3 fastest horsies? You can't time the race, you can only check relative, within-group speed orderings.

A: Bucket into groups of 5 (a,b,c,d,e) and race. This gives within-group orderings. By edge case, if fastest 3 are in one bucket, we can eliminate the slowest 2 from each group. So we have 3 x 5 left.  

Then, race fastest horse from each group of 5. This lets us know H1 (fastest), then label the groups a,b,c,d,e, based on the top horse speed ranking within groups. Then, race a2, a3, b1, b2, c1. In total you use the track 3 times (initial, inter-group, final).

# Door to Offer Question 

Q: Facing two doors. One door leads to offer, one door leads to exit. Two guards, 1 per door. One guard lies, other guard tells truth. You want the job offer. You can only ask a single question to 1 guard. What to ask?
A: The trick is to involve both guards in the question - 'Would the other guard say that you are guarding the door to the offer?'. If 'no', it is current door, if 'yes', it is other door. 

# Message Delivery Lockbox Question

Q: A wants to send message in padlock box to B via messenger service. Service is not secure - anything inside unlocked box is lost. A and B have own padlock and key. (E.g B cannot open A padlock because his key is for his own padlock). How to send?
A: The key is to send the box multiple times. First, A locks box with his lock A and send. B receives, adds his own lock B. Sends back. A receives, unlocks his lock, sends back. B receives, unlocks his lock.

# Light Switches

Q: 1 lightbulb in closed room, 4 switches outside set to off. Only one switch controls the bulb. How many times you need to go into room to figure out which switch controls it?
A: You only need to go into room one time. Turn on 1 & 2, wait, come back,turn off 2 and turn on 3, dash into room and observe. If ON and HOT, 1 controls. If OFF and HOT, 2 controls. If ON and COLD, 3 controls. If OFF and COLD, 4 controls. Key idea is that a lightbulb can be hot and off means it was turned on for a while but turned off just before you observe it.

# Quant Salary

Q: 8 people with diff salaries want to know average salary of group without directly revealing their own. How?
A: First quant takes random number, adds salary to it, gives to second. Second adds salary, gives third. Repeat. Last guy tells first guy the sum. First guy removes the random number and averages.

# Burning Ropes Question

Q: Measure 45m with two ropes. A rope takes 1hr to burn if 1 end is lit.
A: Have to assume burning both ends cuts remaining time by half. So light one end of 1 rope and burn both ends of 1 rope > 30m After that, burn remaining end.

# Counterfeit Coins I 

Q: 10 bags of 100 identical coins each bag. In all bags but one, each coin weighs 10g. In counterfeit bag, all coins weigh either 9 or 11g. Using one single weigh of a digital scale, identify fake bag.
A: Take 1 coin from first bag, 2 from second, ... 10 from tenth bag. You have 55 coins. Weigh. If no counterfeit they should be 550g. The $i$ bag is counterfeit, so weight will be $550 \pm i$. 

# Glass Balls

Q: You are holding two glass balls in a 100 story building. If ball is thrown out of window, it will not break if floor is less than X but break if floor is equal or greater to X?
A: This is tricky. We suppose a strategy with $N$ throws. We throw first ball from $N^{th}$ floor, if it breaks, we start from 1 to N upwards and test the second ball. If it doesn't break, we go up by $N-1$ floors and repeat. The number of floors this lets us cover is $N+(N-1) + \cdots + 1=N(N+1)/2 \geq 100$ and so $N=14$.

# Lightbulbs & Switches Qn (1.28)

Q: Similar to Green book's lightbulb question, but with 3 lightbulbs instead of 4.
A: Same answer

# Blue and Red Hats Qn (1.29)

Q: 3 men. 1 blind. Dark closet with 3B 2R hats. Can only see others hat. Guy 1 draws hat. Guy 2 draws hat. 1 & 2 say I cannot know what color my hat is. Blind 3 guy and goes 'I know what color my hat is'. What color?
A:  1B 2B 3R (blind). 

# Cheating Husbands and the Oracle (1.40)


# Monty Hall Door Problem (4.20/4.21)

Q: You face 3 doors, with a prize behind 1 door. The host lets you choose a door to open. He then will open an empty door instead of the door you chose. He then gives you the option to choose the remaining door that is not open, or stick to your original choice. Should you switch? You choose D3. He opens D2, it is empty. The prize is either behind D3 or D1. Should you switch to D1 or open D3?
A: You should switch. If you don't you have $1/2$ chance of right door. You win the prize if your first choice is an empty door, then do a switch. You have $2/3$ chance of picking an empty door. So you should always switch.

Q: Now instead of the host picking an empty door, a member of audience randomly picks one of the 2 remaining doors. It is empty. Do you still switch to the remaining door?
A: Assuming the audience member has no knowledge, then it is 50-50, in that case, we are indifferent to switching.
