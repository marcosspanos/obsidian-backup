# information hiding
- prioritize information holding 
- private should be default

a deep class hides irrelevant information and provides valuable and easily usable operations


# spr /single responsibility principle
this means designing classes so there is only one single reason to change a class
- leads to smaller and more cohesive classes
- less complex classes

group entities that change for the same reason ,separate entities that change for different reasons -> leads to functional cohesion

# encapsulation and immutability:
the act of keeping both the data and the computation together to limit the number of contact points between different parts of the system is called encapsulation
- closely related to information hiding 

## advantages:
- understanding a piece of code in isolation is easier
- using a piece of code becomes less error prone
- changing a piece of code less likely to break something elese

## how references escape:
1. returning reference to external object
2. storing an external reference internally
3. leaking a reference through a shared structure 


## copy constructors:
this is a popular technique for copying objects 
this can decrease performance if we are copying many entities 

# complexity 
complexity is anything related to the structure of a software system that makes it hard to understand and modify the system 
there are different types of complexity 
1. inherent complexity 
	1. domain complexity that cant be avoided
2. accidental complexity 
	1. avoidable technical complexity introduced through suboptimal design 
## how to reduce complexity:
- limit what methods do to 1 thing
- all classes should have 1 responsibility
- methods should not have side effects
- avoid multiple inheritance 
- avoid threads 

define understandable interfaces for important abstractions
define abstract data types to reduce duplication
avoid using floating point numbers if possible 
### decision complexity 
- avoid deeply nested conditional statements 
- avoid complext conditional expressions 



# uml diagrams:
## activity diagrams:
- the goal is to describe procedural processing aspects of a system
- more high level than state machines or sequence diagrams
- they are based on flow concepts 

### activites:
- more detailed representaiton of a use case
- functions of a business process
- steps of a complex class operation 

### actions:
- basic elements of an activity 
- in the context of an activity they are seen as atomic 
- level of abstraction can differ 
	- could be parts of an operation or a class
	- could be one complete operation of a class
	- could be several operations of one or more classes combined
	- could be the complete behaviour of a major feature 
- naming conventions 
	-  code is allowed but not recommended 
	- use clear and concise natural language 

## control flow:
- edges between actions the direction of control flow 
- once an action is ended the outgoing edge is followed 
- there is an exception with guards, the edge is followed if only the guard evaluates to true 


## decision and merge nodes:
they allow splitting and later merging control flow
mutually exclusive guards decice which branchs to follow 

you can add a decision input text for more complex splits 
![[Pasted image 20250219110646.png]]

## parallelization 
they allow simultaneous active execution of paths 
synchronizing only happens when all actions on the incoming path have finished 

## partitions:
they group nodes and edges of an activity based off common properties 
they are usually roles of organisational units responsible for actions 

# more complex flow constructs
## event based actions:

![[Pasted image 20250219111204.png]]
they allow for modelling signal and time based initiation of flows 
they accept event action
these are the constructs
e is event and t is time 
## call behaviour actions:

![[Pasted image 20250219111354.png]]
different granularity of actions can be modeled by creating hierarchical relationships between activity diagrams
they include an external activity as an action 

## connectors

![[Pasted image 20250219111436.png]]
they allow us to connect different parts of the diagram together without making it overly complicated 
it is important to use unique id to avoid confusion

## object flow 

![[Pasted image 20250219111604.png]]
we are able to model data flow via object nodes

## exception handling 

![[Pasted image 20250219111734.png]]
we can handle exceptions and throw out errors when they happen 
after the error handler is finished normal operation is continued 



# questions:
1. what are object flow constructs
2. 