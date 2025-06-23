# state machine diagrams:
help think about complexity of the system
help model dynamic behaviours
there are states and transitions (the arrows)

guard is an important part of state machine diagrams

## initial state:
start state
no object can be here
there are no incoming edges for it 
it needs outgoing edges

## final state
real state
marks the end of the sequence of states
object can remain in a final state forever

## terminate note
pseudostate
terminates teh state machine
the modeled object ceases to exist

## decision nodes:
they are similar to if else statements
they can be represented in many ways with statements on transitions

## parallelization and synchronization node:
they are both pseudostates 
one splits the control flow into multiple concurrent flows while the other one merges them 
for the first one there is one incoming edge but for the second one there is only one outgoing edge

## composition state
- contains other states 
	- only one substate is active at any point in time

## orthogonal state:
- composite state is divided into two or more regions separated by a dashed line 
- one state of each region is active at any point in time
- transition to the boundary of the orthogonal state activates the initial state of all the regions
- final state must be reached in all regions to trigger completion event

