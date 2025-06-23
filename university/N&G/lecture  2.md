[[lecture 1 N&G]]

# questions during reading lecture:
1. what are bijections
2. what is intermediate hardness
3. is the original graph a subgraph of itself?
4. find the formula for generalization of Kn
5. what does isomorphic subgraph with n edges mean
6. what does it mean not distinct elements
7. how are vertices repeated if we are moving to another vertex
8. what are connected graphs
9. what does connected component mean

# actual notes:

## graph isomorphism:
[[definitions networks and graphs#^b2b437]]

two graphs with different vertex sets and different edges can be represented using the same diagram 
### conditions:
to prove graphs are not isomorphic we generally want 3 conditions:
1. size of the vertex sets must be the same
2. edge set 
3. degree sequence

even if these hold then the 2 graphs might not be isomorphic still

### applications:
- chemistry:identifying a chemical compound within a chemical data base:
- integrated system design: check to see if the layout of the circuit design is compatible with the schematic plan
- cryptography: zero knowledge

## walks and paths:
[[definitions networks and graphs#^2fe11c]]
two vertex are connected if there is an xy walk between them

the 4th definition works for digraphs as well but then we have directed walks/paths and instead call y reachable from x when there is an xy walk

## distance:
[[definitions networks and graphs#^7146a6]]

these definitions are especially important for weighted graphs because this means edges might have different weights or costs 
A weighted graph is represented as G = (V, E,w) where w: -> R is a function on edges

### applications:
- distances on a map ( often weighted graphs where edges can have different weight costs )
- routing in computer networks

## cycles:
[[definitions networks and graphs#^15d785]]

## applications:
- detection of infinite loops in certain programs
- dead lock detection in operating systems
- checking if a node in a list points to an earlier node
- scheduling: directed graphs and job dependencies



## connectivity:
[[definitions networks and graphs#^f1f8c8]]

the definition above can be proven to be equal to those following:
- G is connected if and only if for every pair of vertices u, v which belong in  V(G) there are u and v connected 
- G is connected if for every non empty sets of vertices X and Y there is a path with one end point in X and one end point in Y 

connectivity in undirected graphs is an equivalence relation:
- reflexive: for any v which belongs to G v is connected to itself
- symmetric: for every pair of vertices u and v if v is connected to u then u is connected to v 
- transitive: for any three vertices u v w if u and v are connected and v and w are connected then u and w are also connected 

the equivalence of vertices under connectivity relation are called connected components

### connected components:

[[definitions networks and graphs#^f1f8c8]]

every undirected graph G can be represented by union of its connected components
the number of connected components is given by c(G)


## trees and forests:
[[definitions networks and graphs#^db0976]]

graphs that have this structure are binary trees and other tree structures we have seen in other courses before 
A graph with no cycle is called acyclic 
for undirected graphs this is equivalent to forests but for directed graphs having no directed cycle does not make the graph a tree


## spanning subgraphs:
[[definitions networks and graphs#^63b804]]

## induced subgraphs:
[[definitions networks and graphs#^a78665]]
if there is an edge between u, v which belong in G then it should also be included in any induced subgraph

# final questions:
- what is the difference between a path and a walk
- what are induced subgraphs


# answers to original questions:
- **What are bijections?** A bijection is a one-to-one correspondence between two sets, meaning every element in one set is paired with exactly one element in the other set, and vice versa. In graph theory, a bijection between vertex sets of two graphs is often used to show that the graphs are isomorphic.
- **What is intermediate hardness?** Intermediate hardness typically refers to problems that are harder than P (solvable in polynomial time) but not as hard as NP-complete problems. In the context of graph theory, this may relate to certain graph problems that don't fit neatly into these categories, such as the Graph Isomorphism problem, which is suspected to be neither in P nor NP-complete.
- **Is the original graph a subgraph of itself?** Yes, any graph is a subgraph of itself. A subgraph consists of a subset of the vertices and edges of the original graph, and since a graph includes all its own vertices and edges, it is trivially a subgraph.
- **Find the formula for generalization of KnK_nKn​.** The complete graph KnK_nKn​ has nnn vertices and every possible edge connecting them. The number of edges in KnK_nKn​ is given by the formula n(n−1)2\frac{n(n-1)}{2}2n(n−1)​. The generalization for KnK_nKn​ could refer to varying the number of vertices or edges based on a different structure.
- **What does isomorphic subgraph with nnn edges mean?** An isomorphic subgraph with nnn edges means that there exists a subgraph with exactly nnn edges that has the same structure (i.e., connectivity and relationships between vertices) as another graph. This involves a one-to-one correspondence between the vertices of the subgraph and another graph.
- **What does it mean by not distinct elements?** "Not distinct elements" usually refers to elements that are identical or repeated within a set or context. In graph theory, this could relate to vertices that are the same or edges that are counted multiple times in certain representations.


# answer to final questions:
## Difference Between a Path and a Walk

- **Walk**: 
  - A walk in a graph is a sequence of vertices where each adjacent pair of vertices is connected by an edge.
  - A walk can revisit vertices and edges multiple times.
  - It can be of any length, including zero length (which is just a single vertex).

- **Path**: 
  - A path is a specific type of walk where no vertex is repeated.
  - It is a sequence of distinct vertices, meaning each vertex appears only once in the sequence.
  - Paths represent a more restrictive form of traversal compared to walks.

## Induced Subgraphs

- An **induced subgraph** is formed from a subset of vertices of a graph and includes all the edges that connect pairs of vertices in that subset.
- Given a graph \( G = (V, E) \) and a subset \( V' \subseteq V \), the induced subgraph \( G[V'] \) is defined as:
  \[
  G[V] = (V', E')
  \]
  where \( E' \) consists of all edges \( (u, v) \in E \) such that both \( u \) and \( v \) are in \( V' \).
- Induced subgraphs maintain the connections of the original graph among the chosen vertices, reflecting the structure of the larger graph.



