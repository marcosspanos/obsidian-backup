# composition aggregation:
a common strategy is to define larger abstraction in terms of smaller ones
one way to assemble different pieces of data is through object composition 
an object stores references to one or more objects 
an example of this is a deck of cards 
the deck is composed of cards so we can make up the deck from instances of cards
another situation is when we need to break down a class that is too big and complex
in object oriented programming the easier thing to do is create a huge class with all of the attributes and methods inside it because this means we are able to communicate between all the methods (god class)
to avoid this we can use composition to support a mechanism of delegation 


one important aspect of composition is its transitive 
many structures are object graphs
in class diagrams compositions is represented with an edge decorated with a diamond. 
there is a difference between composition being black diamond and aggregation being white diamonds
# sequence diagrams:
use of composition means we have to do with how objects collaborate with each other 
it is sometimes helpful to model certain design decisions related to object call sequences
this can be done with sequence diagrams 
they represent a specific execution of the code

# decorator design pattern:
sometimes we want objects to have special behaviour 
to do this we can use a specialized class solution 
this cant be changed in runtime so it doesnt work well
a second option is to use a multi mode class
we can provide all features within one class 
this is ugly 
the decorator solves both 
## decorator:
it aggregates one object of the component interfface 
it implements the component interface. 

# combining composite and decorator
although they are distinct they can often be used together in hierarchical operations
