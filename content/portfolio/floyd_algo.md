---
title: Floyd-Warshall Algorithm
date: 
thumbnail: images/portfolio/fw_Graph.jpg
service: Floyd-Warshall Algorithm Implementation
---

#### What is Floyd-Warshall Algorithm? 🔥🔥

The Floyd-Warshall algorithm is a shortest path algorithm for graphs. It computes the shortest distances between every pair of vertices in the input graph.


The Floyd-Warshall algorithm is an example of dynamic programming. It breaks the problem down into smaller subproblems, then combines the answers to those subproblems to solve the big, initial problem. The idea is this: either the quickest path from A to C is the quickest path found so far from A to C, or it's the quickest path from A to B plus the quickest path from B to C.



#### Usages 🌟

* Floyd Warshall Algorithm helps to find the inversion of real matrices.
* It helps in testing whether the undirected graph is bipartite.
* It helps to find the shortest path in a directed graph.
* Different versions of the Floyd Warshall algorithm help to find the transitive closure of a directed graph.
* This algorithm helps to find the regular expression the are accepted by finite automata.

#### Time and Space Complexity Analysis 🧐

**Time Complexity** ⏰ : $O(n^3)$
**Space Complexity** 📁 : $O(n^2)$


#### How it works ? 🤔

At the heart of Floyd-Warshall is this function:
$ ShortestPath(i,j,k) $.

This function returns the shortest path from $ A $ to $ C $ using the vertices from 1 to $ k $ in the graph. The vertices are individually numbered $ 1,2,...,k $.

There is a base case and a recursive case. The base case is that the shortest path is simply the weight of the edge connecting $ A $ and $ C $

$ ShortestPath(i, j, 0) = weight(i, j). $


The recursive case will take advantage of the **dynamic programming** nature of this problem. There are two possible answers for this function. Either the shortest path between $ i $ and $ j $ is the shortest known path, or it is the shortest known path from $ i $ to some vertex (let's call it $ z $) plus the shortest known path from $ z $ to $ j $ :

$ ShortestPath (i, j, k) = min(ShortestPath(i, j, k-1), ShortestPath(i, k, k-1) + ShortestPath(k, j, k-1)) $.

Basically, what this function setup is asking this: "Is the vertex $ k $ an intermediate of our shortest path (any vertex in the path besides the first or the last)?"

If $ k $ is not an intermediate vertex, then the shortest path from $ i $ to $ j $ using the vertices in $ {1,2,...,k−1} $ is also the shortest path using the vertices in $ {1,2,...,k} $.

If $ k $ is an intermediate vertex, then the path can be broken down into two paths, each of which uses the vertices in $ {1,2,...,k−1} $ to make a path that uses all vertices in $ {1,2,...,k} $. That is because the vertex $k$ is the middle point.





Now, It is time explore the written program 😻.




##### Please visit the GitHub repository 
### [GitHub Link ](https://github.com/ronakjpatel/Algorithms-and-Analysis/blob/main/Floyd_Warshall_Algo.ipynb)
