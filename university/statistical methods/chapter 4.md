# continuous variables:
A random variable with CDF F(x) is said to be continuous if Fx(X) is continuous. This is also consistent that any particular value has a 0 percent chance of being selected

- A random variable is continuous if Rx is not countable
- If X is continuous this does not mean that s-> X(s) is also continuous 

CDF can still work for continuous variables but PMF does not work and instead we must use a PDF (Probability Density Function) 
[[definitions statistical methods^PDF|PDF]]
> From the CDF we can get the PDF and vice versa 


## properties of PDF:
![[Pasted image 20241108155235.png]]

## range:
> Range of a random variable is all the possible values of the random variable 
> For a continuous variable it is the set of all real number with non zero PDF 


## expected value and variance:
[[definitions statistical methods#^c4e897|expected value and variance]]

## law of unconscious statistician:
![[Pasted image 20241108171110.png]]


# discrete vs continuous variables:
![[Pasted image 20241108171141.png]]

# functions of continuous variables:
if X is a continuous random variable then Y = G(X) is also a continuous random variable since 
# distributions:
## uniform distribution:
[[definitions statistical methods#^0913f5|uniform distribution]]
### cdf/variance and expectation
![[Pasted image 20241108215028.png]]

## exponential distribution:
[[definitions statistical methods#^a4bd57|exponential distribution]]
### cdf/expectation/variance 
![[Pasted image 20241108215119.png]]

> the exponential distribution can  be viewed as the continuous analogue of the geometric distribution
> assume that the probability of an event l(Ik) for some l > 0 


## exponential distribution:
[[definitions statistical methods#^a4bd57|exponential distribution]]

this is a memoryless distribution which means that the time for it if its 0 or a has the same probability 

## normal distribution:
[[definitions statistical methods#^06343e|normal gaussian distribution]]
- most important distribution we have seen so far 
- important for the central limit theorem later on
- you can get other normal variables by shifting and scaling the standard normal variable 

> The integral in the CDF does not have a closed form ==(what does this mean)==

![[Pasted image 20241109112639.png]]

from a standard normal variable we can obtain any normal variable by shifting and scaling the standard variable 

![[Pasted image 20241109112806.png]]
what are m and s^2

![[Pasted image 20241109112923.png]]

- an important property is that a linear transformation of a random variable is itself a normal random variable 

 this leads us to the following theorem:
 
![[Pasted image 20241109113226.png]]

## questions 
1. what is m and s squared for normal distribution(understand it in detail)
2. what does the last theorem mean 
3. 