- Discrete Mathematics Playlist:
	- [Tending to Infinity](https://www.youtube.com/watch?v=1tf2uKbM4rA&list=PLn3Wz38keZOfEEJmNHNBlnHoepR8wv8gU)
	- [PYQ](https://www.makaut.com/papers/btech-pcc-cse-4-sem-discrete-mathematics-pcc-cs401-2023.pdf)

### Bipartite Graph
2 sets of edges X and Y in the same graph.
X $\cap$ Y = $\emptyset$
### Complete Bipartite Graph
A bipartite graph in which every vertex of one set is connected to every vertex of another set.
### Sub Graph
Any subset of a graph is called a sub graph. 
Ex: {a -> b -> c -> d -> e} them {c-> d} is a subgraph or {c } is a subgraph
### Decomposition of a Graph:
A graph (G) is said to be decomposed into two sub-graphs G1 and G2 if G1 $\cap$ G2 is $\emptyset$
### Complement of A graph:
The complement of a graph is defined as a simple graph with the same vertex set as G and where tow vertices U and V are adjacent only when they are not adjacent in G. 
### Planar Graph:
A graph which can be drawn in the plane, so that it's edges do not cross each other is called a Planar Graph.
**Edges can be represented as curves, so to turn a graph into planar, we can represent required edge as a curve.**

#representation #graph 
### Adjacency Matrix of a Graph:
#adjacency-matrix
![adj matrix](https://media.geeksforgeeks.org/wp-content/uploads/20230727130331/Undirected_to_Adjacency_matrix.png)

#### General Representation:
A = ((a$_i$ $_j$)) is the adjacency matrix of a Graph G.

A =
   v1      v2      v3
v1 [a11, a12, a13]
v2 [a21, a22, a23]
v3 [a31, a32, a33]

a$_{ij}$ is one if the i$^{th}$ and j${th}$ vertices are connected by an edge.

### Properties of Adjacency Matrix:
- Adjacency matrix is always a square matrix iff the graph is undirected.
- Adjacency matrix always a symmetric matrix, i.e. A$^T$ = A

## Incidence Matrix:

Let G, be a graph with m vertices and n edges. Let the matrix, M = ((m$_{ij}$)) = m$\times$n.
- m$_{ij}$ = 1 if e$_{j}$ is incident to V$_i$
- m$_{ij}$ = 2 if V$_{i}$  has self loop as e$_{j}$
- 0 if e$_{j}$ is not incident to v$_{i}$
- This is only a square matrix when the number of vertices is equal to the number of edges.

  e1  e2  e3  e4
v1  1    0    0    0
v2  0    1    1     0
v3  0    0    0    1
v4  0     1    0    1

![incedence matrix](https://www.electrical4u.com/wp-content/uploads/What-is-Incidence-Matrix.png?ezimgfmt=rs%3Adevice%2Frscb38-1)
