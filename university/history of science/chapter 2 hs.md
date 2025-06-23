## supercomputer:
the supercomputer was defined by the cray 1 which was delivered to the los alamos laboratory
it was a million times more powerful than the eniac 
a lot of the features of common computers today originated in supercomputers from that era because the features eventually became commonplace enough to be used by everyone 

## first scientific computers:
the 701 from ibm was the first scientific computer 
nearly all of the computers of this model built were installed in the defense department 

the successor to the 701 was the 704 
it introduced a few major improvements 
1. core memory 
2. hardware support for floating point numbers
3. three index registers

## core memory vs delay lines:
cores can be made small 
they are non volatile 
they also provide random access taking a consistent amount to access a word from memory 

# interrupts:
when the tape drive was done it would ask the processor to interrupt the program and go to a subroutine which would handle the situation 

# scientific programming tools:
## compilers:
while assemblers made writing code faster and more convinient compilers could translate mathematical equations and easy to understand code written in high level languages into code that the computer could execute

the early compilers were written in univac software 
grace hopper defined compilers as program making routine which produced a specific program for a particular problem
the first system to operate in the sense of a modern compiler was developed by J H laning and N Zierler for whirlind computer in the early 50's 

## fortran:
this was introduced in the 1950 for the 704 
fortran was partially successful because the symbols it used were similar to the ones used in algebra 
it was also very fast as the compiler produced code that was as fast and efficient as code written by people

# SHARE:
the customers of IBM computers started sharing code they had developed for trivial tasks in order to make their lives easier, this grew and eventually reached all of the users who had an IBM system 
this is similar to how a lot of open source projects are operating now 
share was important in shaping how the modern operating system software would look like 
the first utility programs to remain in memory were called monitors 
when one program finished the monitor triggered code to load the next without waiting for a human to intervene 

## first operating system:
this was called SOS (share operating system) 
this provided batch control output buffering and a large number of input and output subroutines packaged as microinstructions 

eventually IBM took up the task of making the operating system in order to have something to give to its customers 

# compiler evolution:
it was important to develop a compiler which would give detailed error diagnostics so students would be able to use fortran as well 
this was developed in waterloo university in 1965 and it was called WATFOR waterloo fortran 
they were widely used in other universities as well 

hand calculation methods were implemented in computers which was inefficient since the methods were inefficient 
this was followed by a push to standardize and provide more efficient algorithms for calculating common problems in the form of eispack which was an early project aimed to solve this
## challenges
1. getting the routines to run effectively on different computer architectures 

# algol 
this was a hugely influential programming language 
the greatest influence was on computing research 
it began to crystalise the computer science academic discipline, many of the people who worked on it won the turing award as well as becoming celebrated computer scientists 

there were many hard to implement features inside of algol 
1. procedures 
2. block based refinement of the subroutine
3. procedures could be nested inside other procedures 
4. variables inside procedures or within other blocks
5. recursion

## stacks:
they were implemented to deposit new information on the top of the stack and if a procedure deposited variables on the stack it would be automatically removed once the procedure was done. 

all ibm computes were evolved from the 704 which was created before high level languages were developed 
implementing the stack on them was clumsy since they needed to map the virtual stack on onto the architecture of addressable memory registers and accumulators 
this slowed the computer down significantly 

the burrough corporation designed the burroughs 5000 which was the first to be created with high level languages in mind 
the operating system was written in a specially extended version of Algol 
All variable storage centered on the stack 
subroutine calls could be handle quickly and effectively 
its machines were never mainstream but its ideas were important for the future of computers
# towards the supercomputer
the transistor could serve the same role as the vacuum tubes in digital logic 
they were smaller more reliable and initally more expensive 

the surface barrier transistor was invented by Philco which could make it in quantity and performed well 
it built a computer based off the univac 1103 which was called solo and was probably the first computer to use transistors to operate in the us 
this was the beginning of the second generation of computers 

## computing at nasa ames:
the computing demands for nasa during the 1960 were never ending, this was the space race so more and more computing power was needed to provide the calculations required for flight simulations as well as testing new components?


# ibm stretch:
ibm lost to univac on a contract to build a high performance computer and to not lose its scientific lead it built a machine named stretch which would provide 100 times the power of the 704 
even though using transistors provided a significant power increase it was not enough 
another tactic they used was instruction pipelining which would become standard for all processors

stretch supported multiprogramming which means that if a program was waiting for peripherals the processor would start working on another program 
to prevent overwritting data it added memory protection 

## virtual memory and the atlas:
Atlas was able to use virtual memory which meant when a word of data wasnt used it could be swapped to disk storage so it could free that word for the computer to use. optimizing which words were swapped was crucial because if it needed to recall a word from disk memory it would slow down the computer

## control data 6600:
