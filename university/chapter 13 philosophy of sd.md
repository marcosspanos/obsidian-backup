# comments
comments should describe things that arent obvious from the code
developers should be able to understand the abstraction provided by a module without reading any code other than its externally visible declarations

## pick conventions
conventions ensure consistency. they also ensure you write comments 
there are some major categories of comments:
1. interface
	- comment block that immediately precedes the declaration of a module. 
2. data structure member:
	1. comment next to the declaration of a field in a data structure 
3. implementation comment
	1. comment inside the code of a method or funciton 
4. cross module comment
	1. comment describing dependencies that cross module boundaries

## dont repeat code
comments which repeat the code are not useful 
the information can be provided by the code itself

to write good code you should use different words in the comment from the ones used for the entity 

## lower level comments add precision
comments augment the code by providing information at a different level of detail 
lower level comments add precision on what exactly is happening to the code 
when documenting a variable think nouns and not verbs

