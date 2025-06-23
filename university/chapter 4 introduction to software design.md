# static and dynamic perspective
there are different ways to look at the software elements
one is the static way in which we are only looking at teh source code or a class diagram 
the dynamic perspective represents all the values and references held by the variables in a program at different points in time 
to understand the software sometimes static perspective is needed while othertimes dynamic perspective is needed. Sometimes they are both needed to have a complete picture of the software


# defining object state
the state of an object refers to the particular pieces of information the object represents at a given time
there is a difference between concrete state and abstract state
the cardinality of the set of the possible concrete states is called the state space
for the deck example this explodes rapidly and there is no way to properly consider all of them 
an abstract object state is an arbitrary partion of the concrete state

# state diagrams:
they are used to represent how objects can transition from one abstract state to another 
they represent a dynamic view of the software design 
an absence of a transition means that the transition is not possible 

# designing object life cycles:
the lifetime of an object depends on the design decisions
it is important to keep the complexity of the objects as low as possible 

##
null referencing gets in the way of designing clean state spaces and life cycles

# singleton:
this ensures there is only one instance of a given class at any point 
1. private constructor 
2. global variable for holding a reference to the single interface 
3. an accessor method 

a typical mistake is to store a reference to an instance of the class in a static field called instance without taking proper care to prevent client code from independently creating new objects 
to prevent this we can the class construction private 

