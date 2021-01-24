# Neural_Network_Charity_Analysis

## Overview of the Analysis:

Use the features in the provided dataset to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.
From Alphabet Soup’s business team, Beks received a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of columns that capture metadata about each organization.

## Results

### Data Preprocessing

* IS_SUCCESSFUL is considered the target variable

* The features would be APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT, IS_SUCCESSFUL

* NAME AND EIN are not considered to be either features or targets and are removed from the input data

### Compiling, Training, and Evaluating the Model

* The rule of thumb is to always use the ReLu activation function for hidden layers, but never for the output layer and an activation function is never used for the input layer. I used ReLu for the hidden layer and Sigmoid for the output layer, which was a binary classification.

* For one of the three attempts at optimizing the model, I used 2 hidden layers, but for all other attempts and the original attempt I used only 1 hidden layer

* I typically used about half the number of nodes in the output layer as compared to the hidden layer

* The original attempt in AlphabetSoupCharity.h5, had the best overall performance with an accuracy score of 72%, which simply involved me removing the NAME and EIN features, using 100 epochs, and using a hidden_node_layer1=8 and hidden_node_layer2 =5. The next best performing attempt was Optimization3, which produced an accuracy score of 69%

* To improve the overall performance of the model, I also tried removing more features such as APPLICATION_TYPE, ORGANIZATION, AFFILIATION, AND CLASSIFICATION. Additionally, I attempted to add an additional hidden layer for one attempt, decrease the number of epochs, change the cutoff ranges for the "Other" bin, and adding more neurons

## Summary

For this challenge, we were tasked with creating a neural network model to predict if applicants will be successful if funded by Alphabet Soup. The third deliverable asked to see if we could alter the model to make it even more efficient with it's accuracy by achieving a threshold of 75%. Unfortunately, after 3 attempts plus the initial try, the best accuracy we could reach was 72.8%, which was just a tad under the goal. To improve upon the score potentially, a Random Forest Supervised Model could work because we know the output and the csv is not too large of a dataset. Additionally, a binary logistic regression model could work since the target variable is a known dichotomous output.

![image](https://user-images.githubusercontent.com/70483866/105627508-e2043380-5dfc-11eb-9c1f-13085ea23cc2.png)


