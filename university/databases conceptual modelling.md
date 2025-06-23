# basic translation:
entity sets and relationship sets are represented as tables

- one table for each entity set
- one table for each relationship set
- columns rougly correspond to attributes

## strong entity sets:
they become a table with 
- columns for the attributes
## weak entity sets
they become a table that includes
- columns for the attributes
- columns for the primary keys of the identifying entity 

## relationship sets:
### many to many
they become a table with 
- columns for the attributes of the relationship 
- for the primary keys of the participating entity sets


# eliminating tables:

many to zero/one relations can be represented as 
- adding an extra attribute/ column to the many side with the primary key of the one side

if participation is partial then replacing the table by an attribute will result in null values for the entities that do not participate in the relationship set

if participation is total the declare foreign key not null 

for one to one relationship sets either side can be extended with the key of the other

tables for relationship sets linking weak entity sets to the identifying entity sets can always be eliminated

