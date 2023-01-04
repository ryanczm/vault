Type: #atom 
Atom: [[String Qns (D)]]
Subtopic: Fundamentals
Topic: Computer Science
Status: #inprogress
Understanding: #Exploratory 

----
## Time Conversion - 12H to 24H String (HR)

Q: Given a string of time in AM/PM format `hh:mm:ssAM` convert to `hh:mm:ss`.
A: The trick is that only the `hh` and `AM/PM` part of the string must be addressed. If `AM`, then the time is identical in 24H except for `12AM` being replaced by `00`. If `PM`, then we must add `12` to the hour component except when it is `12PM`.
T: String slicing and concatenation.

## [!] Camel Case 4 - String to Camel Case (HR)

Q: Complex question.
A: [Camel Case 4 Solution](https://programs.programmingoneonone.com/2022/05/hackerrank-camel-case-4-problem-solution.html).

## Determine Pangram (HR)

Q: Given a string of alphabets, determine if it is a pangram (contains all 26 letters of the alphabet).
A: Simply remove whitespaces via `.replace(" "."")`, then `.lower()`, then hash the string. If the length of the set is 26, it is a pangram.

## Valid Palindrome  

Q: Given a string, test if it is a palindrome. [Solution](https://leetcode.com/problems/valid-palindrome/solutions/39982/python-in-place-two-pointer-solution/?orderBy=hot).
A: We can either use **two pointer solution** or **reconstruct cleaned string then check if it is equal the reversal**.

## Valid Anagram 

Q: Given two strings, check if they are anagrams of each other (a permutation)
A: **Sort the two strings** and check if they are equal - `sorted(s) == sorted(t)`.

## Case Sensitive Longest Palindrome in String 

Q: Given string, find len of longest palindrome that can be built from those letters (can rearrange). [Solution](https://leetcode.com/problems/longest-palindrome/solutions/89614/python-simple-set-solution/?orderBy=most_votes)
A: There are even and odd palindromes. Hash (set) the odd letters (create an empty set. Iterate through the letters. If the letter is not in hash, add it, else, remove it - this leaves only odd letters). If there are no odd letters, palindrome is length of string. If there are odd letters, palindrome is length of even letters + 1.

## Longest Common Prefix

Q: Write a function to find the longest common prefix string (e.g `fl` for `[flower, flood]`) amongst an array of strings.
A: The trick is to find the max and min of the array of strings. This implicitly sorts comparing the first alphabetical value of each character in each string, then second, then third etc. So we only need to compare the min and max because these are the most different. Then we iterate through min, if it doesn't match, the l.c.p is the substring up to that mismatched index.

