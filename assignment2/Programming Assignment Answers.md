## Problem 2
>Train a model with 50 dimensional embedding space, 200 dimensional hidden layer and default setting of all other hyperparameters. What is average training set cross entropy as reported by the training program after 10 epochs ? Please provide a numeric answer (three decimal places). [4 points]

Finished Training.
Final Training CE 2.536
Running validation ...
Final Validation CE 2.603
Running test ...
Final Test CE 2.612
Training took 234.48 seconds

## Problem 3
> Train a model for 10 epochs with a 50 dimensional embedding space, 200 dimensional hidden layer, a learning rate of 100.0 and default setting of all other hyperparameters. What do you observe ? [3 points]

* Cross Entropy on the validation set fluctuates around a large value.
* Cross Entropy on the training set fluctuates around a large value.

## Problem 4
If all weights and biases in this network were set to zero and no training is performed, what will be the average cross entropy on the training set ? Please provide a numeric answer (three decimal places). [3 points]

ln250 = 5.521


## Problem 5
>Train three models each with 50 dimensional embedding space, 200 dimensional hidden layer.
>
>    Model A: Learning rate = 0.001,
>    Model B: Learning rate = 0.1
>    Model C: Learning rate = 10.0.

>Use the default settings for all other hyperparameters. Which model >gives the lowest training set cross entropy after 1 epoch ? [3 >points]

#####Model A: learning rate = 0.001
Finished Training.
*Final Training CE 4.431*
Running validation ...
Final Validation CE 4.386
Running test ...
Final Test CE 4.393
Training took 25.22 seconds

#####Model B: learning rate = 0.1
Finished Training.
*Final Training CE 3.953*
Running validation ...
Final Validation CE 3.300
Running test ...
Final Test CE 3.300
Training took 24.97 seconds

#####Model C: learning rate = 10.0
Finished Training.
*Final Training CE 4.701*
Running validation ...
Final Validation CE 4.662
Running test ...
Final Test CE 4.668
Training took 24.83 seconds


##Problem 6
>In the models trained in Question 5, which one gives the lowest training set cross entropy after 10 epochs ? [2 points]

#####Model A: learning rate = 0.001, epochs = 10
Finished Training.
*Final Training CE 4.378*
Running validation ...
Final Validation CE 4.380
Running test ...
Final Test CE 4.386
Training took 236.91 seconds
#####Model B: learning rate = 0.1, epochs = 10
Finished Training.
*Final Training CE 2.536*
Running validation ...
Final Validation CE 2.608
Running test ...
Final Test CE 2.613
Training took 236.26 seconds
#####Model C: learning rate = 10.0, epochs = 10
Finished Training.
*Final Training CE 4.665*
Running validation ...
Final Validation CE 4.662
Running test ...
Final Test CE 4.668
Training took 233.71 seconds

##Problem 7
>Train each of following models:
>
> * Model A: 5 dimensional embedding, 100 dimensional hidden layer
> * Model B: 50 dimensional embedding, 10 dimensional hidden layer
> * Model C: 50 dimensional embedding, 200 dimensional hidden layer
> * Model D: 100 dimensional embedding, 5 dimensional hidden layer 
>
>Use default values for all other hyperparameters.
>
>Which model gives the best training set cross entropy after 10 epochs of training ? [3 points]

##### Model A: 5 dimensional embedding, 100 dimensional hidden layer
Finished Training.
*Final Training CE 2.807*
Running validation ...
Final Validation CE 2.824
Running test ...
Final Test CE 2.834
Training took 195.19 seconds

##### Model B: 50 dimensional embedding, 10 dimensional hidden layer
Finished Training.
*Final Training CE 3.017*
Running validation ...
Final Validation CE 3.031
Running test ...
Final Test CE 3.029
Training took 175.11 seconds

##### Model C: 50 dimensional embedding, 200 dimensional hidden layer
Finished Training.
*Final Training CE 2.536*
Running validation ...
Final Validation CE 2.606
Running test ...
Final Test CE 2.613
Training took 246.46 seconds

##### Model D: 100 dimensional embedding, 5 dimensional hidden layer
Finished Training.
*Final Training CE 3.238*
Running validation ...
Final Validation CE 3.246
Running test ...
Final Test CE 3.244
Training took 184.42 seconds


## Problem 8
>In the models trained in Question 7, which one gives the best validation set cross >entropy after 10 epochs of training ? [2 points]

See the training results of **Problem 7**, you will find the answer easily.

## Problem 9
>Train three models each with 50 dimensional embedding space, 200 dimensional hidden >layer.
>
> * Model A: Momentum = 0.0
> * Model B: Momentum = 0.5
> * Model C: Momentum = 0.9
>
>Use the default settings for all other hyperparameters. Which model gives the lowest >training set cross entropy after 5 epochs ? [3 points]

##### Model A: Momentum = 0.0
Finished Training.
*Final Training CE 4.003*
Running validation ...
Final Validation CE 3.965
Running test ...
Final Test CE 3.969
Training took 118.68 seconds
##### Model B: Momentum = 0.5
Finished Training.
*Final Training CE 3.323*
Running validation ...
Final Validation CE 3.252
Running test ...
Final Test CE 3.250
Training took 121.28 seconds
##### Model C: Momentum = 0.9
Finished Training.
*Final Training CE 2.712*
Running validation ...
Final Validation CE 2.710
Running test ...
Final Test CE 2.717
Training took 120.39 seconds


## Problem 10
>Train a model with 50 dimensional embedding layer and 200 dimensional hidden layer for >10 epochs. Use default values for all other hyperparameters.
>
>Which words are among the 10 closest words to the word 'could'. [2 points]

###### The training result is as followings:
Finished Training.
Final Training CE 2.536
Running validation ...
Final Validation CE 2.608
Running test ...
Final Test CE 2.612
Training took 237.21 seconds
######The top 10 closest words to the word 'could' is as followings:
| word        | distance        |
| ------------- |:-------------:|
| should | 2.89 |
| can    | 3.35 |
| would  | 3.94 |
| may    | 4.32 |
| might  | 4.53 |
| will   | 4.63 |
| until  | 4.73 |
| before | 4.82 |
| program| 4.89 |
| court  | 4.89 |

## Problem 11
>In the model trained in Question 10, why is the word 'percent' close to 'dr.' even though they have very different contexts and are not expected to be close in word embedding space? [2 points]

Both words occur very rarely, so their embedding weights get updated very few times and remain close to their initialization.

## Problem 12
>In the model trained in Question 10, why is 'he' close to 'she' even though they refer to completely different genders? [2 points]

The model does not care about gender. It puts them close because if 'he' occurs in a 4-gram, it is very likely that substituting it by 'she' will also make a sensible 4-gram.

## Problem 13
>In conclusion, what kind of words does the model put close to each other in embedding space. Choose the most appropriate answer. [3 points]

Words that can be substituted for one another and still make up a sensible 4-gram.
