# random variables:
[[definitions statistical methods#^8e1cc0]]
these are the results we get from random experiments

there are different types of random variables 
1. discrete random variables 
2. continuous random variables

the difference between discrete and continuous random variables is that discrete random variables have a countable range while continuous random variables have an uncountable range 

# probability mass function:
[[definitions statistical methods#^218c37]]
## properties of pmf:
![[Pasted image 20241102230305.png]]

# factorials and binomial coefficients:
[[definitions statistical methods#^628a61]]

# independent random variables:
[[definitions statistical methods#^0c50a9]]
- the concept of random variables is similar to random events 
- A and B are independent if P(A,B) = P(A)P(B)

two random variables are independent if knowing the value of one does not change the value of another one 

# special distributions:
these are distributions which are used again and again in practice
it is important to understand the random experiment for each of the special distribution 

## bernouli distribution:
[[definitions statistical methods#^ce13a9|bernouli distribution]]
- random variable which can take two possible values of 0 and 1
- used to model random experiments which have only 2 outcomes often referred as success or failure 

## geometric distribution:
[[definitions statistical methods#^0b67a2|geometric distribution]]
**need to take some more notes on this **

## binomial distribution:
[[definitions statistical methods#^aa6189|binomial distribution]]
- a binomial distribution can be obtained by n independent coin tosses
- if each coin toss is a bernouli distribution then the binomial distribution is the sum of the n independent bernouli random variables

### lemma:
if X1, X2... are independent Bernouli random variables then the random variable defined as X = X1 + X2 ... has the binomial distribution

## negative binomial distribution:
[[definitions statistical methods#^aa6189|negative binomial distribution]]

- generalization of the geometric distribution
- relates to the random experiment of repeated independent trials until observing m successes 
## poisson distribution:
[[definitions statistical methods#^12e596|poisson distribution]]
- very widely used in statistics
- used in counting the occurences of certain events in an interval of time and space

the poisson distribution can be viewed as an approximation of the binomial distribution 
this is useful because the poisson distribution is much easier to calculate than the poisson distribution

![[Pasted image 20241103112951.png]]

# cdf:
[[definitions statistical methods#^c07a64|cdf]]
this can be applied to both discrete random variables but also continuous random variables 

- cdf is always a non decreasing function 
- ![[Pasted image 20241103113256.png]]
- CDF is right continuous 

# expectation:
[[definitions statistical methods#^7e2588|expectation]]
expectation is defined as the weighted average of the values in the range
it is denoted as E(X)

## expectation for special distributions:
![[Pasted image 20241103114251.png]]

## expectation is a linear operation:
![[Pasted image 20241103114321.png]]


# law of unscoscious statistician:
![[Pasted image 20241103114921.png]]

# variance:
[[definitions statistical methods#^c004db|variance]]
![[Pasted image 20241103144016.png]]

# standard deviation:
[[definitions statistical methods#^d95afc|standard deviation]]
![[Pasted image 20241103144111.png]]

![[Pasted image 20241103144129.png]]
