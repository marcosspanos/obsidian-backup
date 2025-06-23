# principles of requirement engineering
there are 8 basic principles 
1. stakeholders 
2. problems requirements and solutions
3. value orientation
4. shared understanding
5. validation
6. evolution
7. innovation
8. systematic work 

## stakeholders and viewpoints
different viewpoints from different stakeholders must be taken into consideration


### consensus and variability:
the viewpoints of different stakeholders may conflict each other 
with requirement engineering you 
1. discover conflicts and inconsistencies
2. negotiate
3. moderate consensus finding 

## problem requirement and solutions
when there is a problem we need requirements for a system that solves the problem 

the traditional way to work was the waterfall method where all the specific requirements were complete 
this doesnt really work in most cases


requirement vs solution decisions
- solution decision inform lower level requirements
- requirements and solutions are inevitably intertwined 

documenting requirements and technical solutions separately makes sense

## value orientation:
the tradition is to always write a complete specification
but
- customers typically pay for systems not requirements
- many successful products dont have complete specification
- good re must create value
- value comes indirectly 

requirements must deliver value 
the value of a requirement is 
-  the benefit of reducing development risk 
- minus the cost of specifying the requirement

if the product is a small risk then putting small amount of time in re is fine as there is less that could go wrong
if the product is high risk then full fledged re is most times required for it to succeed

## shared understanding:
this is a basic prerequisite for successful development of a system
it is created and assured in re

## validation:
need to make sure the requirements you have are the ones the stakeholders need

## evolution:
- development cycles should be very short 1-6 weeks
- there should be requirement change management


## innovation:
- satisfying stakeholders isnt enough 
- innovative requirements are key to gain market share


## systematic work:
- requirements need to be elicited, documented validated and managed systematically 
- this also applies for agile development 
- systematic doesnt mean one size fits all 


# requirement engineering process:

## requirement specification:
- eliciation
- analysis
- documentation
- validation

## requirement managent
- prioritzation 
- change and release management
- traceability 


## no size fits all process
there are some determining factors
- can you talk to stakeholders
- customers order or development for a market

tailor the process from some main configuration options and a rich set of re practices


# ideal re process:
- strongly interactive
- close and intensive collaboration 
- short feedback cycles
- risk aware and feasability aware
- focus on establishing shared understanding 
- strives for innovation

# requirement elicitation:
this is the process of seeking capturing and consolidating requirements from available sources

- determine the stakeholders desires and needs
- elicit information from all available sources and consolidate it into well documented requirements

## information sources
- stakeholders -> direct dialogue and observation
- context 
- documetn 
- existing systems


## elicitation techniques:

| artifact based                                     | stakeholder  driven      |
| -------------------------------------------------- | ------------------------ |
| - background studies                               | interview                |
| questionaires                                      | observation              |
| storyboards                                        | group sessions workshops |
| prototypes and mockupas                            |                          |
| user feedback on review platforms and social media |                          |
|                                                    |                          |


### background studies:
- collect read and summarize documents about 
	- organisation 
	- the domain 
	- the system as is
- goal-> get the basics and prepare before meeting stakeholders
- data mining problem -> huge documentation , irrelevant details, outdated information 

### questionaires:
list of questions to selected stakeholders 
- multiple choice questions
- weighting each option 
- open question

### storyboards:
tell a story by a sequence of snapshots
- a snapshot is a sentence sketch or a picture

the goal is to make sure all stakeholders are on the main page regarding to the product vision and main use cases


### prototype mockups

the goal is to check requirement adequacy from direct user feedback by showing a reduced sketch of software to be in action

#### paper prototypes:
- lightweight
- easy to make
- print out available 

#### mockups
- done digitally 
- higher fidelity than prototypes


### interview:
1. select stakeholders specifically for information to be acquired
2. prepare questions in advance
3. organise meetings
4. write report from interview transcripts
5. submit reports


there are different types of interviews
1. structured interviews
2. unstructured interviews
3. semi structured interviews




# documenting with models:
## uml 
not tied to any software process
general purpose
different representations


### use case diagrams:
- express the expectation of stakeholders
- answers what is being described
	- who interacts with the system 
	- what can the actors do 
- describes functionality expected from the system


there are actors who interact with the system 
there is a relationship between use cases and actors

#### description of use cases:
structured approach 
- name 
- short description 
- preconditiobn
- post condition
- error situations
- system state
- actors that communicate with use case
- trigger events
- standard process

### class diagrams:
most popular form of structure modelling and uml model 
#### class
- construction plan for a set of similar objects of a system 
- can characterize person things or event abstract concepts such as groups 

### binary association:
connects two instances of classes to each other

#### aggregation
- special form of association
- used to express a class is part of another class
- it is transitive and assymetric 
- there is shared aggregation and composition

**shared aggregation**
	expresses a weak belonging to of the parts of a whole 
	parts also exist independently of the whole 


**composition**
- existence depends on composite objects and its parts
- one part can only be contained in at most one composite object at a time

## state machine diagrams:
every object has a finite set of different states during its life 
state machine diagrams are used 
- model these different states at a given time
- reason on the complexity of your system
- avoid overlooking important requirements related to the system behaviour


### concrete state
![[Pasted image 20250323182622.png]]
### abstract state
- arbitrarily defined set of logical states
- goal -> to define the abstract state space of objects to better reason on the system and construct a clean solution


#### state:
- nodes of the state machine
- when a state is active the machine is in that state


#### transition
change from one state to another

event
	can trigger a state transition

guard (condition)
	boolean expression
	if the event occurs the guard is checked 

		
internal transition:
