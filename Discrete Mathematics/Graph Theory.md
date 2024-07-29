#graph
A **graph** G(V,E) is a structure consisting of a set of objects called **vertices** and another set of objects called **edges**.  An edge $e \in E$ is denoted in the form where e = {x,y}, where the vertices x,y $\in$ V. Two vertices x and y can be connected using an edge, e. Thus, the two joined vertices can be called adjacent vertices.

- A simple graph is one where there are no loops  and no two edges joining the same pair of vertices.( The graphs we consider are assumed to be simple unless stated otherwise).

# Categories of Graphs:

### Directed Graphs:
- Directed Acyclic Graph.
- Tree.
### Undirected Graphs:
- Connected : No unreachable nodes.
- Complete : All nodes are interconnected
- Bipartite connected or bi graph: The vertex sets are partitioned into two exact subsets and no two vertices pointing to each other lie in the same subset.
### Cyclic Graph:
A graph that consists of a single cycle, meaning it forms a closed loop. In a cycle graph, each vertex is connected to exactly two other vertices.
### Loop Graph:
A graph where a node is looped or linked to itself, i.e. both ends of a vertex are connected to the same graph is called loop graph.

## Terminologies:
- **Trivial Graph**: One vertex and one edge only
- **Null Graph**: No vertices and edges
- **Directed Graph**: A graph whose edges have direction.
- **Undirected** Graph: Opposite of directed.
- **Self loop**: When an edge is connected to itself is called a self looped edge.
- **Proper edge**: Edge with no self loop.
- **Multi edge**: 2 vertices connected by multiple edges is a multi edged graph.
- **Simple Graph:** No self loop, no multi edge.
- Multi-graph: No self loop but, multi edge.
- **Pseudo Graph**: Both self loop and a multi edge.
- **Incidence and Adjacency**: Two vertices are said to be adjacent if there exist an edge this vertices.
- Degree: No of edges connected to a vertex (self loop counted twice) is called the degree of the graph.
- **Isolated Vertex and pendant** : Vertex with degree 0 and 1 respectively.
