# database design:
- a formal model of the relevant aspects of the real world
- teh real world serves as a measure of correctness


this can be challenging 
- expertise 
	- requires expertise in the application domain
- flexibility 
	- real world often permits exceptional cases
- size 
	- database schema may become huge

## phases of database design
1. conceptual database design
	- what information do we store
	- how are the information elements related to each otehr
	- what are the constraints
	- er model or uml model 
2. logical database design 
	- transformation of the conceptual schema into schema supported by the database 
	- relational model 
3. physical database design
	- design indexes, table distribution buffer sizes
	- the goal is to maximise performance of the final system 

# entity relationship model 
there are 3 main ingredients
1. entity sets
2. attributes
3. relationship sets

## shapes 
- rectangles -> entity sets
- ellipses -> attributes
	- double ellipse -> multi varied attributes
	- dashed ellipse -> derived attributes
- diamonds -> relationship sets
- lines -> link attributes and relationship sets to entity sets
- underline -> indicate primary key attributes


## entity sets:
an entity is an abstract object
	specific person or event
entities have attributes
	people have names and addresses
an entity set is a collection of similar entities
	similar => sharing the same properties/attributes
	set of all persons companies.trees holidays 

### comparison with object oriented programming 
entity -> object
entity set -> class

**the er model is static**
- model structures the data not the operations
- no methods/functions associated to entity sets

## attributes
An entity set is represented by a set of attributes . Those are properties possessed by all entities of the entity set


### attribute types:
- simple and composite types
	- street is composed of street name and number 
- single valued and multi valued attributes 
	- single valued -> age of a person
	- multi valued-> person can have multiple phone numbers
- derived attributes
	- can be computed from other attributes 

## relationship set
a relationship is an association among several entities

a relationship set is a set of relationships of the same kind 

the relationship set connections can be annotated with role indicators

### degree:
the degree of a relationship set refers to the number of entity sets participating in the relationship 
- relationshop sets of degree 2 are called binary 
- of degree 3 are called ternary 

non binary relationships can be represented using binary ones by creating an artificial entity set

# cardinality limits
they express the number of entities to which another entity can be expressed via a relationship set

![[Pasted image 20250513212008.png]]


## total participation
every entity in the entity set participates in at least one relationship in the entity set


# weak entity sets
a weak entity set is an entity set without a primary key 
- the existence of weak entity sets depend on the existence of an identifying entity set
- there must be a total one to many relationship set from the underltying entity set to the weak entity set. This identifying relationship is depicted as a double diamond
# is-a inheritance:
lower level entities inherit all attributes and relationship sets of the higher level entity sets 

## specialization:
- top down design process
- identify subgroups within entity set
- these subgroups become lower level entity sets which may have attributes or participate in relationship sets that do not apply to the higher level entity sets

## generalisation:
- bottom up design process
- combines a number of entity sets that share common features into a higher level entity set 
