# singleton:
- avoids the creation of new object, it reuses the one already created instead
- accomplished by making the constructor private and exposing a static method instead
- controls the instantiation of a class
- public static method getInstance calls the actual constructor only if there is no instance already created
- else the reference to the previous instance is returned
- all the clients reference the same unique instance of the singleton class

## use cases:
- logger
- configuration manager
- handling files
- database connections

## results
### pro
- guarantees only one instance may exist
- provides singular access point
- lazy initialized

### cons
- global states lead to tight coupling
- challenging to create isolated tests
- thread safety is hard
- overuse leads to project inflexibility and therefore difficulty extending modifying systems


# factory method:
- generate different objects at runtime based on values it will acquire
- factory will generate an instance of an object belonging to the same superclass 
- we want to add logic before the object creation itself

![[Pasted image 20250325163918.png]]

# iterator:
provides a way to access elements of a collection sequentially without exposing collection representations
- decouples client code from collection structure

## components:
- iterator interface
- concrete iterators
- concrete collection
- concrete iterator 
- client

## use cases:
- simplifying the interface for a complicated data structure
- forcing custom ordering for lists/arrays
- parsing or tokenization

## results
### pros:
- encapsulates traversal logic promoting separation of concerns
- may provide uniform api for accessing elements across different location kinds
### cons:
- increased complexity. custom new iterators -> new complexity 
- performance overhead. indirect element access will cost
- makes sense only for specific kinds
- iterator invalidation


# decorator:
- we can wrap the base objects in decorators
- each new decorator will wrap the previous object
		- when executed the outer decorator will be executed as well as the inner decorator/objects

