Type: #atom 
Atom: [[String Qns (D)]]
Subtopic: Fundamentals
Topic: Computer Science
Status: #inprogress
Understanding: #Exploratory 

----
## Longest Substring without Repeating Characters

Q: Given a string, find longest substring without repeating characters - e.g `bbbb -> b, abbc -> ab | bc`
A: Use sliding window technique. Have a dictionary to store the index of the visited character, then expand the window rightwards. Every time you see an already encountered character, set the left edge of the window to just after the first encountered character, to prevent duplicates. [Solution](https://leetcode.com/problems/longest-substring-without-repeating-characters/solutions/1731/a-python-solution-85ms-o-n/?orderBy=most_votes)

## String to Integer 

Q: Implement the myAtoi(s) function, converts a string to a 32 bit signed integer. Some specifications and rules follow.
A: Set up some variables, `MIN`, `MAX`, `n`, `empty` (flag), `sign`. If empty is true: iterate through each character in string, performing some logic, then set empty flag to false. Then, multiply n by 10 and add the current digit (simulate base 10 increasing). [Solution](https://leetcode.com/problems/string-to-integer-atoi/)

## Longest Palindromic Substring

Q: Given a string, return longest palindromic substring.
A: Use Manacher's algorithm. [Solution](https://leetcode.com/problems/longest-palindromic-substring/solutions/3337/manacher-algorithm-in-python-o-n/?orderBy=most_votes).

