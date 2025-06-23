# overview of data models:
the data model is one of the most fundemental in the study of database systems
## data model:
a data model is a notation for describing data or information 
the description consists of 
1. structure of the data 
2. operations of the data-> in database data models there is a limited set of operations that can be performed. we are allowed to perform a limited set of queries 
3. constraints:-> ddm have a wya to describe limitations on the data. these constraints can range from very simple to something very complex

## important data models 
1. relational models 
2. semistructured data models including xml and related standards

## relational model 
this is based on tables 
while they might look similar to how some data structures are built in other languages the main difference is that they arent stored in memory but rather they are stored in the secondary storage of the system 
this means the algorithms need to be optimized to ensure a fast access time for the secondary storage

## semistructured model 
this resembles trees or graphs 
the principal manifestation of this is XML a way to represent data by hierachically nested tag elements
the operations on semistructured data usually involves following paths in the implied tree from an element to one or more of its nested subelements

![[Pasted image 20250402114814.png]]
constraints on the structure of the data in this model often involve the data tupe of values associated 

## other data models:
there are other data models which were associated with dbms 
a modern trend is to add object oriented features to the relational model 
1. values can have structure rather than being elementary types such as integer or strings
2. relations can have associated methods


## comparison of modelling approaches:
semistructured models have more flexibility than relations
this becomes more apparent when we show how full graph structures are embedded into tree like semistructured models
it is very important to have fast access times and to have ease of use. 
this can  be done with relational models 
1. they provide a simple limited approach to structuring data which is reasonably versatile 
2. they provide a limited yet usefyl collection of operations of data

# basics of relational model
they give us a way to represent data as a 2 dimensional table called a relation
## attributes:
the columns of a relation are called attributes 
## schemas
the name of a relation and the set of attributes for a relation is called the schema for that relation
we show schema for the relation with the relation name followed by a parenthised list of its attributes

## tuples:
a tuple has a component for each attribute

## **conventions for relations and attributes**
the convention is that relation names begin with a capital letter and attribute names begin with a lower case letter



## domains:
the relational model requires each component of the tuple to be atomic 
it must be an elementary type of int or string 
it cant be an array or any other data structure which has values broken down into smaller componenents

## equivalent representations of a relation:
relations are set of tuples not a list 

## relation instances:
the relations arent static but they change over time
there should be new tuples for movies as they appear 

## keys of relations 
there are many constraints which we are able to use using the database schema
to indicate an attribute forms a key for a relation by underlining the key attributes

## an example database schema
if the star names are unique we could use the star names to ensure there is a unique identifier for all movies in the database

# defining a relation schema in sql 
there are 2 aspects of sql 
1. the data definition sublanguage
2. the data manipulation sublanguage for querying 

the distinction between the two sublanguages is found in most languages 


## relations in sql:
1. stored relations are called tables. 
2. views which are relations defined by a computation. These relations are not stored but constructed in whole or in part when needed.
3. temporary tables which are constructed by the sql language processor when it performs its job of executing queries and data modification. These relations are then thrown away and not stored

the sql create table statement declares the schema for a stored relation. 
It also allows us to declare a key or even several keys for a relation 
## data types:
these are supported by the sql systems
1. character strings or fixed or varying length 
2. bit string of fixed or varying length 
3. the type boolean denotes an attribute whose value is logical 
4. the type int or integer denotes typical integer values
5. floating point number can be represented in a variety of ways. We may use the type float or real 
## simple table declarations 
the simplest form of declaration schema consists of the key words create table followed table of the relation and a parenthized comma separated list of the attribute names and their types


![[Pasted image 20250402212140.png]]

# algebraic query language
