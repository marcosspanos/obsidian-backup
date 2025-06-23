# relational model:
table entries are values that conform to data types/
there are some certain data types which are built into sql 
available data types depend on the database management system and the management version of the sql standard

## domain:
the domain is the set of possible values the data types can take

sql allows to define application specific domain as subset of standard data types

domains are useful to document that two columns represent the same kind of objects and comparisons are meaninful 
# database states:
## tuples:
a tuple with respect to the relation schema 
is a sequence of values that di belongs to dom (Di)

![[Pasted image 20250404203731.png]]

## database state:
database I for database schema S defines 
- for every relation name R
- a finite set of tuples I(Ri) with respect to schema 

## summary database states:
- relation -> classes
	- tuples -> objects
		- attribute -> object properties 

# null values:
the relational model allows missing attributes values
formally the set of possible values for an attribute is extended by a new special value null 
the null is not the number 0 but instead a different from all values of any data type

 they are used to model 
 - no value exists
 - the attribute is not applicable for this tuple
 - a value exists but is not known
 - any value will do 

there are no clear semantic for null values

without null values  we would need to split a relation into many more specific relations -> subclasses
this makes it easier if there are a couple of students who do now have a 

if null values arent allowed then users might make up fake values 
this is bad for database design because a value not being known is represented in many different ways

## problems:
to get null rows we need to use select rows where A is null 
some languages do not know about null values 
this complicates application programs

by default sql allows attributes to be null 
this is done by using not null condition -> this leads to simpler application and fewer surprises

# integrity constraints:
integrity constraints are conditions which every database states need to satisfy 
integrity constaints should make the dbms to refuse any update that violates them 

## create
- not null 
- key contraints
	- values can appear only once
- foreign key constraints
	- values must appear in another table
- check constraints
	- given predicate

## why:
- constraints document knowledge about valid db states
- some protection against data input errors
- enforcement of law/ company standards
- protection against incosistency 
- queries application programs become simpler if the programmer may assume teh data fulfills certain properties


# keys:
a key of relation r is set of attributes that uniquely identify the tuples in R
![[Pasted image 20250404205751.png]]

the dbms will refuse keys which are the sam

## composite keys:
key rows may agree in A or B but not both 

all relations satisfy the key constraint

any superset of a key is still a key
a key is minimal if no proper subset is a key

![[Pasted image 20250404210911.png]]
minimal is often required

in the relational model one key is designated as the primary key 
a primary key cant be null 

## good design practice
primary key
- consists of single attribute
- is never updated

this is good for
- consistency -> applications might store the key
- indexing and retrieving items

keys are constrains -> they refer to all possible db states not only the current one

 you should create an artificial id which makes it easy to identify tuples
when declaring keys think about all intended database states

# foreign keys:
there are not links or pointers 
we instead use key attributes to reference a tuple

they refer from a relation r to tuples of S 

such a reference is only stable if the address does not change 
if the key attributes are not updated 

a foreign key implements one to many relationship 
foreign keys are not themselves keys
they do not identify uniquely the tuple


## constraints:
the foreign key constraint ensures that there is a valid key that the foreign key points to 
foreign keys may bu null unless not null constraint

![[Pasted image 20250404213040.png]]
