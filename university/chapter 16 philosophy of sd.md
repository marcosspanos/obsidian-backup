# strategic design 
when developers need to change code for a system they have not designed they try to make the smallest possible change that would allow the code to still work. 
ideally when you are finished with the code the system should have a structure it would have if you had designed it from the start 

if youre not making the design better you are probably making it worse

# maintaining comments
to ensure comments get updated you should position them close to the code they describe

## avoid duplication:
try to document each design decision exactly 
find the most obvious single place to put the documentation 

if information is documented outside of your program just reference to the information and do not write it again from scratch

## higher level comments are easier to maintain
if comments are more high level then small changes to the code will not change what the comment describes
comments which are not describing exactly what the code is doing are also better for clarity because they are not duplicating the code

