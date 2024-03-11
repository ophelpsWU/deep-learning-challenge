# deep-learning-challene
Module 21 Challenge

## Overview of the Analysis

* Create a predictive model to evaluate the likelihood of success of a funding application for funds from a charity.
* The model uses details about the organization (affiliation, governmental industry classification, organization type, and income) along with details about the proposal (use case, amount requested, and special considerations)
* The training and testing data also included the ultimate outcome for each request.
* Categorical data was converted to boolean columns, and the data was scaled by the StandardScaler. It was then split into training and testing data.
* The training data was evaluated by a Neural Network with 3 hidden layers with a Rectified Linear Unit activation function. After training the model, the testing data was evaluated for accuracy.
* Additional attempts to optimize the model were preformed, but nothing reached the desired threshold.           

## Results

* Initial Model:
  * Parameters:
    * 2 hidden layers
	* 80 nodes and 30 nodes respectively
	* 'relu' activation function on all hidden layers
  * Accuracy: 72.78%

* Optimization 1:
  * Parameters:
    * 3 hidden layers
	* 80 nodes, 30 nodes, 30 nodes respectively
	* 'relu' activation function on all hidden layers
  * Accuracy: 72.92%

* Optimization 2:
  * Parameters:
    * 3 hidden layers
	* 80 nodes, 30 nodes, 30 nodes respectively
	* 'tanh' activation function on all hidden layers
  * Accuracy: 72.82%

* Optimization 1:
  * Parameters:
    * 3 hidden layers
	* 32 nodes, 16 nodes, 8 nodes respectively
	* relu activation function on all hidden layers
  * Accuracy: 73.20%

* The target of the model is success or failure of the project.
* The features are the inputs to the model: (affiliation, governmental industry classification, organization type, income, use case, amount requested, and special considerations).
* The Name and EIN were removed because they are not relevant to the prediction.
* I selected 3 layers because I wanted to expand upon the number from the original design. I tested a couple different activation functions to see if a change made a significant difference. I tested with 80, 30, and 30 neurons, and I tested with 32, 16, and 8 neurons in the layers.
* I was unable to achieve the target model preformance.
* I made changes to the number of layers, the number of neurons, and the activation functions to try to achieve better results.


## Summary

I tested several different variations on parameters, and none of them made enough difference to meet the 75% accuracy threshold. In addition to the optimization attempts listed here and in the code, I also tried:
 * removing the amount from the inputs
 * reducing the number of Application Type and Classification by changing the threshold for what was considered "other"
 * increasing the number of epochs

I am convinced that 75% accuracy is not achievable with the data available, so I don't believe a different type of model would have been a better alternative.
