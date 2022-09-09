---
title: Floyd-Warshall Algorithm
date: 
thumbnail: images/portfolio/Fl_w_algo.gif
service: Floyd-Warshall Algorithm Implementation
solution: I learned to implement this algorithm in Python and understood the time and space complexity to run the algorithm on any weighted graph.
---

#### What is Floyd-Warshall Algorithm? 🔥🔥

The Floyd-Warshall algorithm is a shortest path algorithm for graphs. It computes the shortest distances between every pair of vertices in the input graph in other words this algorithms finds the transitive closure of the relation _R_ on to the set _S_.


The Floyd-Warshall algorithm is an example of dynamic programming. It breaks the problem down into smaller subproblems, then combines the answers to those subproblems to solve the big, initial problem.



#### Usages 🌟

* Floyd Warshall Algorithm helps to find the inversion of real matrices.
* It helps in testing whether the undirected graph is bipartite.
* It helps to find the shortest path in a directed graph.
* Different versions of the Floyd Warshall algorithm help to find the transitive closure of a directed graph.
* This algorithm helps to find the regular expression the are accepted by finite automata.

#### Time and Space Complexity Analysis 🧐

**Time Complexity** ⏰ : _O(n^3)_
**Space Complexity** 📁 : _O(n^2)_


#### How it works ? 🤔

At the heart of Floyd-Warshall is this function:
 **ShortestPath(i,j,k)**.

This function returns the shortest path from _A_ to _C_ using the vertices from _1_ to _k_ in the graph. The vertices are individually numbered _1,2,...,k_.

There is a base case and a recursive case. The base case is that the shortest path is simply the weight of the edge connecting _A_ and _C_

**ShortestPath(i, j, 0) = weight(i, j)**.


The recursive case will take advantage of the **dynamic programming** nature of this problem. There are two possible answers for this function. Either the shortest path between _i_ and _j_ is the shortest known path, or it is the shortest known path from _i_ to some vertex (let's call it _z_) plus the shortest known path from _z_ to _j_ :

**ShortestPath (i, j, k) = min(ShortestPath(i, j, k-1), ShortestPath(i, k, k-1) + ShortestPath(k, j, k-1))**.

Basically, what this function setup is asking this: "Is the vertex _k_ an intermediate of our shortest path (any vertex in the path besides the first or the last)?"

If _k_ is not an intermediate vertex, then the shortest path from _i_ to _j_ using the vertices in  _{1,2,...,k−1}_ is also the shortest path using the vertices in _{1,2,...,k}_.

If _k_ is an intermediate vertex, then the path can be broken down into two paths, each of which uses the vertices in _{1,2,...,k−1}_ to make a path that uses all vertices in _{1,2,...,k}_. That is because the vertex _k_ is the middle point.





Now, It is time explore the written program 😻.




##### Please visit the GitHub repository 
### [GitHub Link ](https://github.com/ronakjpatel/Algorithms-and-Analysis/blob/main/Floyd_Warshall_Algo.ipynb)
