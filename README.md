# Overview

The purpose of this analysis is to determine if applicants will be successful if funded by Alphabet Soup. A deep neural network will be used to evaluate various features to predict the success rate.

# Results

    -Data Preprocessing
        Target Variable: IS_SUCCESSFUL
        Features: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE,<br>
        ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT<br>
        Removed Features: EIN, NAME

    -Compiling, Training, and Evaluating the Model
        First Pass:
        -Two hidden layers with 8 neurons on the first layer and 4 in the second layer 
        -Relu was used as the activation function. This function is versatile and fast in most cases.
        -The model performance acheived an accuracy of 68% which is below the requested 75%
        Second Pass:
