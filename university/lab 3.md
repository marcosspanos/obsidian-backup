# object orientation
best practices
- encapsulation
- immutability 
- reduced complexity 

## encapsulation
it conceals the attributes in the class to prevent the data from being accessed by other parts of the system
prevents references escape

## immutability 
- not possible to change the internal state of an object after internalization instead a new object is created

## reduced complexity
- classes should have a single responsibility 
- methods should only do one thing
- minimise the depth of inheritance hierarachies

# activity diagrams:
- describe procedural processing of a system
- model the system behaviour in terms of control and data flow

## activities:
- specifies user defined behaviour
- a directed graph where nodes are behavioural components and edges represent flow
- there is a clear start and end 

## actions:
- basic elements of an activity 
	- naming conventions 

## control flow:
- edges between actions specify the direction of control flow 
- once the action is ended and if available the guard on the edge evaluates to true the outgoing edge is followed


## partitions/ exception handling
- partitions group nodes and edges of an activity based on common properties
- exception handling models how to handle specific types of errors
- interruptible regions are used to terminate a flow when a specified event occurs

# decision nodes:
the if else statement is the most basic way of controlling the flow of the code
