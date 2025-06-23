# functional dependencies:
they are 
- generalisation of keys
- central part of the relational database design theorem

this theory defines when a relation is in normal form 


if a normal form is being violated then that means that 
- there is another copy of the data 
- different concepts are mixed together 


there are different normal forms
the main ones are 
- third normal form -> the standard form used in practice
- boyce codd normal form 
	- a bit more restrictive 
	- easier to define
	- in bcnf all functional dependencies need to be keys 

there are some cases where bcnf doesnt preserve all the functional dependencies



# functional dependencies

instructor -> phone
when two rows agree on the instructor name they must also have the same phone number


## keys 
keys are functional dependencies since they uniquely determine all the attributes in the relation 

not all functional dependencies are always keys but they are always partial keys 

**the goal of database normalization is to turn FD into keys**


## covers:
they are all functional dependencies directly from an attribute as well as all functional dependencies implied by the other attributes the original attribute implies

## minimal keys
to find a minimal key we start from the cover of all the attributes and then we remove attributs until the cover isnt a key anymore 
that is a minimal key


# consequences of bad design 
## redundant storage:
- wastes storage space
- difficult to ensure integrity when updating the database 
	- all redundant copies need to be updated 



# boyce codd nromal form
A relation R is in normal form if all its functional dependencies are implied by its keys
