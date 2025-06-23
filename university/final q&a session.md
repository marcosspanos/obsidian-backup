# details about exam:
## types of class diagram relationships
- association 
- aggregation
- composition
- generalization

1. is one class a specialized version of another class
	1. if so its generalisation 
2. does one class have an attribute of the other class type 
	1. no -> uses dependency 
3. is one class a part of the oether 
	1. no->association 
4. is the whole part relationship very strong(part cant exist without the other )
	1. yes composition 
	2. non aggregation

# package diagrams:
## by layer
organize packages according to the types of classes and the technical responsibility they have
## by feature
organize package according to their domain related functionality 

# design principles:
## immutability:
we do this to share information without breaking encapsulation
if a class is immutable its not a problem if its references to its objects escape
keep your objects consistent

# inversion of control:
## limitations:
- high coupling:
	- in every panel i need to remember the apis for updating the other panel 
- low extensibility 
	- adding/removing a panel -> modify all other panels
	- dependencies grow quadratically
- high complexity 
	- the code for updating a panel is also intermingled with the code for updating the other panels
## benefits:
- better separation of concerns
- loose coupling
- better extensibility 

inversion of control is a key part of what makes a library different to a framework 
## library 
- set of functions that you can call usually organised into classes
- each call does some work and returns control to the client

## framework 
- embodies some abstract design with more behaviour built in 
- in order to use it you need to insert your behaviour to various places in the framework 
- the framework codes then calls your code at those points



# design patterns:
- reusability
	- they provide proven solutions to common problems making code more reusable and reducing redundancy 
- efficiency 
	- they accelarate development by offering templates that save time and effort
- maintainability 
	- they promote best practices -> cleaner more maintainable code that is easier to understand and modify 
- communication
	- they server as a common language among developers facilitating better communication and collaboration with teams 


## factory:
![[Pasted image 20250321140712.png]]


## decorator:
- this is an instance of open closed principle
- decorators allow you to add functionality to tager class without having to modify it
- decorators usually provide the same api as the target
- they do additional work before or after forwarding the argument to the object
- 