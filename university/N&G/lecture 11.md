# questions during lecture:
1. what is a flow network 
	1. a source and a sink with edges and vertices in between which a certain number of something goes from the source to the sink 
2. things going in = things going out?
	1. this is the flow conservation which says that the total flow going into a vertex must be the same flow that goes out of the vertex otherwise this principle does not hold
3. what are cuts
	1. we create a cut when we split a graph in segments, the flow between the two cuts are the edges which go from the source cut to the sink cut
4. 

# random notes:
we want to send the maximum amount of information the graph can handle 
there is traffic and we want to find the path which will maximise the flow in the graph
need to match the flow going inside any vertex to the flow going out of it, 
except the sink and the source a 
edge being saturated => cant send any more flow to the edge
edge being avoided => there is a 0 flow to the edge 
when i cut a graph there are some edges which go between the parts 
the edges between the cuts tell us how much flow can go from one part to another 
we want to find the cut with the smallest capacity 
if we saturate the edges goign the right direction and dont use the ones going in the wrong direction then we have the maximum flow # corollary4
we want to change the graph to "delete" cycles from the graph
	we add a vertex to prevent cycles


# actual notes:
## flow conservation:
![[Pasted image 20241204142557.png]]
this means that the flow coming into an edge must be the same flow coming out of that same edge for all edges in the graph 

an edge can be saturated meaning no more flow can go through that edge 
an edge can be avoided meaning no flow is going through the edge 

## cuts:
a cut is a partition of V into 2 parts with distinct vertices and edges in each one 
The capacity of a cut is measured by the edges between the two partitions 
the max flow between the two partitions is the capacity of the edges 

![[Pasted image 20241204143435.png]]
### minimum cut:
![[Pasted image 20241204143731.png]]

## ford fulkerson:
we keep pushing flow along augmenting paths in G
![[Pasted image 20241204144818.png]]
### integrality:
![[Pasted image 20241204144925.png]]

### running time:
![[Pasted image 20241204144958.png]]
