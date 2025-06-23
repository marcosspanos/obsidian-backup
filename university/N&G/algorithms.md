# kruskal algorithm:
sort the weights in the graph in increasing order 
then connect the edges to form a minimum spanning tree in order unless they are forming a cycle 
if they are move to the next edge and continue until all vertices are in the minimum spanning tree 
then the algorithm is done
# prims algorithm:
this algorithm allows us to find a minimum spanning tree of a graph
we have 2 sets 
one contains the vertices already in the minimum spanning tree and the other one contains all the vertices which are not in the tree yet 
we parse through the ones not in the spanning tree yet and pick the edge with the minimum weight until no vertices remain in the second set 
then the algorithm is done

# djikstra 
this is useful to find the shortest distance but only when there are no negative weights in the graph
# bellman ford:
this can find minimum distances even when there are negative weights in the graph using relaxations from each node n-1 times 

# all pair shortest
this can find the minimum path from any pair of vertices and this can even deal with negative cycles


| Djikstra                | bellman ford             | all pair                  |
| ----------------------- | ------------------------ | ------------------------- |
| only positive weights   | can use negative weights | can use negative cycles   |
| is the fastest algorith | second fastest           | slow compared to the rest |
|                         |                          |                           |

these are all connected in that they are improvements over one another in some way and lack in other areas 
there is a trade off between speed and versatility in the algorithms

# ford fulkerson:

^18a1b7

this is an algorithm which allows us to find the max flow between any two points which we call source and sink
the algorithm finds augmenting paths and pushes flow between the edges until the capacity is maxed out
then the algorithm finds another path and pushes flow through that path again 
this repeats over and over until we have no more capacity in any of the edges/ there is no other route from the source to the sink to push flow to 

## running time:
the running time of a single iteration is just a depth first search which is O(E) for the amount of edges that are in the graph
this is repeated O(f) times with f being the max flow at the end of the algorithm(this is true when the flow is increased by 1 over and over again but generally this is what holds)


## other notes:
the maximum flow is equal to the minimum cut
this is true because the maximum flow will always be constrained by the edges with the lowest value 
this means that if we find the minimum cut in a flow graph this will automatically show us what the maximum flow for the graph is



# pseudocode:
## djikstra algorithm:
![[Pasted image 20241210155903.png]]

## bellman ford:
![[Pasted image 20241210155937.png]]


## floyd warshall :
![[Pasted image 20241210160029.png]]


# ford fulkerson:
this allows us to find the bottleneck of a flow network
residual edges allow us to fix any wrong paths we have taken, this means that no matter which path we take we are able to find the max flow 

the minumum cut is the maximum flow of the graph since this will always be the bottleneck of the graph no matter what we do 
finding the minimum cut allows us to find the maximum flow for the graph


# running times:
![[Pasted image 20241210160131.png]]

# conclusions:
there is a tradeoff between speed and how much information we are able to extract from the graph 
the faster algorithms do not work when there is a negative weight because this would break the one pass over the graph since they assume that a weight below 0 is impossible 


# sources:#
https://www.geeksforgeeks.org/kruskals-minimum-spanning-tree-algorithm-greedy-algo-2/
https://www.geeksforgeeks.org/prims-minimum-spanning-tree-mst-greedy-algo-5/
https://www.youtube.com/watch?v=VbeTl1gG4l4 => ford fulkerson
