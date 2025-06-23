# machine learning:

## why machine learning 
machine learning is useful when business logic becomes too comlex to maintain by hand 

## from data to models:
### training;
they use a large dataset of input and output examples to teach the model 

- the model then is able to learn to map x -> y 

even if we dont know what x and y are

## model shapes
- decision tree
- complex neural network

## difficulties:
models decay
models need to be updated with new data to maintain their efficiency 


debugging a prediction is hard 

# ml ops
they are set of practices tools and principles for managing the end to end life cycle of the machine learning systems 

## automation

we have
- continuous integration 
- continuous delivery 

there is also 
continuous training which is unique to mlops
- automatically retraining the model on new data 

## versioning 
- code 
	- the code used for data processing feature engineering and model training 
- data 
	- keep track of the dataset for training 
- models 
	- save different versions of your trained models 


## data versioning - feature stores
- offline/ online consistency 
- reproducibilyt 
- discoverability and reuse 

## model registers
- centralized repository -> there is one shared truth for all models
- lineage -> track iterations of a model 
- experimentation -> test different models in production


in mlops collaboration is core to workflow 

![[Pasted image 20250619165810.png]]
