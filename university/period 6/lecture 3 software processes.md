# software testing:
this is a process where you execute the program using data that simulates user input

## types of testing:
- functional testing 
- user testing
- performance and load testing
- security testing

### functional testing
- unit testing -> test program units in isolation 
- feature testing -> program units are integrated to create features
- system testing -> code units are integrated to create a working version of the system 
- release testing -> packaged for release

### black box and white box
black box
- equivalence partitioning
- boundary analysis 

this involves the identification of sets of inputs 

white box
- statement coverage testing
- branch coverage testing

the statement coverage means that all the executable statements in the source code are executed at least once


### test automation:
automated testing is based on the idea that tests should be executable 

this includes the input data to the unit that is being tested, the expected result and a check that the unit returns the expected result 

if the test returns the expected value then it passes

arrange 
set up the system to run the test

action 
call the unit test that is being tested with test parameters

assert
assert what the value should be if the test is being executed correctly 

### test driven development 
the system should have 
- identify partial implementation 
- write mini unit tests
- write an incomplete code that will fail tests
- run all existing automated tests
- implement code that should cause the failing test to pass
- rerun all automated tests 

