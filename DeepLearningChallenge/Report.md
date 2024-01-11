## Overview 

The  Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures.The purpose of the analysis is, to create a binary classifier by using machine learning and neural networks, on the features of the dataset that can predict whether applicants will be successful if funded by Alphabet Soup.

## Results

# Data Preprocessing

What variable(s) are the target(s) for your model?

target = IS_SUCCESSFUL

What variable(s) are the features for your model?

APPLICATION_TYPE

AFFILIATION

CLASSIFICATION

USE_CASE

ORGANIZATION

STATUS

INCOME_AMT

SPECIAL_CONSIDERATIONS

ASK_AMT

What variable(s) should be removed from the input data because they are neither targets nor features?

EIN and NAME 
These two Identification columns are neither targets nor features so deleted but NAMES column was later added in features to optimize the model for obtaining 75% or above accuracy.

## Compiling, Training, and Evaluating the Model

How many neurons, layers, and activation functions did you select for your neural network model, and why?

# In the initial Model 

Number of Hidden Layers = 2

Number of Neurons for each Layer

hidden_nodes_layer1 = 80

hidden_nodes_layer2 = 30

Activation Function used For Hidden Layers = RELU

Result:

The model displays the accuracy of 72%.

# Attemp Number 1 To Optimise the Model To Acheive Accuracy Higher than 75%

Number of Hidden Layers = 2

Number of Neurons for each Layer

hidden_nodes_layer1 = 40

hidden_nodes_layer2 = 15

Activation Function used = RELU

Result:

Making above changes to the model increased the accuracy to 73%.

# Attemp Number 2 To Optimise the Model To Acheive Accuracy Higher than 75%

For Optimising the Model in this attempt number of bins has been altered for Applitication Type column and Classification.

Number of Hidden Layers = 3

Number of Neurons for each Layer

hidden_nodes_layer1 = 7

hidden_nodes_layer2 = 14

hidden_nodes_layer3 = 21

Model has been tried and optimised using two activation fuctions :

Tanh and Relu

Result:

Making above changes to the model displays the accuracy of 72%.

# Attemp Number 3 To Optimise the Model To Acheive Accuracy Higher than 75%

For Optimising the Model in this attempt 'Name' column is included in the features and used binning for rare occurrences (for less than 10 value counts).

Number of Hidden Layers = 3

Number of Neurons for each Layer

hidden_nodes_layer1 = 100

hidden_nodes_layer2 = 50

hidden_nodes_layer3 = 25

activation function = relu

Result:

Making above changes to the model increased the accuracy to 78%.

## Summary

To Summarize the overall results of the deep learning model, I would say that adding or deleting features, trying different number of hidden layers and number of neurons or creating more or fewer bins for rare occurrences columns do affect the model efficiency and it can be seen from the above explanation and results that how adding 'Name' feature increased the model accuracy to 78%.

Though the above deep learning model worked well but it is worthwhile to explore the applicability of Random Forest, a non-deep learning algorithm, for this classification problem.Random Forest offers insights into feature importance, helping to explore which features contribute significantly to the classification. It can be valuable for feature selection and comprehending the underlying patterns in the data.



