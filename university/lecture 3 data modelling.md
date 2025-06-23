# phases of database design
the goal is to 
- formal model of the relevant aspects of the real worl
- the real world serves as a measure of correctness

this is challenging because it requires 
- expertise
	- requires expertise in the application domain
- flexibility 
	- real world often permits exceptional cases 
- size 
	- they can become huge

## phases:
3 phases
1. conceptual database
	1. what information we store
	2. how are the information related to each other
2. logical database design
	1. transformation of the conceptual schema into the schema supported by the database
3. physical database design
	1. design indexes, table distribution 
	2. maximise performance of the final system

# entity relationship model 
- entity sets 
- relationship sets
- attributes

![[Pasted image 20250404213722.png]]

## entity 
an abstract objecg
they have attributes
an entity set is a collection of similar entities 
- similar -> share same properties


## attributes:
these represent an entity set 
types:
- simple
- composite
- single valued
- multi valued
- derived attributes

## relationship sets:
relationship is an association among several entities

relationshio set is a set of relationship of the same kind 
![[Pasted image 20250405091712.png]]

## degree of a relationship set:
refers to the number of entity sets participating in the relationship 
![[Pasted image 20250405091831.png]]

non binary relationship sets can be represented using binary ones by creating an articial entity set


# cardinality limits:
express number of entities to which another entity can be associated via a relationship model 
we use the uml notation

![[Pasted image 20250405093402.png]]

if cardinalities are not given the default is many to many

## total participation:
means every entity in the entity set participates ina t least one relationship in the relationship set



# relationship sets with attributes:
an attribute can also be a property of a relationship set

# weak entity sets:
 an entity set without a primary key 
 this depends on the existence of an identifying entity set
 there must be a total one to many relationship set from the identifying entity set to the weak entity set 
 this is depicted by the double diamond
the discriminator is a partial key 
it needs the primary key of the identifying primary key


# ISA inheritance:
![[Pasted image 20250405094750.png]]

## specialisation:
top down design process
identify subgroups within entity sets
there subgroups become lower level entity sets which may have attributes 

## generalisation:
 bottom up design process
 combine a number of entity sets that share common features into a higher level entity set

## membership 
value based -> assigns an entity to a specific subclass based on attributes values
default -> is user defined-> manual assigmnent to subclasses


## complete constraint
total specilisation 
each superclass entity must belong to a subclass
