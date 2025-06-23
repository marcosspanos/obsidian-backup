# questions:
1. how to know when n is much larger than m 
2. 
# random notes:
degree of a vertex can be at most n-1 

for a directed graph adjacency list it depends on whether we are storing outgoing and or ingoing edges

if n is asymptotic larger than m then the graph is disconnected

when we want to take inward degrees instead we just flip the value of the 1 to -1 to represent flipping the edge 


# actual notes:
## graph represantation:
- adjacency list
- adjacency matrix
### adjacency list:
In the adjacency list $G=\left(E,v\right)$$ for each vertex $v$ we store a list of neighbors N(v)
Concretely we have an array of n $\left\vert v\right\vert$ linked lists denoted by adj 
Each list Adj[i] corresponds to a vertex v such that u is in adj V

### space complexity:
for an adjacency matrix the space complexity is $O\left(n+m\right)$
### time complexity:
the time complexity is $O\left(deg\left(u\right)\right)$ where u is the degree of the vertex we want to find if the relationship exists 

### adjacency matrix:
In the adjacency matrix for graph G we have a |V| x |V| matrix represented by a 2d array such that 
$$ a_{ij} = A[i,j] = \begin{cases} 1, & \text{if }(i,j) \in E \\ 0, & \text{otherwise} \end{cases} $$
for undirected graphs the matrix is symmetric since if there is an edge from Node v to u there must also be an edge from node u to v 
This is not the case for directed graphs since there might not be an edge 

### space complexity:
The space complexity for an adjacency matrix is $n^2$ no matter how many edges there are since the matrix will have a position for the data there

### time complexity:
The search time is constant since we are only looking at a particular item to check if there is an edge 


## graph traversals:
- breadth first search:
- depth first search 

### applications:
- graph exploration
- connectivity
- shortest path/ connectivity
- flooding/ broadcasting a message

### bfs:
[[definitions networks and graphs#^7610be|bfs]]
the running time of this algorithm is $O(n+m)$
	we need O(n) time for initialization at the beginning 
	we need O(m) time for the main loop after that


![[Pasted image 20241106090540.png]]

### shortest path via bfs:
Bfs returns the shortest path from any source s to any vertex v (in unweighted graphs) 

### depth first search:
Instead of searching all the vertices wide explore deep and then backtrack when you have seen a vertex before 
[[definitions networks and graphs#^bdf9d4|depth first search ]]

#### running time:
>$O(n+m)$
>every node considered at most 2 times 

for each vertex we keep note of 2 values 
- d(v) which is discovery time 
- f(v) which is finish time 

## edge types:
[[definitions networks and graphs#^683235|edge types]]
## topological sort :

### dag:
[[definitions networks and graphs]]
#### applications:
- modelling dependencies/requirements of jobs that need to be scheduled 

![[Pasted image 20241106110625.png]]
![[Pasted image 20241106110654.png]]

### topological sort:
need to figure out what this means

![[Pasted image 20241106131618.png]]
this only applies to DAG because we cant have cycles or undirected graphs 
thisu is a way for us to make sure that all dependencies are completed before we move on to the next step which might require that dependency. 
There is more than one way to topologically sort a DAG 


