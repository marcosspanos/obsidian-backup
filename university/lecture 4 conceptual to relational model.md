we translate from an entity rleation

# basic idea
entity sets and relationships are represented as tables
there is roughly
- one table for each entity set
- one table for each relationship set 
- columns rougly correspond to the attributes


A strong entity sets becomes a table with columns for each attributes
![[Pasted image 20250408141527.png]]
a weak entity set becomes a table that includes 
- columns for the attributes 
- columns for the primary keys of the identifying entities

![[Pasted image 20250408141631.png]]

a many to many relationship sets becomes a tasble with 
- columns for the attributes of the relationship set and 
- for the primary keys fo the participating entity sets

![[Pasted image 20250408141757.png]]

we can use this relation for arbitrary relation sets
this depends on the cardinality set


# eliminating tables:
we can do this for efficiency 
we get more possibilities to design cardinalities constraints


## many to zero or one
- adding an extra attribute  to the many side with the primary key of the one side 

![[Pasted image 20250408142020.png]]


if participation is partial then replacing the table by an attribute will result in null values for the entities that do not participate in the relationship set

if the participation is total 1-1 then declare foreign key not null
for one to one relationship sets either side can be extended with the key of the other 

tables for relationship sets linking weak entity sets to the identifying set can always be eliminated
there is no need for extra table 

# cardinalities and constraints
when translating entity sets and relationship sets to tables
- every table should have a primary key
- declared foreign keys constraints for each relation

## foreign keys
should be declared
- not null or not
- unique or not
## attributes
attributes should be declared not null and or unique if appropriate

![[Pasted image 20250408143623.png]]


# composite and multi valued attributes
they are flattened out by creating a separate column for each component attribute

## multi values
A of an entity E is represented by a separate table with
- columns for primary keys of E 
- columns for the attribute value
each single value of the multi valued attributes get its own row


# isa:
## hierarchy of tables
- table for the higher level entity set
- table for each lower level entity set-> includes primary key of higher level entity set and local attributes

this requires accessing multiple tables
![[Pasted image 20250408144059.png]]
## many tables
form a table for each entity set with all local and inherited attributes

![[Pasted image 20250408144235.png]]
if specialisation is total when we need no table for the generalised entity 

### drawbacks
- explicit table for the generalised entity might be needed for foreign key constraints
- attributes are stored redundantly if an entity belongs to several specialised entity sets -> overlapping ISA

## one table with null values
from a single table with local and specialised attributes

if an attribute is not applicable we just fill null in the table 

the advantage is we dont need joins
null values are needed
# model keys/ recursive relations

it is often good to introduce an artificial internal keuy
- unique 
- does not change
- it doesnt have a descriptive meaning

## recursive relations:
it depends on the cardinality 
![[Pasted image 20250408160544.png]]
this is for 0 to 1 relations

if it is many to many we need a separate table with 2 foreign keys which both refer to the same table 
