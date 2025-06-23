
#class-diagram #notes
# class diagram
we use this to model the static structure of a system->describing the elements of the system and the relationship between them 
the relationships do not change over time
this is the most widely used UML structure 
it is applied in various phases of the software development 
due to the simplicity and the popularity the class diagram is suitable for quick sketches 
it can also be used to generate program code automatically 

## objects:
an object has a unique identity and a number of characteristics that describe it in mode detail
usually they appear in pairs and interact with other objects
the relationship between objects is called a link 
the characteristics of an object include its structural characteristics (attributes) and behavior(form of operations/methods)

## classes:
this is a construction plan for a set of similar objects that appear in the system to be specified 
they can characterize nouns
objects represent the concrete form of classes and are referred as their instances
an attribute allows you to store information, they generally have different values for each instance


## notation:
classes are represented by rectangles that can be subdivided into smaller rectangles 
the first one must have the name of the class 
second compartment must have the attributes of a class 
the third compartment must have the operations of a class 
![[Pasted image 20250215165945.png]]
## attributes:
attributes must have a name 
the type of the attribute might be specified after the name 
to define a default value you specify =default where default is a user defined value or expression 

## multiplicities:
this indicates how many values an attribute can contain
using this we are able to define arrays 
![[Pasted image 20250215172708.png]]

## operations:
they are characterized by their name their parameters and the type of return value 

## visibility markers:
this specifies who and who isnt able to access them 
if nothing is shown then no default visibility is assumed 
this is used in information hiding to prevent unauthorized access 
access is only allowed from clearly defined interface 

## class variables and operations:
attributes are defined at an instance level 
when a class is realized in a programming language memory is reserved for all the attributes of an object
these are referred as instance variables or instance attributes
instance variables are different than class variables
class variables are only created for one class 

## associations:
they model relationships between instances of the classes

### binary associations:
this is used to associate two classes with one another 
the relationships are shown as a solid line
### n-ary associations:
if there are more than 2 objects we can use nary associations
this is represented using a hollow diamond in the center

## association classes:
this is used to assign attributes to the relationship between classes rather than the classes themselves
this is presented using a dashed line 
## aggregations:
special form of association that is used to express that the instance of one class is part at an instance at another class

### shared aggregation:
this has intentionally informal semantics

## generalisations:
we use them to highlight commonalities between classes 
we dont have to define these common characteristics multiple times 

### inheritance
generalisation is also referred as inheritance 
there is the super class and the subclass and the subclass has all of the elements of the super class
uml allows multiple inheritance meaning a class can have many superclass and inherit many attributes

## classification:
refers to instanceOf relationship between an object and a class
with multiple classification an object can be an instance of multiple classes 
here no new class in inheriting the characteristics of the superclasses involved

# abstract classes vs interfaces:
these are classes which cant be instantiated with themselves 
there are no objects for these classes only their subclass can be instantiated 
operations of abstract classes can also be labelled as abstract
they are indicated with using the keyword abstract 
this is similar to interfaces which do not have an implementation or direct instances
in contrast to a relationship between abstract class and subclasses a relationship between interface and subclasses is not necessary 
operations of interfaces never have an implementation
to denote an interface we use the word interface before the name 
# data types:
a type can be either a class or a data type 
primitive data structures do not have any internal structure 

# creating a class diagram:
there are some guidelines which allow us to create a class diagram 
nouns often indicate classes
names often indicate relationships between classes
