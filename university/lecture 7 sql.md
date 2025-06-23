to write for all we can write not exists not for x which is the same exists for all x 
# implication:
there is no implication pattern so for the implication of f1 implies f2 we instead use 
not f1 and f2


# all any some
we are able to compare a single values with all values in a set 
example syntax 
``` sql 
SELECT ...
FROM ...
WHERE attribute COMPARISON ALL/SOME (select ...)

```
the comparison here represents > >= = 
the all comparison is universal while the any is existential 


# nested subqueries:
subqueries are always executed before the main query is done as the table is the one where a condition applies for the query 

# aggregations:
these are functions from a set or multiset to a single value 
they take a set of values and return a single value 
one example is min 

they are also known as group functions or column functions 

there are five main categories
1. count
2. sum 
3. avg
4. max
5. min 

all these ignore null values

the aggregate functions go in the select clause 

## handling null values:
usually null values are filtered out but there are some excpetions
count counts null values
and it also counts rows not attribute values


# group by:
this constructs partitions of a table into disjoint groups

``` sql 
SELECT    (group by attributes and aggregation functions)
FROM      ...
WHERE     ...
GROUP BY  attributes

```

when using group by we are only able to use attributes which are guaranteed to have unique values for every group 

## grouping without aggregation
duplicates should be eliminated with distinct 


# having:
we can filter out entire groups based on some aggregated group property 
this is possible using the having clause 

the where clause refers to single tuples, the having condition applies to entire groups 
