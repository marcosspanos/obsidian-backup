#software-design #lecture1 
# object oriented programming
look at the tutorial again in lecture 

the difference between scala and java 
![[Pasted image 20250205094403.png]]
java is not purely object oriented
int float boolean are primitive 
you cant type 3.tostring because numbers are not objects

## primitive 
- have no methods
- have operators


you cant use primitive classes for generics
instead you can use wrapper classes to use primitive types
![[Pasted image 20250205094934.png]]
this is how you convert it to the wrapper class
java does some of the unboxing for you -> autoboxing 

arrays can consist of primitive types 

# equality:
if you use equality on non primitive types then equality means that if they are pointing to the same object 

to do the equality function you need to use .equal for objects as this is the way to check if 2 objects are equal 


# static members:
they are associated with the class itself not an instance of the class
![[Pasted image 20250205095408.png]]

# polymorphism:
functions can work with many different types of types
enables code reuse 

# questions
- what is abstract
- why we make different classes for everything


# lecture notes:
need to figure out how to use programs that are UML compliant and how they work

software engineering is different than programming in that software engineers need to manage large projects with millions lines of code and make sure they are operational for a long time without any downtime

- abstraction of data and computation
- the organisation of these abstractions into a working software system


>mapping features : a model is based on an original system 
reduction feature: a model only reflects a selection of the original properties
prgramatic feature: a model needs to be usable in place of the original with respect to some purpose


## modelling purposes:
- descriptive models:
	- they are used for astronomy 
	- ![[Pasted image 20250210120228.png]]
- prescriptive models:
	- they are used for electrical engineering

### descriptive models:
- sketches and throw away models
	- to better understand reality and explore possible solutions 
	- short lifetime usually
- models of ideas and vision about the system to be developed 
	- to exploit the model for having feedback before implementing a system
- models extracted from running system on source code
	- visualize all possible calls between a set of java classes


### prescriptive models:
- they guide the development of the system
	- more detailed than descriptive models 
	- specify constraints for the system 
- common consumers of prescriptive models are developers of code generators 
- prescriptive models are often used for development
	- their importance might decrease when the system is implemented

