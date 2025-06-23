# notes
# notes during class
induction base()
induction hypothesis (assume the claim holds for N = k)
induction step(if hypothesis is true then this should also hold ) => proof 


# counting 
## combinations:

$n!/(n-k)!k!$
this is also shown as 
$comb(n,k)$


# basic of graphs:
they show the way pieces of data are connected to each other 
## undirected graphs:
the relationship between 2 edges doesnt have to follow a path but can go both ways 

**adjacent vertex**
if they have an edge to that node

N(v) = { v1, v2,v3...} for v node 
## directed graphs:
- ordered relationships 
- transportation netwroks with one way traffic 
- representing dependencies 


## degrees:
the degree sequence is the sequence of degrees of vertex degrees in non decreasing (maybe) order
this does not hold for directed graphs, there are in degrees and outdegrees 

## complete graphs:
simple graph which there is an edge between any pair of vertices 

number of edges in a complete graph:
combination 
(n 2 )

n vertices 
each has n-1 neighbors 
cant count the same edge 2 times 


d+ is outdegree
d- is indegree

## questions in slide:
1. maximum degree
	1. connected to all the other nodes




## questions:
1. how does the proof for the picture i took work (first pic) 
2. what are combinatorial argument
3. could we prove anything by induction?



# notes after class:

## induction:
[[definitions networks and graphs#^a78665|induction]]
this is useful when we want to prove something 
it consists of 3 parts 
1. base case
   this is usually the lowest case we can have usually 1 or 0
2. induction hypothesis 
	1. we assume for a random number k that the proof holds 
3. induction step
	1. in this step we must prove using our previous step that the condition holds for any number larger than our original base case 


## counting:
### permutations:
this is a way to count how many ways we can order n elements 
it is denoted as 

this is equal to n! /(n-k)!

### possible subsets:

how many subsets of size k does a set with n elements have 
this is represented as 
(n k ) and is equal to n!/(n-k)! k

#### first proof:
we have shown that there are n! /(n-k)! ways to choose an ordered set but since different ordering of the same elements should not add to the count we should divide this by k! 

#### second proof:
we can also prove this by induction 
![[Pasted image 20241029170758.png]]

## combinatorial arguments 

[[definitions networks and graphs#^ed4366]]
this is just an example of what we can prove 
## computer science applications:

- complexity algorithms 
- probability theorem
- data compression/storage
- dna sequencing
- cryptography 

## graphs:
### undirected graphs:
[[definitions networks and graphs#^2f4292]]
**example applications:**
- ordered relationships 
- transportation networks with one way traffic 
- representing dependencies
in a simple undirected graph there is at most one edge between every pair of vertices
### directed graphs:
[[definitions networks and graphs#^ce0370]]

in a simple directed graph there is at most one edge in one direction

### degrees:
[[definitions networks and graphs#^46aec1]]

![[Pasted image 20241029171643.png]]
some questions from the slides 


### complete graphs:

[[definitions networks and graphs#^0707a2]]

![[Pasted image 20241029172037.png]]


![[Pasted image 20241029172611.png]]

## handshaking lemma:

what can we say about the number of people who shake hands with an odd number of people

how to represent this as a graph:

[[definitions networks and graphs#^15730f]]
the handshaking lemma can also be used for simple directed graphs but the direction ensures no double counting 



