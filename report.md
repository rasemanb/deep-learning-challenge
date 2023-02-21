# Alphabet Soup Neural Network Report

# Overview

A nonprofit business named Alphabet Soup has asked us to create a machine learning model to predict success of a business funded by them. 
Their business team has given us a csv containing over 34,000 organizations and their records over the years with Alphabet Soup funding. 
This machine learning model was created to help find the applicants with the highest probability of success to fund. 
This model used a binary classifier to predict whether applicants will be successful or not if they recieve funding.

# Results

## Data Preprocessing 

#### Target Variables (y)

- The target variable was the IS_SUCCESSFUL column in the dataset since we were looking at whether the business was succesful or not.

#### Features (x)
    
- The features for this model was everything in the dataset except EIN and the target variable IS_SUCCESSFUL. In the non-optomized model, 
    we tried to drop the NAME column as well, but that had a negative impact on the accuracy of the model, so we added it back in.

#### Noise Variables to be Dropped

- In the non-optomized model, we dropped both EIN and NAME because we hypothesized that these variables carried little to no weight in the model. However, after optomizing, we found that adding the NAME column back into the model had a positive impact on the accuracy score, rendering our
initial hypothesis false.

## Compiling, Training, and Evaluating the Model

#### Neurons, Layers, and Activation Function

- In the non-optomized model we used 2 hidden layer, one with 20 nodes and one with 10, since the optimal amount of neurons is anywhere in the range of 1 to the number of features (in this case, it's 20 after encoding). Since the optimal number of layers for deep learning is 1 to 3, we chose to use the same method as the neurons (splitting the middle), so we chose 2. ReLU was our selected activation function since it is widely regarded as the best model to use for deep learning. 

- For our optomized model, we first added back in the NAME variable and filtered the number of names to only those who appear more than 10 times in the
dataset. We then increased the number of hidden layers to 3 and lowered the number of neurons to 9, 6, and 6. We chose to use 9, 6, and 6 based on the succes of the Spiral Data tensorflow playground scenario (achieved test loss of 0.002 and training loss of 0.007 so we thought it may produce a similar
result in this model). We utilized ReLU again and were able to achieve an accuracy score of approximately 78 percent.

# Summary

Overall, this model could predict whether or not an investment would be successful with around 78 percent accuracy. To improve accuracy further,
we could continue with a neural network and tweak the number of features, hidden layers, and nodes as we did in the optimization stage, or we could 
try a completely new model. If we were to attempt a new model, I would suggest an SVM model as it is robust to outliers, generally has a high prediction accuracy, and it generalizes well. Howerver, I do believe that neural networks are most likely the best model for this problem as it is tailored to deep learning queries.





