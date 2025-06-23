# ensure serialiability 
1. pessimistic 
	1. lock based concurrent control and timestamp based concurrency control 
2. optimistic 
	1. read set write tracking and validation before commit 
3. multiversion techniques
	1. eliminate concurrency control overhead for read only queries

## lock based concurrent control 
this is one of the pessimistic strategies 
types of locks:
- shared locks -> is acquired on Y before reading Y 
  many transactions can hold a shared lock on y 
- exclusive lock 
	- a transacton holds an exclusive lock on y if no other transaction holds a lock on y before it 

## two phase locking
this is what is used in dbms today 
each transaction must get
- an s lock before reading it 
- an x lock before writing it 

# deadlocks:
two phase locking has risks of deadlocks

## deadlock detection 

- the system maintains a waits for graph
- the system checks for cycles in the graph
- if cycle is detected the deadlock is resolved by aborting one or more of the transactions

# cascading rollbacks

when a transaction reads unconfirmed data from another transaction there is a risk of cascading rollbacks 
if the latter is aborted then the former transaction also needs to be aborted
