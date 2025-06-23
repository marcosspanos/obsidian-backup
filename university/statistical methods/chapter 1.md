# randomness:
[[definitions statistical methods#^ddea1d]]
this is related to random experiments

this can be viewed as a way to express lack of information
an example of this would be a coin flip. We don't know which result we will get after we flip the coin

## examples:
- flip a fair coin (multiple times)
- length of pregnancy
- value of stock 
- time till death


## probability:
to talk about probability we must know 
- sample space 
- events(subset of sample space)
- probability 
- conditional probability 


## set theory 
[[definitions statistical methods#^d8ed57]]

A set is denoted by a capital letter and denoted by listing its elements in curly brackets 
(A = { a,v,n}) is an example of a set 

the ordering of set does not matter, if they have the same elements in different order they are still the same set 

the universal set is the set which contains all the elements we are studying, this is denoted by S( this is also the sample space )

the set with no elements is called the null set or the empty set 

## venn diagrams:

they are useful to visualise relationships between sets
a set is depicted as a closed region while the sample space is usually a rectangle

example of venn diagram
![[Pasted image 20241101110354.png]]
### intersection:
the intersection of 2 sets contains all elements which are both in A and B 

### complement:
the complement of a set contains all elements which are part of sample space but not part of that set

### disjoint sets:
sets are disjoint if they do not have any shared elements

- the intersection of 2 disjoint sets is 0 by definition

## de morgan theorem
[[definitions statistical methods#^39220b]]

we use de morgan law when we want to flip from an intersection to a joining 2 sets together but then we need to complement the sets 
## distributive law:
[[definitions statistical methods#^e1966d]]

this allows us to rearrange sets if we have formulas we already know so we can use them 


## cartesian product:
[[definitions statistical methods#^c50506]]

the pairs are ordered so if we switch them around before multiplying those 2 are not equal 

## cardinality:
[[definitions statistical methods#^4dd436]]

if set A has a finite element count then it's cardinality is how many elements are in the set 

### infinite sets:
- countable infinite sets:
- uncountable infinite sets

if 2 sets are countable then the cartesian product is also countable 


## functions 
[[definitions statistical methods#^4156b2]]

- each input in the domain is mapped to exactly one output in the co domain
- the range is the set of all possible values of f(x) and is a subset of the co domain 


## axioms of probability:
[[definitions statistical methods#^f0f5eb]]

union means or and intersection means and

## discrete probability models:#
- if sample space is countable we can list of all of the elements
- if A ⊂ is an event then A is also countable and![[Pasted image 20241101113645.png]]

### finite special case with equal probability:
- All outcomes are equally likely => P(si) = 1/N where N is the number of elements
- if A is an event with cardinality |A| = M then we have ![[Pasted image 20241101113855.png]]

## sum rule:
[[definitions statistical methods#^b832a1]]

- probability of the empty set is 0 
- P (Ac) = 1 − P (A)
- If A ∩ B = ∅ then P (A ∪ B) = P (A) + P (B)

## conditional probability:
[[definitions statistical methods#^3536d9]]

- this deals with how you should update probabilities given more information


this doesn't mean we need to discard the axioms for probability but just update them 
[[definitions statistical methods#^f0f5eb]]
### useful results for conditional probability:
![[Pasted image 20241101114859.png]]
## independence:
[[definitions statistical methods#^325a62]]

independence is not the same as disjointness 
the differences are shown in the table below
![[Pasted image 20241101115010.png]]


## law of total probability:
[[definitions statistical methods#^86ab1f]]


## bayes rule:
[[definitions statistical methods#^f07347]]


# questions 
look more into finite special cases with equal probability

how to use total law rule thing
bayes rule application

