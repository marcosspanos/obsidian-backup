# version control systems:
they are software tools which help software teams to keep track and manage changes to source code over time


## repositories
they are file folders which contain the projects file and each files version history

a local repository is stored on the developer computer and only the developer has access to it 


## centralized vs distributed version control systems

### distributed 
- flexibility for local work without internet connectivity 
- speed to perform commands on the repository 
- resilience to a damaged remote repository 


- if the project has a long history it might take up a lot of space on the developer computer 


## git
distributed version control system 


## git vs github 
![[Pasted image 20250613175826.png]]



# pull requests:

the main goals of pull requests are to 
- allow code review 
- perform automated checks on changes

before they are merged in the main branch 



# pull based development

this allows for external contribution to the repository 



# github actions:

they are meant to automate software development tasks and processes 

## workflow 
a workflow is a configurable automated process that will run one or more jobs

they are defined in .yml files and checked in your repository 

they are defined in the workflows directory in the repository 

### basics
they must contain
- one or more events which will trigger the workflow 
- one or more jobs which will execute on a runner machine and run a series of one or more steps
- each step can either run a script by a developer or a predefined action 


# best collaboration practices:
each commit should be an atomic message
each commit should be clear follow a pattern 


- create issues to organise small tasks
- issues should be updated/closed when resolved


# open source
## free software 

freedoms 
1. the freedom to run your program as you wishj
2. the freedom to study the program and to change it so it does your computing as you wish 
3. the freedom to redistribute copies 
4. the freedom to distribute copies of the modified version to others 


## open source 
this is a bit looser than open source
