# complexity:
anything related to the structure of a software system that makes it hard to understand and modify the system
complexity also works in terms of cost and benefit
a complex system it takes a lot of work to implement even small improvements
## symptoms of complexity:
- change amplification
	- a seemingly simple change might require many code modifications in many different places 
- cognitive load
	- this refers to how much a developer needs to know in order to complete a task. A higher cognitive task means that a developer needs to know more to complete it and it also means there is a higher chance of bugs being present. Cognitive load is not related to how many lines the code is because fewer lines of code might not mean the code is less complex but it might mean it is more complex than code with more lines which accomplishes the same
- unkwown unwkowns
	- it might not be obvious which part of code needs to be modified to complete a task, this is the worst because there is something you need to know to complete the task but there is no way for you to know that piece of information 

one of the most important goals of good design is for a system to be obvious 

## causes of complexity:
it is caused by 2 things 
1. dependencies
	1. this exists when a given piece of code cannot be understood or modified in isolation
	2. dependencies are a fundemental part of software design and cant be eliminated
2. obscurity 
	1. this occurs when important information is not obvious. simple examples are when variables do not have descriptive names and are not clear what they do 
	2. obscurity often comes about because of not adequate documentation 

## complexity is incremental:
complexity isnt caused by a single chunk of code but instead it builds up over time with a lot of small chunks 
