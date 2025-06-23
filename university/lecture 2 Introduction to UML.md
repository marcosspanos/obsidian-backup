#software-design #lecture2
# uml:
they merged a bunch of different languages together to on e

- not tied down to any development processes 
- can be used in the whole life cycle 
- very scalable 
- different representations
- general purpose modelling language
- very comprehensive 
- suppports both descriptive and prescriptive models 
![[Pasted image 20250215142532.png]]
this is an example of uml model represented by diagrams

there are 2 types of uml diagrams:
1. structure
	1. emphasize the static description of the elements of the system to be modelled 
	2. structural elements may have an associated behavior 
2. behavior
	- the direct consequence of an action of at least one object
	- affects how the states of objects change over time
	- can be specified through the actions of a single object 

models != diagrams
uml models contain everything related to your system 
diagrams are just windows on your model 
- can be considered projections of the model 
- one diagram will show you some parts of the model but not everything(abstraction)


## class diagrams:
1. name 
2. attributes
3. methods/operations

![[Pasted image 20250211155200.png]]

the beginning of an attribute is who can access it (+,-,· and other)
a language can be specified for uml which allows us to use datastructures inherent in that language and not only use the 4 data types of uml
## parameters:
there is direction in parameters
out means after the operation is executed the parameter changed 

when something is underlined in uml it needs to be static 

## relationships between classes:
1. generalisation(inheritance, abstract)
2. aggregation 
3. association

|Feature|Association|Generalization|Dependency|
|---|---|---|---|
|Meaning|Relationship between objects|"Is-a" relationship (inheritance)|Temporary reliance on another class|
|Direction|Can be bidirectional|Always from subclass to superclass|Always unidirectional|
|Strength|Strong (objects are connected)|Very strong (inheritance)|Weak (only a temporary connection)|
|UML Notation|Solid line|Solid line with a triangle|Dashed line with an open arrow|

### binary associations:
connect 2 classes together 
give an association name
![[Pasted image 20250211160741.png]]
navigability-> an object knows its partner object and therefore can access their visible attributes and operations 
indicated by open arrow head

multiplicity:
number of objects that may be associated with exactly with one object of the opposite side 

role:
describes the way in which an object is involved in an associated relationship 

2 or more classes can be involved at once 
### association class:
assign attributes to the relationship between classes rather than the class itself 
mandatory when n to m relationships -> otherwise cant specify relationships
why is that the case ??
## aggregation:
weak belonging of the parts to the whole 
one element can be part of multiple other elements 
![[Pasted image 20250211162759.png]]

# package diagrams:
this is a way to organise classes 
they display packages that group model elements 
can be used for grouping various models or model elements

## notation:
![[Pasted image 20250215143538.png]]

## importing:
- use import connectors to indicate the functionality is used in other packages 
- import is possible for packages or individual classes

## goals of packaging:
1. improve reasoning
2. isolate change
## approach for packaging
1. package by layer
2. package by feature

### by layer:
this organises layers according to the types of classes and the ==technical responsibilty== 
this is easy to understand and easy to navigate
not good for isolating change-> a change somewhere will cause changes in other layers most likely

### by feature:
organise packages by their ==domain related functionality== 
very good at isolating change
hard to understand unless you are knowleadgable about the field 
advised for larger projects