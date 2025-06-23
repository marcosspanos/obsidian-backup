# code management
its a set of software supported practices to manage an evolving database 

code managent tools make it easy to create an executable product from source files 


## fundementals of source code management
source code management is designed to manage an evolving project codebase 
developers can work in parallel without interfering with each other

featueres
1. code transfer. 
2. version control and retrieval 
3. merging and branching 
4. version information


when new files are added the vcs assigns a unique identifier to the file 
any version of a file can be retrieved from the system 

when many people are working on the same file the version control system handles merging the committed files together at the end

in the past when storage costs were expensive only the new code was stored
now that storage is cheap and plentiful modern code management dont optimise for stora anymore 



## git
in git a fundemental concept is the master branch 

you create new versions by creating a new branch 

distributed code management tools have a few advantages over centralized tools
1. resilience
2. speed
3. flexibility


## why use git
when working on a project which uses git you can set up a workspace on your laptop by cloning the latest versions 

when you do you can start working on the files and changing them 
to add to the files in the project you can commit to the cloud


### branching/merging

a branch is an independent stand alone version that is created when a developer wants to change a file

the repository ensures no files can be overwritten without a merge operation

git compares files line by line
if 2 users committed the same file but were working on differnet lines then there is no problem 
if they did work on the same lines then they need to resolve these conflicts


![[Pasted image 20250616185309.png]]


# dev ops automation 10.2 
a fundemental princinple of devops is that anything that can be automated should be 

automation of issue tracking is also important 
there are several open source tools which are used for issue tracking such as 
bugzilla fogbugz and jira

they include 
1. issue reporting
2. searching and querying
3. data analysis
4. integration with source code management

## continuous integration:
system building is the process of gathering all the elements required in a working system and moving them together to create an operational system 

there are certain activities which are common
- installing database software 
- loading test data into the database
- compiling the files that make up the product 
- checking that external services used are operational 
- running a set of system checks to test that the integration has been successful 


continuous integration means that any bugs which are caused by outside systems are found quickly 


continuously integrating means that a working system is always available for the team 

continuous development is only effective if there is constant integration of new code 

### dependencies
a dependency model that shows which dependencies are required to execute
