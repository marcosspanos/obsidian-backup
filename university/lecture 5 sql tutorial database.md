# basic syntax:
![[Pasted image 20250408161004.png]]
from clause 
	declares which tables are accessed
the where clause
	 specifies a condition for rows in these tables to be considered for this query 
the select clause 
	specifies the attribute of the result 

the from clause can be understood as declaring variables that range over tuples of a relation 

![[Pasted image 20250408161335.png]]


for each table in the from clause there is a tuple variable 

- if the name of the variable is not given explicitly the variable will have the name of the relation
- ![[Pasted image 20250408161527.png]]


if a tuple variable is explicitly declared then we need to use it 
## attribute reference
in the form 
R.A
if r is the only tuple variable with attribute A then writing just A is fine


# joins:
these specify combination of rows to consider
the query optimiser looks at the query and tries to determine the most efficient way to evaluate the query 
query optimiser might build an index structure to be more efficient

we dont need to understand how the query optimiser works
the simple for each is sufficient

a join needs to be explicitly specified in the where clause 
![[Pasted image 20250408162506.png]]
a join condition correlates the two tables 

it is almost always an error if there are two tuples variables which are not linked via join conditions

we can show the join condition in a join diagram
![[Pasted image 20250408162740.png]]
they typically correspond to the foreign key relationships


# cycles in connection graph
the connection graph may contain cycles which make the selection of the right path more difficult and error prone



## unnecassary joins
query will run slower if there are redundancies 

# duplicate elimination:
a difference between sql and relational algebra is that duplicates need to be explicitly eliminated in sql 

the distinct modifier may be applied to the select clause to request explicit duplicate row elimination

## when to use distinct
![[Pasted image 20250414175958.png]]
K is the set of attributes that are uniquely determined by the result 


## query formulation traps:@
- missing joins conditions (very common)
- unnecessary joins (may slow query down significantly)
- self joins
- unexpected duplicates
- unneccessary distinct


# left / right outer and inner joins
![[Pasted image 20250414181611.png]]
the dbms would add the join to the query 
the join predicates arises implicitly by comparing all columns with the same name in both tables

## specifying 
- natural
	- yields comparison of columns with the same name
- using 
	- The Ai must be columns appearing in both tables 
- on
	- The matching condition works similar ot the where clause but it is important in combination with left/right joins

the cross join operator has no join predicate

![[Pasted image 20250414181857.png]]
## inner/ outer joins
![[Pasted image 20250414181937.png]]


