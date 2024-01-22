<h1>Analysis Report for Challenge 21</h>

## Overview
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. The data contains information such as identification columns, application type, affiliation, organization, is successful, etc.

## Data Preprocessing

Columns `EIN` and `NAME` are dropped. Columns that have less than 10 unique values were dropped. A cutoff value was set to bin together 'rare' categorical variables together into a new value `Other`. The categorical variables were then one hot encoded, merged with the original dataframe, and the categorical columns were then dropped. The data was then split into training and test data for compiling, training, and evaluating.

## Method

Attempt 1:

- Input Neurons: 80
- Hidden Layers: 1
- Activation Functions: ['relu', 'relu', 'sigmoid']

The model started with 80 input neurons with `relu` activation function, a 30 hidden layer neuron also with `relu` activation function, and an output of 1 neuron and a `sigmoid` activation function. These were chosen as our result needs to be a clear successful (1) or unsuccessful (0). By categorizing values between 0 and 1, `relu` and `sigmoid` functions would be the most logical choice. The input number of features is just the number of features in our X train dataset. The hidden layer number of neurons was set to 30, a number less than the number of features.

Attempt 2:
- Input Neurons:
- Hidden Layers:
- Activation Functions:

Attempt 3:
- Input Neurons:
- Hidden Layers:
- Activation Functions:

## Results

After training with 100 epochs, the model produced a

- Loss: 0.5578
- Accuracy: 0.7263

## Analysis

This is by no means a good model. The results lost over half the data with only 72.63% accuracy. 


