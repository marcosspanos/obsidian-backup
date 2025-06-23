#lecture #notes 
# documenting requirements:
- communicating requirements
- having a basis for contracts and acceptance decisions


the mean to do this is documented requirements
## classic requirements specifications:

full fledged requirements specifications are typically needed when 
- customers want contractually fixed requirements costs and deadlines
- systems are built by an external contractor based on a set of given requirements
- in regulated environments where regulators check the compliance of developed systems

## requirements in agile development 
here there is no classic requirement specification 
there are various artifacts and work products which specify requirements

### specification artifacts:
requirements are primarily captured as a collection of user stories 
a system vision provides an abstract overview of the system to be developped 

## aspects to be documented
1. functionality
	- data
	- functions
	- behaviors
	- normal/abnormal cases
2. performance
	- data volume 
	- reaction time
	- processing speed
3. specific qualities
	- usability
	- reliability
	- quality
4. constraints
	- technical 
	- legal
	- cultural 
	- environmental 


# how to document:
there are 2 main ways to document
1. ieee
	- three parts
	- system requirements only 
	- representation of specific requirements tailorable 
2. volere
	- 27 chapters
	- system and project requirements

in agile you do things only if they add value 

## informally 
- natural language (narrative text)
- some problems with this is it can be vague 
	- this can be improved by using well formed natural language requirements 
	- ![[Pasted image 20250227181016.png]]
	- use active voice
	- attach a unique identifier to every requirement
## semi formally 
- structural model s
- interaction models 
## formally
formal models typically based on mathematical logic and set theory


## general rules for requirements documentaiton
- specify requirements as smal identifiable units
- record metadata
- use structure templates
- specify normal and exceptional cases

# persona:
this should paint a picture of a type of product user 
sometimes the personas will be similar if the type of users are really similar 
# scenarios:
aim is to discover product features that will tempt users to adopt the product rather than competing products

1. brief statement of the overall objective 
2. reference to the person involved 
3. information about what is involved in doing the activity 
4. description of one way the identified problem might be addressed

# documenting requirements with models:
## model based requirements specification
- requirements are described as a problem oriented model of the system to be built 
- architecture and design information is omitted 
- mostly graphical represented

## case diagrams:
these express the expectations of the stakeholders
- what is being described(the system)
- who interacts witht the system(users)
- what can actors do(the use cases)


## best practices:
who uses the main use casea
who needs support for their daily work
who is responsible for system administration
what are the external devices 
who is interested in the results of the system
what are the main tasks that an actor can perform 
does an actor want to query or even modify information contained in the system


