#lecture #notes 
# law of demeter
you should avoid as much as possible long chains of message calls
this leads to dependency issues 
the solution to this is to have intermediate classes. 
	the classes should be deeper and provide complete services
	they should not return references to their internal structure

the code of a method should only access 
	the instances variables of this
	the arguments of the method
	any new object created within the method


# interface segregation:
when this is not applied the client might depend on services they dont need
the code should not be forced to depend on interfaces it doesnt need to 

to prevent this we can use specialized interfaces that specify a small and coherent slice of behavior that clients can depend on 

if you notice that two interfaces are always used together then its better to merge them into a single interface


# objects identity, equality, uniqueness

- the identity of an object distinguishes one object from another 
- it is useful to think of an objects identity as the place where its value is stored



## equality;
refers to the fact that two distinct objects are semantically the same 
in general this must be defined by the programmer
### template for overriding the equals method 
![[Pasted image 20250318161431.png]]
## uniqueness:
objects of a class are unique if its not possible for two distinct objects to be equal 

# liskov substitution principle
this is a way to ensure that inheritance is used correctly
- inheritance should only be used to extend the behaviour of a superclass
- bad design to use inheritance
	- restrict the behaviour of a superclass
	- when the subclass is not a proper subtype of its superclass
- the subclass cant have
	- stricter preconditions
	- less strict postconditioin
	- take more specific types as parameters
	- throw more checked exceptions
	- less specific return type

# applying design patterns
we may encounter problems 
design patterns are not off the shelf functions we can use but we need to follow the pattern details and implement a solution 

