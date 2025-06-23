# object oriented design patters:
- singleton
- factory method
- iterator
- decorator 
- observer

## design pattern:
this is a template on how to solve a problem 
it can be used in many different situations


in 1994 4 ibm programmers observed and documented 23 problems and their best accepted solutions
### types of design patterns:
- creational 
	- how objects can be created
	- control 
	- extensibility 
- structural 
	- how to form larger structures 
- behavioural 
	- how responsibilities can be assigned to objects

### singleton:
a class for which only a single instance can exist in the system at any one time 

![[Pasted image 20250304173906.png]]

### factory method:
creates an object without hardcoding its type in the code??
![[Pasted image 20250304174231.png]]
### decorator:
adds responsibilities to objects dynamically
![[Pasted image 20250304174359.png]]

### iterator:
sequentially accesses the elements of a collection

![[Pasted image 20250304174319.png]]

### observer
a way of notifying change to a number of classes
![[Pasted image 20250304174416.png]]

## essential patterns of design pattern
- pattern name
	- provides a common vocabulary for software designers
- intent
	- what does the pattern do 
	- what is the rationale and intent
	- what particular design issue or problem does it address
- solution
	- the basic element providing the solution to the problem in terms of
		1. structure
		2. participants
		3. collaborators
- consequences
	- what are the results and trade offs by applying the design pattern



# additional notes:
https://www.geeksforgeeks.org/singleton-design-pattern/?ref=lbp
## singleton:
it is used to ensure that there is only one instance of a class throughout the application at one time
it can prevent multiple threads from creating separate instances simultaneously
it can also restrict direct instantatiation by making the constructor private

## decorator:
allows behaviour to be added to individual objects dynamically
it involves creating a set of decorator classes which are used to wrap concrete components
they are a structural design pattern used in software development
it is useful when you need to add functionality to objects in flexible and reusable ways

they promote flexibility and extensibility in software 
it follows the open closed principle meaning new decorators can be added without modifying existing code
it is commonly used in scenarios where a variety of optional features or behaviors need to be added in object in a flexible and reusable manner.
**use cases**
extending functionality
multiple combinations of features
legacy code integration
gui components
input/output streams

### code:
1. components interface
		this is the interface representing the component
2. concretecomponent
		this is the concrete class implementing the interface
		it provides the description 
3. decorator
		this is an abstract class implementing the interface
		it maintains a reference to the decorated object
		the methods are implemented to delegate the decorated object
4. concretedecorators
		these are concrete decorators extending the part above
		they override to add the respective decorator desc

## observer 
it establishes a one to many dependency between objects 
when one object changes state all its dependent are notified and updated automatically 
it deals with how the interaction and communication between objects, specifically on how objects behave in response to changes in the state of other objects

### 
- defines how a group of objects interact based on changes in the state of a subject
- observes react to change in the subjects state
- the subject doesnt need to know the specific classes of its observers allowing for flexibilty
- observers can easily be added or removed without affecting the subject

### components of observer design patterns
- subjects
	- the subject maintains a list of observers
	- it provides methods to register and unregister observers dynamically and defines a method to notifyu observers of changes in its state
- observer
	- observer defines an interface with an update method that concrete observers must implemewtn and ensures a common or consistent way for concrete observers to receive updates from the subject
- concretesubject
	- concrete subjects are specific implementation of the subject. they hold the actual state or data that observers want to track. when this state changes concrete subjects notify their observerss
- concrete observer
	- implements the observer interface. they register with a concrete subject and react when notified of a state change
	- when the subjects state changes the concrete observers update method is invoked allowing it to take appropriate actions
	- 

## factory:
it is a creational design pattern used in software development. it provides an interface for creating objects in a superclass while allowing subclasses to specify the types of objects they create
- this pattern simplifies the object creation process by placing it in a dedicated method 
- this approach enhances flexibility extensebility and maintainibility enabling subclasses to implement their own factory method for creating specific object types

this is similar to inheritance but there are a few key differences
### **Key Differences:**

| Feature              | **Inheritance**                                                   | **Factory Pattern**                                                     |
| -------------------- | ----------------------------------------------------------------- | ----------------------------------------------------------------------- |
| **Purpose**          | Establishes an "is-a" relationship between classes to reuse code. | Encapsulates object creation logic to provide flexibility.              |
| **How It Works**     | A subclass inherits fields and methods from a parent class.       | A factory method decides which subclass instance to return.             |
| **Code Reusability** | Improves code reuse by sharing common functionality.              | Improves reusability by centralizing object creation.                   |
| **Flexibility**      | Can lead to **tight coupling**, making changes harder.            | Promotes **loose coupling**, as object creation logic is separated.     |
| **Example**          | `class Dog extends Animal {}`                                     | `Animal animal = AnimalFactory.create("dog");`                          |
| **Object Creation**  | Objects are created using `new` directly.                         | Factory encapsulates `new`, so object types can be changed dynamically. |
| **Extensibility**    | Changes require modifying existing code.                          | Easier to add new object types without modifying existing code.         |
