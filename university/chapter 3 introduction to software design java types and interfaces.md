#book #notes #software-design 
# decoupling behaviour from implementation:
![[Pasted image 20250305174331.png]]
in this code the methods in the class deck are coupled to the class
if we want to use any of the three methods we must use them in an instance of the class there is no other way to use them
sometimes we might want to decouple the interface of the class from the implementation 
to do this in java we use java interface types
they provide a specification of the methods that it should be possible to invoke on an object 
with interface types we can define an abstraction cardSource as any object which supports a draw() method and isEmpty() method 
to tie a class with an interface we use the ==implements== keyword
it has two related effects
1. it provides a formal guarantee that the instances of the class will have concrete implementations for all the methods of the interface type. this is enforced by the compiler
2. it creates a subtype relationship between the implementing class and the interface type. 

the subtype relation between the implementing class and the interface is what enables polymorphism 

# specifying behaviours with interface types
to sort a deck of cards using the sort algorithm wouldnt work because it doesnt know how to sort them(suit,rank)
using the comparable function we are able to tell the function to compare it against a given object 
this means it doesnt matter what the objects are as long as we are able to compare them against each other 
to declare the comparable function we must declare it with the implement function 

# class diagrams:
they represent a static view of the software system 
they are useful to represent how types are defined and related 
they are the closest diagram to code in UML

# function objects:
an interface only defines a subset of the operations of the classes that implement it 
sometimes we might want to change how we sort the cards
a way to do this would be using a global bool value and depending on what we want to do change the way the cards are sorted. 
a better way would be to use compare instead of compareTo so the class instead of having one explicit parameter now takes 2. 
An instance of Comparator is simply an object that provides the implementation for a single method 
the use of comparators introduces many interesting design questions and trade offs 
if comparator classes are defined as standalone top level java classes the code of their compare method will not have access to the private members of any objects they compare 

# iterators:
to support iteration we must have a specification of what it means to iterate . this specification is captured in an interface
the interface defines two abstract methods hasNext() and next()
to make sure we are able to iterate over any object we must create an iterable interface. This specifies the smallest slice of behavior to make it possible to iterate over an object
we can iterate objects in java using a foreach loop 

# strategy design pattern:
the use of function objects to to customise the behavior of another part of code is a general idea called strategy design patterns
the context for this is 
	define a family of algorithms, encapsulate each one and make them interchangable.
algorithms are in the same family if they implement the same interface
