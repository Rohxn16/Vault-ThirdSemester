#theorems #graph 
### Handshaking Theorem:
Handshaking theorem: The sum of the degrees of the vertices of a graph G is twice the number of edges in it. 

### Path or Reachability Matrix
#representation 
For a simple directed Graph, G, with n vertices, then the path matrix P will be defined as,
P = (($P_{i,j}$))$_{mxn}$ and $P_{i,j}$ = 1 for all non 0 elements of B$_m$ matrix and 0 for all 0 elements of B$_m$ . Where B$_m$ = A + A$^2$ + .... A$^m$, where A is #adjacency-matrix .

![pathmatrix](https://img.brainkart.com/imagebk7/ZQBpoqo.jpg)
### Isomorphism of A graph:
Two graphs G1 and G2 are said to be isomorphic, if:
1. The number of vertices are same.
2. The number of edges are same.
3. Sequence of degrees of vertices are same.
4. Vertices and Edges correspondence will be preserved.

![isomorphic-graph](https://i.sstatic.net/yTCwu.jpg)

### Graph Coloring:
Chromatic number of a graph: The least number of colors required for coloring vertices of a graph G, such that, no two adjacent vertices have the same color is called the chromatic number of a graph.

- The chromatic number of a graph G will be denoted by $\chi$ (G).
- If $\chi$ (G) = k, then the graph is called k chromatic number.
- Chromatic number of null graph is one.
- Chromatic number of a complete graph is n, where n is the number of vertices.
- If a graph is a circuit, with n vertices, it is:
	1. Two chromatic if n is even.
	2. Three chromatic if n is odd.