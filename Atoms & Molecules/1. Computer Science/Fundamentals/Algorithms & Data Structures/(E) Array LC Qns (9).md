Type: #atom 
Atom: [[Array Qns (D)]]
Subtopic: Fundamentals
Topic: Computer Science
Status: #inprogress 
Understanding: #Exploratory 

----
# Divisible Sum Pairs (HR)

Q: Given an array, find the number of pairs inside that are divisible by some common divisor $k$.
A: We need to use a nested for loop with `enumerate` - first to set the target, then to iterate through all elements to the right of target, then if the output of their sum mod k is 0, increment the counter. 

# Sparse Arrays - Count Occurences of Queries in String (HR)

Q: Given an array of strings and queries, find and return the number of occurences of queries in the strings, in an array of integers the shape of queries.
A: Create an empty array of 0s, do a nested for loop. The outer loop produces an index. The inner loop iterates over the target array and checks if the query value at that index is the same as the string, then increments the empty array at that index.

# Grading Students  (HR)

Q: Given an array of grades, convert it to an array of grades with the correct specifications (e.g rounding, failure) - this is mentioned in the question. Very tedious. If grade is less than 38, no rouding occurs. Grades are rounded to the next multiple of 5 if the difference is less than 3.
A: Create an empty array. Iterate through the grades array, if it is less than 38, calculate remainder mod 5. If the remainder is greater than 3, round up via adding 5-remainder - [Solution](https://www.hackerrank.com/rest/contests/master/challenges/three-month-preparation-kit-grading/hackers/ayush18012002/download_solution)

# Diagonal Difference (HR)

Q: Given a square matrix 2D array, calculate the absolute difference between the sums of its diagonals
A: We need two variables to store the diagonal sum and a final variable to calculate absolute difference. We can use a for loop to iterate across the diagonals, adding the result cumulatively - [Solution](https://www.hackerrank.com/rest/contests/master/challenges/three-month-preparation-kit-diagonal-difference/hackers/dayeneew/download_solution)

# Counting Sort (HR)

Q: Implement the first few steps of counting sort by creating a frequency array. This is an unstable sorting algorithm that is used when the range is small (e.g 1-10).

1. Create array of zeros.
2. Iterate through target array, increment zero array at corresponding index.

# Counting Valleys (HR)

Q: Given an array of up or down steps, find num. valleys (1 or more down steps below sea. [Solution](https://shounaklohokare.medium.com/counting-valleys-hackerrank-solution-in-python-ccd342931e91).
 
1. Initialize two variables to 0 for the level and the valley count.
2. Iterate through the array. If up, add to levels. Within this, if levels is 0, add a valley.
3. If down, subtract a level.

# Permuting Two Arrays s.t Elementwise Sum > K (HR)

Q: Given two arrays, permute them such that thesum of their $i^{th}$ elements is greater than some constant for increasing $i$ till a certain point.

1. Sort both arrays. One in ascending and other in reverse.
2. Iterate through both arrays, checking sum condition. 

# Subarray Division 2 (Lily & Ron Chocolate Bar Sharing) (HR)

Q: How many ways (discrete segments) can an array of integers be divided into s.t the length of the subarray equals some constant $m$ and the sum of the subarray equals some constant $d$?.

1. Set a counter for the answer
2. Iterate through the `range(n-m+1)`. If `sum(s[i:i+m])==d: ans+=1`.