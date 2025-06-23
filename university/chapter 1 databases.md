# world of databases;
they are essential to any business
## evolution of databses:
databases are nothing  more than a collection of information that exists for a long period of time
the dbms is expected to
1. allow uses to create new databases and specify their schema
2. give users the ability to query data and modify the data using an appropriate language often called a query language 
3. support the storage of a very large amount of data over a long period of time allowing for efficient access 
4. enable durability -> the recovery of the database in the face of failures 
5. control access to data from many users at once without allowing unexpected interactions between users


### early dbms
the first dbms appeared in the late 1960 
they evolved from file systems 
file systems cant quarantee that files wont be lost if they are not backed up 

the first important application of dbms were ones where data was composed of many small items
1. banking systems -> maintaining accounts and making sure that systems do not cause money to disappear
2. airline reservation systems
3. corporate record keeping


## relational database systems;
there was a popular paper which introduced the idea of relations for databases 
databases should present the user with a view of data organised as tables called relations

by 1990 relations were the norm for dbms but databases continued to evolve and change

## smaller and smaller systems:
at the beginning dbms were large expensive systems running on large computers 
this has changed as computers have become smaller and smaller allowing even a laptop to run a dbms at this point


## bigger and bigger systems
data has increased in size rapidly 
a gigabyte is not that big anymore 
there are databases which hold a petabyte of data

## information integration:
this is one of the biggest problems in building and maintaining databses
it is hard to join the information contained in many related databases into a whole


# overview of a database managament system
conventional users and applications programs that ask for data or modify data
a database administrator -> a person or people responsible for the structure or schema of database


## data definition language commands
this allows database administrator to set specific rules for the data inside the database


## overview of query processing:
![[Pasted image 20250402112617.png]]
### answering the query:
the query is parsed and compiled by a query compiler 
the resulting query plan is passed to the execution engine 
this issues a sequence of requests for small pieces of data 
the requests for data are passed to the buffer manager which is responsible for bringing appropriate portions of the data from secondary storage 

### transaction processing 