# information hiding:
the information hidden usually consists of information implementing some mechanisms 

this reduces complexity in 2 ways
first it simplifies the interface to a module 
second this makes it easier to evolve the system 
if a piece of information is hidden there are no dependencies on that information 

# information leakage:
this occurs when a design decision is reflected in multiple modules 
this creates dependency between the modules 
this also occurs when the same knowledge is used in multiple places such as 2 different classes that both understand the format of a particular type of file 

# temporal decomposition:
here the structure of the system corresponds to the time order in which operations will occur 

this happens because we keep adding functions out of order while we are designing an app and this leads to us not realising some functions could be the same function in the end 
in temporal decomposition the execution order is reflected in the code structure 

having a slightly bigger class will make it less likely for it to have information leakage if the functions of 2 similar classes are combined 

