	# transactions:
a transaction should be atomic-> executed fully or not at all
a transaction should be immune to concurrent errors 
## transaction properties:
- atomicity 
- consistency 
- isolation
- durability 

## formal definition:
the transaction is a list of actions 
the actions are 
- reads 
- writes 
of a database object O 
transactions end with commit or abort 

# scheduler:
it decides the execution order of concurrent database access

A schedule is serial if the actions of the different transactiosn are not interleaved. They are executed one after another

A schedule is serializable if its effects on the databases is the same as that of some serial schedule

A schedule can be serialized if the there is no cycle in dependencies graph thing 
# conflicts:
there is a conflict i f
- are from different transactions
- involve teh same data item 
- one of the actions is a write
## swapping actions:
we can swap actions without changing the outcome if the actions are non conflicting

## conflict equivalent schedules:
two schedules are conflict equivalent if they can be transformed into each other by a sequence of swaps of non conflicting adjacent actions of different transactions


# conflict serializability 
given a schedule we can create a precedence graph 
the graph has a node for each transaction

a schedule is conflict serializable only if there is no cycle in the precedence graph

if there is no cycle an equivalent serial schedule is obtained by a topological sort of the precedence graph

# ensuring serializability:
there are different ways to ensure serializabilyu:
1. pessimistic
	1. lock based concurrent control
	2. timestamp based concurrency control 
2. optimist 
	1. read write set tracking
	2. validation before commit 
3. multi version techniques
	1. less concurrency control overhead for read only queries

# two phase locking:
- transactions must lock objects before using them 

## types of locks:
- shared lock S lock is acquired on Y before reading Y 
- exclusive lock 
	- A transaction can hold an exclusive lock on Y only if no other transaction holds a lock on y 

A transaction cant get new locks once it releases any lock


Any schedule that confirms to 2 phase lock is conflict serializable 


## deadlocks:
both transactions are waiting for each other before continuing which means they will never finish 

## wait graphs:
nodes of the graph are transactions
edge t1-> t2 means t1 is blocked by t2 

if there is a cycle then the deadlock is resolved by aborting one or more of the transactions


## cascading rollbacks:
once a transaction is aborted it might mean that another write might need to be aborted since it was relying on it before. this can go on and on 

we can prevent this by delaying commits 
- if t2 reads a value written by t1 then the commit of t2 must be delayed until after the commit of t1

## strict 2 phase locking:
all the same hold for this as the 2 phase locking but moreover
- a transaction releases all locks only when the transaction is completed 

this protocol is cascadeless but there might still be deadlocks


# granularity of locking:
this is a trade off 
![[Pasted image 20250510191954.png]]

## intention locks:
database use an additional type of locks
intentions locks
these are a step before exclusive and shared lock


## multi granularity locking protocol 
before a granule g can be locked in s or x mode the transaction has to obtain an is or ix lock on all coarser granularities containing g 
after all intention locks are granted the transaction can lock g in the mode 

## isolation levels:
some degrees of inconsistency may be acceptable for specific applications to gain increased concurrency and performance
