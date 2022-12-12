Type: #atom
Atom: [[Probability & Stats Qns (C)]]
Topic: Quant 
Status: #inprogress
Level: #Exploratory 

----
# Overview 

Combinatorics questions are often solved by applying binomial coefficient to find the number of possible subgroups from a group.

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

