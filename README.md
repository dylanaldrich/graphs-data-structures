# graphs-data-structures
Short intro to graphs

## What is a graph? 

A **graph** is a collection of nodes which stores data and edges which represent relationships or connection between nodes. Unlike other relationships between nodes, graphs do not simply have parent / child relationships. Instead, they are defined as **directed**, which is to say, one node leads to another, and **undirected**, a mutual connection between the nodes. Graphs are represented in code in two different ways: via an **adjacency list**, where there is a collection of arrays for each node, and an **adjacency matrix**, which is represented by a two-dimensional array (adjacency lists being the more commonly used example). 

A graph is an ordered pair G = (V,E) comprising a set of vertices or nodes, and a collection of pairs of vertices from V, which are called "edges" of the graph.

V = { 1, 2, 3, 4, 5, 6 }
E = { (1, 4), (1, 6), (2, 6), (4, 5), (5, 6) }


### How are graphs used in programming?


### Examples of graph implementation
Google Maps: locations on a map, starting/end point - can be directed or undirected
Facebook: friends (undirected graph), likes (directed)

### Dijkstra's algorithm
Created by Edsger in order to find the shortest path between nodes on a graph.

Big O: O(e + v(log)v)
Where v = number of nodes (vertices)
And e = number of edges (paths between vertices)


### Breadth-First Search
Breadth-first search (BFS) is a method for exploring a tree or graph. In a BFS, you first explore all the nodes one step away, then all the nodes two steps away, etc.

Breadth-first search is like throwing a stone in the center of a pond. The nodes you explore "ripple out" from the starting point.

Starting with the root, a BFS traverses a tree by first visiting all immediate children (all the nodes that are one step away from the starting node), then move to those nodes' children (i.e. now we're two steps away from the original node), and so on.

Advantages: 
A BFS will find the shortest path between the starting point and any other reachable node. A depth-first search will not necessarily find the shortest path.

Disadvantages:
A BFS on a binary tree generally requires more memory than a DFS.


### Depth-First Search
Depth-first search (DFS) is a method for exploring a tree or graph. In a DFS, you go as deep as possible down one path before backing up and trying a different one.

Depth-first search is like walking through a corn maze. You explore one path, hit a dead end, and go back and try a different one.

Advantages:
Depth-first search on a binary tree generally requires less memory than breadth-first.
Depth-first search can be easily implemented with recursion.

Disadvantages:
A DFS doesn't necessarily find the shortest path to a node, while breadth-first search does.


### Possible interview questions related to graphs
1. Is there a path between two nodes in this undirected graph? Run DFS or BFS from one node and see if you reach the other one.

2. What's the shortest path between two nodes in this undirected, unweighted graph? Run BFS from one node and backtrack once you reach the second. Note: BFS always finds the shortest path, assuming the graph is undirected and unweighted. DFS does not always find the shortest path.

3. Can this undirected graph be colored with two colors? Run BFS, assigning colors as nodes are visited. Abort if we ever try to assign a node a color different from the one it was assigned earlier.

4. Does this undirected graph have a cycle? Run BFS, keeping track of the number of times we're visiting each node. If we ever visit a node twice, then we have a cycle.

### Resources
https://www.interviewcake.com/concept/java/graph
https://medium.com/techie-delight/graph-data-structure-interview-questions-and-practice-problems-22d5cd488855
https://www.cs.usfca.edu/~galles/visualization/BFS.h
https://www.cs.usfca.edu/~galles/visualization/DFS.html
https://www.geeksforgeeks.org/graph-data-structure-and-algorithms/
https://www.interviewcake.com/question/python/balanced-binary-tree
https://en.wikipedia.org/wiki/Dijkstra%27s_algorithm