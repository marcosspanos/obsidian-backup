# activity diagrams:
they specify the control flow and the data flow between various steps -> the actions required to implement an activity 

## activities:
they allow to specify user defined behavior in the form of activities
an activity can describe the implementation of a use case
the content of an activity is a directed graph whose nodes represent the components of the activity 

you can specify preconditions and post conditions for an activity 
they need to be fulfilled before or after an activity 



## actions:
they are the basic elements of activities
they are represented with a rectangle with rounded edges
they process input values to produce output values. 
actions and parameters are connected using directed edges

### event based actions:
they enable objects and signals to be transmitted to receiver objects 

you can use accept ewvent action to model for an action that waits for the occurence of a specific event

![[Pasted image 20250224173131.png]]

### call behavior actions
![[Pasted image 20250224173202.png]]
actions can call activities themselves 
they are referred as call behaviour actions 

## control flows:
to show how execution goes we need execution semantics to specify how the activity diagram flows. 

there are guard which are specified in square brackets. they need to be true for the condition which follows to run 

## object flow:
they are similar to control tokens
we never show them in the diagram but we know they are there 
### object nodes:
![[Pasted image 20250224174721.png]]
they contain the name of the object they represent


### pins:
![[Pasted image 20250224174816.png]]

they are used to represent objects that serve as input and output for actions 

## partitions:
![[Pasted image 20250224174911.png]]

they allow grouping of nodes and edges to an activity based on common properties


## exception handling:
![[Pasted image 20250224175010.png]]

they are activated when there is a specific error to prevent undefined behaviour 
the sequence continues normally after the exception as if the defective action had ended normally 
