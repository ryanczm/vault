Type: #atom
Atom: [[Dynamic Programming Qns (D)]]
Subtopic: Fundamentals
Topic: Computer Science
Status: #inprogress
Understanding: #Exploratory 

----
# Parallel Courses II

Q: [Parallel Courses II (Tanishq Choudhury)](https://leetcode.com/problems/parallel-courses-ii/solutions/1373540/detailed-explanations-diagrams-annotated-code/?orderBy=most_votes). We are supposed to find minimum number of semesters to cover all courses. The courses are a DAG as an adjacency list. Each semester, we can only take $k$ courses.

1. Define the `minNumberofSemesters(n, relations)` function:
2. (M) Construct a list for number of `in_degrees`, the number of total classes and number of classes to take each semester.
3. Construct the `graph` which is is an adjacency list.
4. Populate the `graph` and `in_degrees` objects from iterating through the `relations` object (1-indexing)
5. Call the recursion by returnin the `recurse(mask, in_degrees)` function called with arguments of a new bitmask and a tuple of `in_degrees`.
6. Define the `recurse(mask, in_degrees)` function.
7. (R) Define the base case (0 bit mask).
8. Construct the `nodes` object from a list comprehension and the constant `ans`.
9. Enumerate through each list of nodes the `combinations`, constructing a new mask and new in_degrees object for that combination iterate through each node in the combination by updating the new mask and in_degrees.
10. Create the `ans` object from the minimum of `ans` and `1+recurse(new_mask, tuple(new_in_degrees)`.
11. Return `ans`.