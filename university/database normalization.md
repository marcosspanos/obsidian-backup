# normalization
this is an important part of database design theory 
this defines when a database is in normal form with respect to some functional dependencies
tjere are different normal forms
- third normal form
- boyce codd normal form
## goal 
using database normalization we can avoid unecassary data redundancy 
## normalization algorithms
they are able to construct a good relation schemata from a set of attributes and a set of functional dependences

# functional dependencies
they are a generalization of keys that are important for design theory 

![[Pasted image 20250425222547.png]]
## definition:
a functional dependency has the form A1..An ->B1...Bn 
This functional dependency holds for a table r if for all rows t,u we have
t.A1 = u.A1 and t.An = u.An 
t.B1 = u.B1 and t.Bn = u.Bn

## keys are functional dependencies
a key functionally determines all the attributes of the relation

we try to turn functional dependencies into keys 
then functional dependencies can be enforced by the dbms as key constraints

## armstrong axioms:
![[Pasted image 20250425223409.png]]
this is useful to check whether a set of functional dependencies imply a functional dependency 

## covers
armstrong axioms can be confusing 
a simpler method uses covers
![[Pasted image 20250425223618.png]]
![[Pasted image 20250425223650.png]]
# minimal keys:
a key is minimal if removing any attribute from the key destroys the key 

## find minimal keys:
consider a relation with R with attributes r and a set of functional dependencies  F 
1. start with X = G 
2. if there is an attribute A in X such that then remove A from X
3. Repeat step 2 until no more attributes can be removed

# determinants
this is a non trivial minimal functional dependency 
## definition:
{A1...An } is a determinant for {B1..Bn} if and only if the conditions are met
1. the FD A1...An -> B1..Bn holds 
2. the left hand side is minimal that is whenever any Ai is removed then A1 ...An -> B1..Bn does not hold
3. the FD is not trivial that is {B1...Bn} is not {A1...An}


# canonical functional dependencies
we are interested in a minimal set of functional dependencies that implies all other dependencies 
we determine a minimal (canonical) set of FDS that is equivalent to the given FDs F as 
1. make the right hand sides singular 
2. minimize left hand sides 
3. remove implied fds

repeat steps 2 and 3 until all left hand sides are minimal and 

# first normal form:
the first normal form requires that all table entries are atomic 
## examples of atomic values
- strings 
- number 
- boolean values

## not atomic values
- lists
- sets
- records
- relations

# boyce codd normal form 
this requires that all functional dependencies are keys

## definition:
a relation R is boyce codd normal form if al of its fd are implied by its key contstraints

# third normal form:
## definition:
a key attribute is an attribute that appears in a minimal key 
assume that fd with multiple arguments on the right hand side have been expanded -> every single fd has a single attribute on the right hand side

then a relation is in third normal form if every fd A1...An -> B satisifies at least one of the three conditions
1. B belongs to (A1..An)
2. A1..An contains a key of r 
3. B is a key attribute of R 

the third normal form is the standard in the industry for databases

