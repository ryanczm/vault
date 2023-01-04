Type: #atom 
Atom: [[DFS Qns (D)]]
Status: #inprogress 
Understanding: #Exploratory 
Distribution: 20 (1E, 14M, 5H)

----
# Flood Fill (HR)

Q: Given a 2D array (grid of pixels) of integer values, a starting pixel, and a target color, perform flood fill. This involves converting the starting pixel to the target color (replacing an integer value), then recursively doing so  4-directionally, if the adjacent pixels are the same color as the starting pixel. [Solution](https://leetcode.com/problems/flood-fill/solutions/109604/easy-python-dfs-no-need-for-visited/?orderBy=most_votes)
A: We need to define a DFS takes in two coordinates. It first checks conditions - are coordinates within the bounds (lengths of array) and is the input coordinate pixel same as the starting pixel color? If yes, perform DFS on the NSEW neighbours. Then, outside the body, if the starting pixel is not the same color as the target, call `dfs(sr, sc)`.

# 01 Matrix (HR)

Q: Given a 2D array of a binary matrix, return the (Manhattan) distance of the nearest 0 for each nonzero cell. This involves a **queue**.

# Clone Graph (HR)

Q: Given a reference of a node in a connected undirected graph as an adjacency list, return a deep copy of the graph. 

# Course Schedule (HR)

Q: Given an array of lists of `[course, prereq]`, check if you can finish all courses. This involves **detecting a cycle with DFS**. 