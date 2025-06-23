# statistics:
we can use statistics to 
> -> predict outcome of an election
> -> decide whether medical treatment is effective
> -> recover a signal disturbed by noise 
> -> predict the weather 

## statistical interference:
collection of methods which deal with drawing conclusions from data which are prone to random variation
## statistical model:
view data as realisation of random variables 
### central idea:
gives the probability under which we assume the data has been generated 
typically this model contains parameters 

## approaches:
1. frequentist approach : parameters are considered fixed quantities 
2. bayesian approach : parameters are assigned a probability distribution that quantifies information we have about them 
## random sample:
the collection of random variables is said to be a random sample of size n if they are independent and identically distributed (i.i.d)
## point estimator:
this is a function of a random sample which 

### evaluating a point estimator:
![[Pasted image 20241118160107.png]]

### properties of a point estimator:
![[Pasted image 20241118160138.png]]
### estimators of mean and variance :
![[Pasted image 20241118160205.png]]
## constructing estimators:
To construct an estimator we need simple settings and only then we can come with a scenario for an estimator 
**general guidelines for creating an estimator**
- input: statistical method
- output: estimator
- ideally construct estimators using  small mean squared error 
- maximum likelihood is a way to create good estimators
- Bayesian statistics can do the same 


## maximum likelihood:
![[Pasted image 20241124135050.png]]

# statistics part 2:
## confidence intervals:
a confidence level in statistics is a type of estimate computed from the observed data 
This gives a range of values for an unwkown parameter
![[Pasted image 20241124135548.png]]
we try to find intervals of small ranges which allows us to have a better chance of being closer to the actual value using an estimator 

### example for constructing an interval estimator:
![[Pasted image 20241124135920.png]]

**interpretation**
$\theta$ is either in or out 
if we repeatedly create CI then in a (1-a)100% of the cases will be in (??) 
### pivots:
the random variable Q is said to be a pivot or pivotal quantity if it has the following properties
## hypothesis testing:
statistical method for testing hypothesis about a parameter
- for testing the population mean when the standard deviation is known 
	![[Pasted image 20241224214702.png]]
- for testing when the population mean is uknwown which is most of the time
	![[Pasted image 20241224214743.png]]

## steps in hypothesis testing:
1. state null hypothesis Ho and alternative hypothesis Ha 
2. choose significance level 
3. compute test statistic 
4. determine the critical value or p value 
5. make decision- reject if h0 fails or accept it


# interval estimation:
A confidence interval provides a range of values which the true population parameter is expected to lie within with some confidence level 
