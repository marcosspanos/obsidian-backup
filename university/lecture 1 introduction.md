# course goals:
thourough understanding of database concepts
 - from a user perspective 

# learning goals:
- developing data models -> entity relationship models
- reasoning about good/bad designs
- understanding and writing non trivial sql statements
- basic knowledge of database programming


# structure of course
- introduction
- data modelling
	- entity modelling 
	- unified modelling language
- relational mode
- advanced sql 
- functional dependencies
- transactions
- database api's


# database:
a collection of 
- certain logical structure
- specific semantics
- specific group of users

## database management system
allows to
- create modify and manipulate a database
- query and retrieve data using a query language
- support persistent storage of large amounts of data
- enable durability and recovery from failure
- control access to the data by many users in parallel 


## motivation for dbms:
- data independence
	- logical view on the data indepenedent of physical storage
	- user interacts with a simple view on the data
	- behind the scenes are complex structures which allow for rapic access and manipulation
- avoidance of duplication
	- different views on the same database
there are also different views for different applications

this is achieved by the ansi sparc architercture
## levels
there is the physical level
	how data is stores
	disk pages index structures
the logical level 
	describes data stored in the database
	relations among data
and the view (external ) level
	application programs hide details of data types
	hide information for privacy or security 

these 3 levels ensure logical and physical data independence

## logical data independence
the ability to modify the logical schema without breaking existing applications

## physical data independence
ability to modify the physical schema without changing the logical schema 


# relational model;
view and logical level represent data as relations/tables

in pure relational model a table is a set of tuples 
- no duplicate tuples
- no order on the tuples


the tables can be thought of classes 

## database schema
structure of the database -> relations + constraints

# structured query language
high level declarative query language
- query tells what you want independent of storage structure
- efficient data access

we only describe what information we want 
we dont need to prescribe how to retrieve the information
the database will then handle how to retrieve information


## imperative vs declarative languages
algorithm = logic + control 

### imperative
- explicit control 
- implicit logic
### declarative 
- implicit control 
- explicit logic


sql is a declarative data manipulation language
the user describes condition to be met 
![[Pasted image 20250331174708.png]]
select -> properties to include in output
from-> which database we use
where -> what conditions to be met

the database system will take this query 
- decide how to execute efficiently 


## data models
- well defined data models and data integrity constraints
	- relational model
	- meta langauge for describing 
		- data
		- data relationships
		- data constraints
sql can be used for table and contraint definitiion


### integrity constraints
- primary key constraint
	- database will reject duplicates keys
- foreign key constraint
	- there must be a key matching the foreign key 

there are data constraints
columns constrains and check constraints (logical constraints)

## sql ddl:
![[Pasted image 20250331175126.png]]
constraints are after datatypes
varchar -> string
check constraints are after data column constraints


![[Pasted image 20250331175250.png]]

## concurrent access and transactions:
- transaction with acid properties

a transaction is a sequence of operations that perform a single logical function in a database application

### acid properties
- atomicity -> executed fully or not at all 
- consistency -> database remains in a consistent state where all integrity constaints hold
- isolation -> multiple users can modifyu database at same time but they should operate as if alone
- durability -> once a transaction is confirmed then the modified data is persistent 

# design database schemes
## entity relationship modek
- entities -> objects
- relationship between entities

	