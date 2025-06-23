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
- 