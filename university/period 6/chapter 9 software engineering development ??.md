# testing

testing simulates user input with automated tests 

if your program does what is expected then the program behaves correctly 
if they do not match there are certain scenarios to check why 
1. programming errors
2. understanding errors

in both scenarios the code needs to change to address bugs or errors the tests have identified 


## types of testing
1. functional testing
2. user testing
	1. usability testing
	2. utility testing
	3. user interface testing
3. performance and load testing
4. security testing 


there are 2 phases for user testing
1. alpha testing, users are involved with developers to test which features are useful and which are not needed afterall 
2. beta testing. most of the features are done and this is more involved in polishing the user experience for users of different operational environments


# test automation:
the idea behind this is that tests should be executable 
you create and run tests and if they pass your code is fit for production

the test pyramid
![[Pasted image 20250616172553.png]]

users access gui most often but that is expensive to test
the best way is to create an api to instead check whether the api is able to complete what you need


# test driven development
this is an approach based on the idea that you should write executable tests before writing the code 

## benefits
1. systematic approach to testing. you are confident that the tests cover all the code and there are no untested code sections
2. the tests act as a written specification for program code. you can understand what the code is doing by reading tests 
3. debugging is simplified because when code failure is observed you can check what test failed 
4. leads to simpler code as programmers only need to pass tests and not create features which are not required


# security testing:
it aims to find vulnerabilities an attacker could use to gain access to the system 

this is much harder than finding bugs because of three reasons
1. you are testing for something the software should not do so there are many possibilities
2. they are obscure and hidden in rarely used code 
3. software products depend on a software stack, they may contain vulnerabilities but also they may change how they work so a vulnerability might appear when you utilise a new version


# code reviews:
there are major limitations of testing
1. you can only test code against your understanding. 
2. tests are sometimes hard to design and do not cover the entirety of the code 
3. testing doesnt infer anything about other attributes such are readability or structure


to reduce these effects you can put all code through code review before tests

these involve one or more reviewing the code to check for strange behaviour 

![[Pasted image 20250616174442.png]]