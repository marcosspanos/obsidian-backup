# dynamic programming:
the main step is to break the problem into subproblems
- optimal subproblems: the optimal solution to the problem contains the optimal solution to the subproblems
- we should have small number of subproblems 
  the number of subproblems impacts running time 
- ranges of subproblems should match the range in the optimal solution

we want to turn the optimal substructure theorem into algorithm which fills in table indexed by subproblems 
- correctness: induction and optimal substructure theorem 
- running time: sum of the time of all table entries. this often is # table entries x time per entry 

## theorem 1:
![[Pasted image 20241128185215.png]]

## bellman ford:
when the cycles are negative bellman ford doesn't work anymore 
this will make the distances smaller forever 

# floyd warshall 
this will give us all distances between all pairs of vertices 
we can use intermediate paths which all are nodes in the graph except u and v which are our beginning and end 
![[Pasted image 20241128230845.png]]
## algorithm:
![[Pasted image 20241128230929.png]]

to find negative paths we need to check if d (k)  
ii < 0. 
we start setting it 0 and if it ends up negative this means it has a negative cycle 

## optimal substructure:
![[Pasted image 20241129165156.png]]

# ongoing research:
this is all still being studied 
sometimes approximate shortest paths are ok and we want a faster algorithm instead
