Type: #atom
Atom: [[Probability & Stats Qns (CZ)]]
Topic: Quant 
Level: #Exploratory 

----
# Overview 

Combinatorics questions are often solved by applying binomial coefficient to find the number of possible subgroups from a group.

# Poker Hands

Q: You have a standard deck (13 x 4 sets). A hand is 5 cards. What is probability of 4-of-a-kind (AAAAD), full house (AAADD), two pairs (AABBD), where D is a different and A and B are same. Note same means same number, not suits. Somehow color is disregarded (?).
A: 
Hands with 4-of-a-kind - 13 choices for first 4 and 48 choices for remaining so $13\cdot 48=624$.
Hands with full house - 13 choices for the first 3 and $\binom{4}{3}$ suits, and 12 for the pair and $\binom{4}{2}$, so we have $13 \cdot B(4,3) \cdot 12 \cdot B(4,2)=3744$
Hands with two pairs - $\binom{13}{2} \cdot \binom{4}{2} \cdot \binom{4}{2} \cdot 44=123552$. 13C2 is choosing values of 2 pairs, 4C2 twice is for the suits of the pairs, and 44 is the remaining choice (52 - 4 - 4).
Divide these combinations by $B(52,5)$ - the number of distinct hands.

# Hopping Rabbit

Q: A rabbit can climb up a flight of $n$ stairs with a hop of 2 stairs at a time or 1 stair. How many ways can he do it?
A: This is a recurrence relation that is related to a Fibonacci sequence: $S(n)=S(n-1)+S(n-2)$. The number of ways to climb of $n$ stairs is the sum of ways to climb up $n-1$ stairs and $n-2$ stairs. Why? At the end, you either climb up with a 1-hop or 2-hop. Clearly, $S(1)=1$. $S(2)=2$. Just keep going. 

# Screwy Pirates 2

Q: There are 11 pirates left from Screwy Pirates 1. These guys put their loot in a special safe, only $\geq 6$ pirates can open it.  So $5$ pirates cannot but $6$ can. So they ask locksmith to put locks on safe. One lock can be opened by multiple keys but not the other way round. Pirates can carry more than 1 key.
A: I can't quite get the logic but I'll just memorize it. For each randomly selected group of 5, there must be some special lock the other 6 have (so 5 cannot open, but 5+1 can). This is $B(11,5)=11!/(5!/6!)=462$ locks. For each lock, there are 6 keys (why?). So each pirate must have $462\cdot 6/11=252$ keys.

# Chess Tournament [!]

# Application Letters (Inclusion Exclusion) - Montmort's Matching Problem [!]

Q: There are 5 cover letters to be put in 5 labelled envelopes. If we randomly put cover letters into envelopes, what is the probability all cover letters are put in the wrong envelope?
A: This is the complement of the probability at least one cover letter is in the right envelope. This is the union of events that letter $i$ has the correct envelope: $P(\bigcup_i^5 e_i)$. We can apply inclusion exclusion to get our answer. For example, $P(e_i, e_2)=1/5 \cdot 1/4$ and there are $B(5,2)$ ways to select 2 elements. The final answer is $$1-(1-1/2!+1/3!+1/4!+1/5!)=11/30$$
This question can also be done with derangements (this is the probability of a derangement).

# 100th Digit (Binomial Theorem) [!]

# Cubic of Integer (Binomial Theorem) [!]

# Guests & Room Allocation Qn (1.34)

Q: $N$ people are allocated $N$ rooms for convention. However, all are drunk so doorman allocates at random. Probability that at least one guest ends up in room which he was originally assigned?
A: This uses [derangements](https://math.stackexchange.com/questions/3060725/probability-question-a-large-number-n-people-go-to-a-convention-at-a-hote). The formula is $$!n=n!\sum_{i=0}^{n}\frac{(-1)^i}{i!}$$ and answer is $\frac{!n}{n!}=e^{-1}=0.367...$ for the complement case (no guest ends up in his originally assigned room).

# Handshakes at Party Qn (1.35)

Q: At a party, everyone shakes hands with everyone else. If there are 66 handshakes, how many people are at party?
A: This is actually a number of parameters in the covariance matrix question. If there are $N$ people, the covariance matrix is $N \times N$. Now handshakes are symmetric and we can't shake our own hand, so the diagonal + half is crossed out. The formula is $N(N-1)/2=66$ where $N=12$. Alternatively, this is simply $\binom{N}{2}=66$. 

# Distinct Birthdays & Birthday Problem (Blitzstein 4.4.5)

Q: This question is from Blitzstein 4.4.5. In a room witn $n$ people, what is the expected number of distinct birthdays amongst them?
A: **Complements:** p(j day is represented) = 1 - p(no one born on day j), then we take **expectation** (365 days).$$365(1-(\frac{364}{365})^n)$$
# Expected Number of Pairs of People with same Birthday Qn (1.36)

Q: Same party with 25 people, expected number of pairs of people with same birthday?
A: The probability of match success is 1/365 (assuming birthday's are i.i.d and uniform) - given one person's birthday, the probability of a match is simply 1/365. Then the answer is number of pairs $\binom{N}{2}/365$.

# Grid East - North Question (1.68):

Q: Consider a grid 5x5. You start at 0,0 and move to 5,5. You can only go up or right along grid. How many paths are there?
A: The trick is to realize you must take 10 steps (5x2) no matter what path. Then, how many combinations of selecting 5 right steps from 10 total (symmetric). Answer is $\binom{10}{5}=252$.

# Investing 20000 into 5 Funds | Stars & Bars Qn (4.37)

Q: How many different ways can you invest 20000 into five funds in increments of 1000? E.g $(0, 4000, 1000, 2000, 13000)$.
A: We use a 'stars and bars' method. Essentially, you insert 4 bars into 20 stars (1k incremenets). The number of ways you can insert the bars is the answer to the question. Thus, it is $\binom{24}{4}=\frac{24!}{4! 20!}=10626$ ways.

# Chocolate Chip Cookies & Dough Qn (4.38) [!]

Q: **Very tough question!** You are making choc chip cookies. You add $N$ chips to the dough. Then randomly split dough into 100 equal cookies. What value of $N$ ensures at least 90% of cookies have at least one chip?
A: This can be answered with the **inclusion-exclusion principl**e - used to calculate a union. If $p$ is the probability all cookies have >1 chip, then $1-p$ is the probability of event at least some cookies have no chips. This event is the union of each cookie having no chips: $1-p=p(\bigcup_{i=1}^{k}A_i)$.

# Probability of Difference of Highest and Lowest Numbers of 3 Fair D6 Rolls Qn (4.49)

Q: You are going to roll three fair dice. What is the probability that the difference between the highest and lowest numbers showing is exactly four?
A: There are $216 =(6^3)$ outcomes. We need $p([6,2] \cup [5,1])$. For the first case, our unordered outcomes are $226,236,246,256,266$. The first outcome is permuted 3 ways, the second, third, fourth 6 ways and last 3 ways. That gives us $1(3)+3(6)+1(3)=24$ ways. Do the same for the $5,1$ case.