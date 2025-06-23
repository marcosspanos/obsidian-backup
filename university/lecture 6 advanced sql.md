#  non monotonic queries
sql queries using only constructs from before are monotonic constructs

if further rows get inserted then these queries yield a superset of rows



non motononic behaviour in natural language are phrases like 
- there is no 
- does not exist
-> negated existential quantificatioin

- for all 
- the min/max
-> universally quantification

this boilds down to a test whether yields a non empty result

# not in:
checks whether a value appears in the result sql subquery 

the subquery is evaluated before the main query 
then the query is computed on the table returned by the subquery 

# exists/not exists
check whether subquery result is empty or not 

when we have a loop in the out row then the subqyert will be evaluated as many time as we have rows

non correlated subqueries with not exists are almost always an indicator of an error 
non correlated subqueries evaluate to a set relation constant and may make perfect sense 
