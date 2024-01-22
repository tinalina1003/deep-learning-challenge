<h1>Analysis Report for Challenge 21</h>

## Overview
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. With your knowledge of machine learning and neural networks, you’ll use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

From Alphabet Soup’s business team, you have received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. The data contains information such as identification columns, application type, affiliation, organization, is successful, etc.

## Data Preprocessing

Columns `EIN` and `NAME` are dropped. Columns that have less than 10 unique values were dropped. A cutoff value was set to bin together 'rare' categorical variables together into a new value `Other`. The categorical variables were then one hot encoded, merged with the original dataframe, and the categorical columns were then dropped. The data was then split into training and test data for compiling, training, and evaluating.

## Method

Attempt 1:
- Cutoff for application types: < 250
- Input Neurons: 41
- Hidden Layers: 1
- Neurons per hidden layer: [80]
- Activation Functions: ['relu', 'relu', 'sigmoid']

Attempt 2:
- Cutoff for application types: < 1000
- Input Neurons: 41
- Hidden Layers: 2
- Neurons per hidden layer: [80, 40]
- Activation Functions: ['relu','relu', 'tanh', 'sigmoid']

Attempt 3:
- Cutoff for application types: < 250
- Input Neurons: 41
- Hidden Layers: 2
- Neurons per hidden layer: [40, 30]
- Activation Functions: ['tanh', 'tanh', 'tanh', 'sigmoid']

## Results

After training with 100 epochs, the model produced a

Attempt 1:
- Loss: 0.5578
- Accuracy: 0.7263

Attempt 2:
- Loss: 0.5848
- Accuracy: 0.7312

Attempt 3:
- Loss: 0.5623
- Accuracy: 0.7289


## Analysis and Summary

Changing any of the parameters and hyperparameters has minimal change to the results; any and all results produced has more than half of data loss and less than 75% accuracy. Attempt 2 had a higher accuracy with over 73% but no attempts were able to produce a performance of at least 75%.


