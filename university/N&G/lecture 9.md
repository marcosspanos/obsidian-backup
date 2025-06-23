# relaxations:
this is a common primitive for shortest path algorithms and specifically Dijkstra
relaxations are important and they are what allows us to find the shortest path from any vertex to any other vertex 
this means that we try to find if there is another shortest path to another vertex as soon as we visit a vertex. This allows us to create a path which will end up being the shortest from the vertex to any other vertex in the graph 
# Dijkstra’s Algorithm
![[Pasted image 20241126111640.png]]

## Dijkstra correctness:
### theorem 1:
Throughout the algorithm:
1. T is the shortest path tree from v to vertices in T
2. d^(u) = d(u) for every u which belongs in T 

we can prove this using induction 
it leads us to a contradiction which means this must be true 

## running time:
there are different running times depending on what data structure we are using to store the nodes

### lists:
the running time for lists is o($n^2$)

### binary heap:
the running time for binary heaps is O((n+m)log(n))

## Dijkstra limitation:
if we have negative distances then the algorithm might fail 
some examples of this are 

# bellman ford:
## dynamic programming approach:
**Sub problems:**
- OPT (u, i ): shortest path from v to u that uses at most i hops (edges)  
- If no such path, set to “infinitely long” fake path.  
- For simplicity assume each vertex has distance 0 to itself
### theorem 2:

![[Pasted image 20241126113427.png]]

this can also be proved by induction 
### algorithm for bellman ford:
![[Pasted image 20241126113532.png]]

the algorithm does not work when there are negative cycles. 
This will lead to an 
# difference between bellman ford and dijkstra:

| dijkstra                                                     | bellman ford                                                 |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Is faster for any graphs which do not have negative weights  | Is slower                                                    |
| Cant find the shortest path for graphs with negative weights | Is able to find the shortest path even with negative weights |
| Doesnt work on negative cycles                               | Doesnt work on negative cycles                               |
| Running time of O((n+m)logn)                                 | Running time of O(mn)                                        |
