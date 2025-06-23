# continuous integration:
whenever a change is made to the code's main branch a new executable version is deployed 


# continuous delivery and deployment
delivery -> a simulation of the products operating environment is created and the executable software version is tested

deployment-> a new release of the system is made available to users every time a change is made to the projects core repository main branch 


# github actions:

the main goal of actions is to automate software development tasks and processes

## workflow
this is a configurable automated process which runs one or more jobs
they are defined in a yml file in the repository

they are defined in the github/workflows directory in the repository 


workflows must contain
- one or more events triggering the workflow 
- one or more jobs 


## software quality checks
executability and functionality should be covered by basic checks


# new
## github actions:

the main goal is to automate software development tasks and processes


### workflow
a workflow is a configurable automated process that will run one or more jobs 
workflows are defined in a .yml file checked to your repository 


they must contain 
- events to trigger the workflow
- one or more jobs that will execute on a runner machine 
- each step can either run a script or a predefined action 

