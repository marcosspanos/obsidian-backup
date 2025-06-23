# modular design
it is important that developers only face a small fraction of the overall complexity at any time
a software system is decomposed into a collection of modules
modules can take any form. 
In an ideal world each module would be completely independent 
this is not possible and modules must interact with other modules 
to manage dependencies we think of each module in 2 parts 
interface and implementation 
a module is a piece of code which has an interface and an implementation
each class is a module 
methods within that class can also be thought of as modules 

the best modules are the ones whose interfaces are much simpler than their implementations 

## interface:
it contains 2 kinds of information 
1. formal 
2. informal 

## abstractions:
this is a simplified view of an entity which omits unimportant details
in modular programming each module provides an abstraction in form of its interface
## deep modules:
deep modules provide powerful functionality but have simple interfaces
this is the opposite to shallow modules 

even though classes are good having a lot of classes is not good if they are shallow classes and the functionality they provide makes the overall complexity of the system worse 
it is better to have fewer deep classes instead which reduce the complexity of the system 
