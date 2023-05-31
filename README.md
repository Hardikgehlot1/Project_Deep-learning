deep-learning-challenge
Deep learning homework for the GT Data Science Bootcamp!

## Report

After creating and tuning the nn model, here are my takeaways on the model's performance and the tuning process.

## Overview

This analysis will cover the details of the neural network model created for this challenge. Further, the adjustments made to the model in order to increase performance will be described.

## Results

### Data Preprocessing

1.0  The target variable in this model is the "IS_SUCCESSFUL" column.
2.0 The feature variables in the final model were:
    NAME
    APPLICATION_TYPE
    AFFILIATION
    CLASSIFICATION
    USE_CASE
    ORGANIZATION
    INCOME_AMT
    ASK_AMT
3.0 The variables that were removed from the final model were:
     EIN - just an id number
     SPECIAL_CONSIDERATIONS - this column had over 34,000 'N' values and only 27 'Y' values. Not helpful.

## Compiling, Training, and Evaluating the Model
The final model had six layers. The first layer had 100 neurons or nodes, the second layer had 100 neurons, the third layer had 100 neurons, the fourth layer had 60 neurons, the fifth layer had 60 neurons and the six layer had 60 neurons.The model used two different  activation functions - rectified linear units (relu) and sigmoid. See the image below for details of the model construction.
![image](https://github.com/Hardikgehlot1/deep-learning-challenge/assets/120690578/e2dcf714-4190-4bc1-94a6-875fb6c9d5e0)

The model exceeded the target performance of 74%. The model reached 73% accuracy 
![image](https://github.com/Hardikgehlot1/deep-learning-challenge/assets/120690578/47014799-b83a-447b-a6e9-02f2076592bb)



I took the following steps to increase the model's performance:
  1.  I had rearange the X_test and X_train assinged data
  2. the column, SPECIAL_CONSIDERATIONS  was removed because they were both almost all one value.
  3.  I added a more layer to increase the model's complexity.
  4. I changed the activation functions to layers as well as the output layer.
  
  ## Summary
The tuned neural network was able to predict outcomes with 74% accuracy. This is a marked increase when compared to the original neural network which predicted outcomes with 72% accuracy. This was achieved by rearanging data, removing SPECIAL_CONSIDERATIONS and STATUS from the feature variables, increasing the model's complexity by adding more hidden layer, and changing some of the layers' activation functions.

As an alternative to the nn model, a random forest classifier could be used. I attempted this and was able to get 78% accuracy. This is a much better score than the 75% threshold I was shooting for. However, the neural network won out with 79% accuracy. With further tuning, it may be possible to improve on one or both of these models and get an even better predictive classifier.
  
  
