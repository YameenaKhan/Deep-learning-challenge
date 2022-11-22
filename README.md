# Deep-learning-challenge
Repo contains solution to HW21

## Contents of Repo
1. Resources folder: Containing the charity_data.csv from which the data has been extracted and used in the model
1. Jupyter Notebooks : AlphabetSoupCharity_model.ipynb & AlphabetSoupCharity_Optimzation.ipynb
1. HDF5 Files: AlphabetSoupCharity.h5 & AlphabetSoupCharity_Optimization.h5 
1. Neural Network Model Report


## Overview 
The purpose of this assignment is to create a model that helps a Non- Profit Alphabet Soup to predict whether applicants will be successful or not if funded. 

Using deep learning and neural networks, I have created a model to predict the performance of the organizations using the data provided in the CSV file that contains information of 34000 organizations that have received funding from Alphabet Soup over the years. 

I compiled and trained the model and then evaluated it using the test set to see its accuracy and loss. Then attempted to optimize the model after making a few changes and then evaluated the optimized model’s accuracy and loss.

## Data Preprocessing


* *Target Variables* <br>
We can say the main target variable for our model would be the success of the Non-Profit. Hence the last column of our dataset IS_SUCCESSFUL would be the target.

* *Feature Variables* <br>
In the dataset provided all columns except for unique identifiers (Name and EIN) seem to be of importance in influencing the performance of the Organization. 

* *Variables that are neither Target nor Features* <br>
The unique identifiers i.e. variables like organization name and EIN a unique number to identify the organization are variables that do not and cannot influence the performance of the particular organization hence we would drop them from the data set.


## Compiling, Training, and Evaluating the Model

**Model Features**<br>
The model I created initially I used two hidden layers with 10 nodes each and relu activation since Relu activation is known to work and train better as it overcomes the vanishing gradient problem, allowing models to learn faster and perform better. Used 10 nodes and two layers as it seems like a reasonable and consistent number to start work with.

**Model Performance**<br>
My model did not achieve the target performance, although I used 200 Epochs when i was training my model. 
My model could not achieve more than 75% accuracy. It only achieved an accuracy of 0.7306. So i took further steps to optimize my model 


**Model Optimization**<br>
In order to make my model perform better i took a few steps:<br>

1. Added a third hidden layer with 15 nodes and activation “sigmoid”
1. Added a fourth hidden layer with 12 nodes and activation “Relu”
1. Changed the number of nodes on the first two hidden layers from 10 to 15
1. Changed the activation from “Relu” to “Sigmoid” on the second hidden layer
1. Reduced the number of epochs from 200 to 100 when training the model

**Optimized Model Performance**<br>
After making the above changes my model still did not achieve the target performance. 
Although the performance of the optimized model is better than the initial Model that I had put together. The optimized model could achieve accuracy of 0.7325.


## Summary 

Looking at the results of both models - initially created and further optimized, we can easily say that the Neural Network Model is not the best model for this particular dataset. 

As even the optimized model presents just 73.26% accuracy and loss of around 55%.

Instead we could use model that uses Dimensionality Reduction like Principal Component Analysis and then run logistic regression to predict whether the Non Profit would perform well if provided with funding or not.

