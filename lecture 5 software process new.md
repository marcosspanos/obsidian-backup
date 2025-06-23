# dev ops:
we have requirements and we want to get a software in production


## typical release
plan -> code -> test -> build -> deploy -> operate and monitor 

these are all steps for the initial launch 

then we can have improvements which are 
- addition of features
- bug fixes
- performance improvements


the development phase happens in the code repository and when its done the operation is passed to servers


## challenges:
1. communication and collaboration between developers and operations
- developers dont consider the deployment environment 
- operations dont know how the system works

1. conflict of interest
-  developers want to finish implementation fast
- operations want to maintain stability 

1. manual work
- manual testing
- manual release creation 
- manual deployment

# dev ops
this is a combination of cultural philosophies practices and tools 
it is about anything that makes the process of releasing software fast and high quality


different companies have different implementations of this
some companies have a separate role for this called a dev ops engineer


## benefits
- faster deployment
- reduced risk 
- faster repair 
- more productive teams

## aspects of dev ops
- continuous integration 
- continuous delivery 
- continuous deployment 

## continuous integration 
each time someone makes a change to the project core repository an executable branch is built and tested

**benefits**
- faster to find and fix bugs -> if there is a bug it was caused by this version 
- your changes are shared with the whole team 
- might create a quality culture in the development team 

## continuous delivery and deployment 
simulation of the product operating system is created and the exectuable is tested 

**benefits**
- faster customer feedback 
- faster problem solving
- reduced costs

## infrastructure as code

### characteristics
- visibility 
- reproducibility 
- reliability 
- recovery 


# agile and dev ops
agile approaches target reducing the development time
dev ops targets the challenges in the release process


