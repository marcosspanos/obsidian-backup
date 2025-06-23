
/and/ 
/or
/to
/if
/iff 
/all
/ex
/fun

# examples:
any proposition can be viewed as a type 
a hypothesis or premise is just a variable of that type

building proofs is then a matter of writing down expression of the correct type 

if p is an expression of type A and B then and.left P is an expression of type A 


variables A B : Prop
variable h : A ∧ ¬ B
/# check and.intro (and.right h) (and.left h)
this essentially means the following proof 
![[Pasted image 20250411174123.png]]

this way of representing natural deduction proofs there are no free floating hypotheses 
every hypothesis has a label 

if h1 is proof of A and h2 is proof of B then and.intro h1 h2 is a proof of A and B 
for and.intro we need 2 arguments

lean adopts teh convention that application associate to the left so that expression h1 h2 h3 is interpreted as (h1 h2 ) h3

implications associate to the right so that 
A-> B ->C is interpreted as A -> (B-> C)

the implication introduction rule is the tricky one because it can cancel out a hypothesis 
Suppose A and B have Prop and assuming h is the premise that A holds P is proof of B possible

