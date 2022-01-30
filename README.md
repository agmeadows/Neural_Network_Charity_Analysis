# Overview

The purpose of this analysis is to determine if applicants will be successful if funded by Alphabet Soup. A deep neural network will be used to evaluate various features to predict the success rate.

# Results

## Data Preprocessing
        Target Variable: IS_SUCCESSFUL
        Features: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE,<br>
        ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT<br>
        Removed Features: EIN, NAME

## Compiling, Training, and Evaluating the Model

**First Pass:**<br>
- Two hidden layers with 8 neurons on the first layer and 4 in the second layer 
- Relu was used as the activation function. This function is versatile and fast in most cases.
- The model performance achieved an accuracy of 68% which is below the requested 75%
    
**Second Pass:**<br>
- Column ASK_AMT was binned into 4 groups to reduce the variation.
- The IS_SUCCESSFUL column was turned into a category and the 0 value column was discarded
- Three hidden layers with 8 neurons on the first layer and 6 in the second layer and 4 in the third.
- Sigmoid was used as the activation function. Since the input values have not been normalized, sigmoid is able to place the output between 0 and 1. This will improve fit at the potential cost of overfitting.
- The model performance achieved an accuracy of 72% which is much closer to the requested 75%

## Summary

The optimized second pass performs marginally better than the first pass. There is some risk to overfitting if the model is trained for more than 15 epochs. Sigmoid appears to be the best activation function for this data set. Further optimizing the input features could lead to better results.
