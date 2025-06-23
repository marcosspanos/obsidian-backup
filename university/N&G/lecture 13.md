# random questions:
what are reductions?
what the fuck is non determinism ??

# random notes:
N to a constant is still a polynomial running time 
n! factorial worse than exponential 
can check really quickly when a solution is presented to us 
verification can be done in polynomial time
if someone can solve a harder problem then this we can also solve the easier problem 
we can transform problems into other problems 
reductions relate hard problems 
might take a long time still 

to reduce a problem we need to match the answers 
whenever we have yes to one problem we must have yes to the second problem to prove they are equal 
we set minimum distance 1 so we multiply n edges by 1 so there is at most a path with weight n 

you can go from an optimization problem to a decision problem so we can reduce any kind of problem kind of 
this means that we are able to reduce from an optimisiation problem to a decision problem and then further reduce to all different kind of problems

we are still not sure which problems are just P Or NP because we havent had a proof that NP are not equal to P 

any algorithms which can be represented as N to a constant is considered a polynomial time 
2 to any power is considered an exponential 
# actual notes:
## decision problems vs search problems

decision problems have a clear yes or no answer while search problems might have a value we are looking for like a minimum or a maximum 

we can reduce from a search problem to a decision problem in polynomial time
![[Pasted image 20241211163803.png]]
type of problems 
we still are not sure about NP being a different class from P or not 

## reductions:
we transform any instance of B to some instance of A 
The transformation should be possible in polynomial time
![[Pasted image 20241211163957.png]]

harder problems require at least the same amount of time if not more amount of time to be able to solve them 
![[Pasted image 20241211164045.png]]

## NP complete problems:
![[Pasted image 20241211164228.png]]
if we are able to solve one then we are able to solve all the ones linked to it above and below because we are able to prove that we can transform one to another thus having a solution for all of them 
it is important for them to be decision problems in order to be able to do that
