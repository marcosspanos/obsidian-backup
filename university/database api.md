# application architecture
there are various ways we can talk to a database

## access a database:
1. static embedded queries
	1. static sql 
	2. inflexible but syntax checked at compile time
	3. sqlj embedded sql c/c++
2. dynamic
	1. dynamic sql (queries constructed at runtim)
	2. application programming interface
	3. powerful but error prone
	4. jdbc, python api
3.  object relational mapping 
	1. high navigational access behind objects
	2. jpa/hibernate ruby on rainls 

## dynamic sql;
### impedance mismatch:
database query language does not match the application programming language

there are different data types in sql which are not one to one with other languages 
![[Pasted image 20250512123536.png]]

### advantages
- powerful flexible but error prone
- sql query given as string may be incorrect
- risk of sql injection
- mismatch between sql and java types

### optimising applications
- connection pooling 
	- keep db connection open . reduces latency
- prepared statements
	- sql calls that are repeated often 
	- allows driver to optimise queries performance 
	- in jdbc created with connection.prepareStatement
	- allows parameters select * from products where id = ?
- stored procedures
	- written in db specific language -> not portable
	- in jdbc accessed with connection.prepare call
- use a driver that is bulk transfer optimised 
	- when retrieving large result sets
	- driver can send several tuples in a single network packet
# sql injection:
to prevent sql injection you should never build sql queries with user input string concatenation 
instead you should use the api to fill in query parameters


## object relational mapping:
database schemas are not always ideal 
- not the same set of constructs and abstractions
- in programming languages : objects, relations inheritance

in applications instead we would like to work with 
- objects 
- inheritance
- relations

## object relational mapping:
maps rows in tables to objects
- tables roughly equal class
- row roughly equal object
- foreign key navigation roughly pointer/ referernce


### ingredient
- mapping from objects to database
- run time library handles interaction with the database

## hcl queries:
- allow member access 
- this is not calling methods on objects 
- query may return objects

## important aspects of orm toolkits;
- mapping specification 
	- map relational data onto objects
	- can largely be derived automatically 
- query language 
	- adds objet oriented features to sql 
	- typically queries as strings (second class citizen)
- persistence
	- transaction semantics
	- languages offer start of transactions/commit/abort
- fetch strategies
	- danger of implementing queries in java
	- object caching
	- 