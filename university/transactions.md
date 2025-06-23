# transactions

a transaction is a sequence of one or more actions performed on a database

## definition
a transaction is a list of following actions
1. reads 
2. writes
performed on a database object O 
transactions end with commit or abort 

## interrupted transactions:
![[Pasted image 20250429212622.png]]
when a transaction is partially but not fully executed then there are unintended results

a transaction should be an atomic event
it should either be fully executed or not at all but never partially

## concurrent access anomalies
when transactions operate on the same objects concurrently there might be concurrency issues

- lost update anomaly 
	- the effects of one transition are lost due to an uncontrolled overwrite performed by a second transaction
- dirty read anomaly 
	- a transaction reads values change by another transaction which is aborted so the values will revert 
- non repeatable anomaly 
	- a transaction reads a value which is concurrently changed by anothed transition so another read of the same object will result in a different value 
- incosistent read anomaly 
	- a transaction reads the partial result of another transaction. so the former transition works data from an inconsistent database state

## acid properties:
A: Atomicity -> transactions execute fully or not at all 
C: Consistency -> transactions always leave the database in a consistent state where all defined integrity constraints hold 
I: Isolation -> multiple users can modify the database at the same time but will not see each others partial actions
D: Durability -> once a transaction is committed successfully the modified data is persistent regardless of disk crashes


# schedules:
the scheduler decides the execution order of concurrent database access

## definition:
A schedule is a list of actions from a set of transactions 
the order in which two actions of a transaction T appear in a schedule must be the same order as they appear in T 

## serializable schedule
A schedule is serial if the actions of the different transactions are not interleaveaved 
they are executed one after another

the advantage is that transactions are executed in full isolation
the lack of concurrency is a big disadvantage 
some transactions spend a lot of time waiting for io resulting in an idle cpu 
for a responsive database and for optimal cpu usage it is important to allow transactions to be executed in parallel 

# conflicts:
there are several types of conflicts between transactions:
1. write read 
2. read write
3. write write

actions conflict if 
- they are from different transactions
- they involve the same data item
- one of the actions is a write

# conflict seriazibility 
when transactions are executed concurrently and operate on the same data conflicts arise 
we want the schedules to be serializable 
## swap non conflicting actions
we can swap actions without changing the outcome if the actions are non conflicting 

## conflict equivalence
two schedules are equivalent if they can be turned into each other by a sequence of non conflicting swaps of adjacent actions

## conflicting serializable schedules
a schedule is conflict serializable if it is conflict equivalent to some serial schedule 


## precedence graphs
in order to determine whether a particular graph transaction schedule is conflict serializable we can draw a precedence graph

- the graph has a node for each transaction
- there is an edge from transaction T1 to T2 if there is a conflicting action between them 


## conflict serializablity via precedence graphs:
if the precedence graph contains no cycles then the schedule is conflict serializable 
we can obtain the schedule with a topological sort of the precedence graph 

