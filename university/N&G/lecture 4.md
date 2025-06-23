# strongly connected components:
[[definitions networks and graphs#^a3192c|strong connected components]]

there is a unique partition of V into SCC's 
this is because bireachability is an equivalence relation so if u and v are
 bireachable and v and w are bireachable as well that makes u and w bireachable as well 

## how to compute the strongly connected components given a directed graph:

we can either use DFS/BFS and keep track of the vertices which are reachable from each position 
the running time for this algorithm is $O(n(n+m))$ 

## graph of SCC 
for any digraph the SCC graph is a DAG 
![[Pasted image 20241107155717.png]]


## sink SCC:
[[definitions networks and graphs#^385020|sink SCC]]

- at least one sink SCC exists 
	the final SCC in the topological sort must be a sink since there cant be any incoming edges to that 

## lemma 5:
![[Pasted image 20241107160244.png]]

![[Pasted image 20241107164005.png]]

this is the proof for the lemma above 
the vertex with the max finishing time is in the source SCC (with no incoming in G)

the previous lemma implies 
- vertex with the max finish time is in the source SCC 
- Consider a graph G ′ remaining at a given stage of the algorithm. If we remove
the sink SCC C ′ and G ′ ∖ C ′ is non-empty, the vertex with max finish time is still
in G ′ ∖ C ′, since it is in the source SCC.
- Since the vertex with max finish time is in a source SCC (no incoming edges in
ˆG ), and we are looking for a sink SCC (no outgoing edges), we reverse the edges
- Since the vertex with max finish time is in a source SCC (no incoming edges in
ˆG ), and we are looking for a sink SCC (no outgoing edges), we reverse the edges

## strongly connected component algorithm:
![[Pasted image 20241108110045.png]]

> the idea behind the algorithm is to keep deleting sink SCC until the graph is empty 
> 
> the running time is $o(n+m)$  

## eulerian graphs:

![[Pasted image 20241108110528.png]]

![[Pasted image 20241108110915.png]]
![[Pasted image 20241108110925.png]]
![[Pasted image 20241108110939.png]]


# questions:
1. what are sinks 
2. how to use the strongly connected algoruth