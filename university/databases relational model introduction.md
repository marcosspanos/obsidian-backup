# data types and domains
table entries are values which conform to some data type
available data types depend on the database management system and the supported version of the sql standard 

## domain:
the domain dom(d) of a type d is the set of all possible values 

sql allows us to define application specific domains as subsets of standard data types

# relation schema
a relation schema s of a single relation defines 
- a finite sequence A1... An of distinct attribute names
- for each attribute a data type (or domain )
a new relation schema can be written as 
s = A1: D1.. An : Dn



## notation:
these are used to communicate schemas from human to human


# relational database schemas:
they define 
- a finite set of relation names
- a relation schema for every relatiion
- a set of integrity constraints 

## example 
![[Pasted image 20250513113517.png]]


# database state: tuples:
tuples are used to formalise table rows
A tuple t with respect to the relation schema 
s = (A di .. )

given a tuple t we write t.A1 for the value in column A1


## database state 
this is equal to set of tables conforming to the schema
except 
- there is no order on the tuples
- tables contain no duplicate tuples


# relational model null values

the relational model allows missing attribute values
table entries may be empty 

formally the set of possible values the domain for an attribute is extended by a new special value null


## null values:
they are used to model scenarios where
- no value exists
- the attribute is not applicable for this tuple
- a value exists in the real world but its not known 
- any value will do 

if null values arent allowed then users might make up fake values to fill in the missing columns which is worse than having a null value

# integrity constraints
## valid database states
database should model the relevant part of the real world
the plain definition of tables often allows too many meaningless database states

integrity constraints: 
- this restricts to possible database states
- they are specified in the database schema

# keys:
a key of a relation r is a set of attributes that uniquely identify the tuples in r 


A key is minimal if no proper subset is a key 

A relation may have more than one minimal key but there is only one primary key 
A primary key cant be null 
all other keys are alternate or secondary keys
## keys as constraints
they refer to all possible db states not just the current ones
