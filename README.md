# Credit Risk Classification Analysis

## Overview of the Analysis
The purpose of this challenge was to assess the creditworthiness of borrowers.  The dataset was the historical lending activity from a peer-to-peer lending services company comrpised of: 
* loan size
* interest rate
* borrower income
* debt to income
* number of accounts
* derogatory marks
* total debt
* loan status  
To fulfill the aim of this task, two logistic regression models were built to use the data above to predict the loan status of each individual.  In order to build the models and complete the challenge, the process was split into the following stages for each model:

* Model 1: Original Data
    1. Splitting the data into training and test sets 
        1. The data was read and put into a data frame called lending_data_df.
        2. The data was split into X and y values with y being the loan status column and X being the entire lending_data_df excluding the loan status column.
        3. The .value_counts() function was used with y to determine the number of healthy loans (depicted as 0) and high-risk loans (depicted as 1).
        4. Imported the train_test_split module to split the X and y into training and test sets.
    2. Create the logistic regression model
        1. Used the LinearRegression module to instantiate the model.
        2. Then the model was fit using the training data.
        3. The predictions were made using the test data.
    3. Gather the results
        1. Used the 

* Model 2: Resampled Train Data
    1. Resample the train data
    2. 


## Results
* Model 1: 
    * Healthy Loan (0)
        * Accuracy: 0.99 (99%)
        * Precision: 1.00 (100%)
        * Recall: 1.00 (100%)
    * High-Risk Loan (1)
        * Accuracy: 0.99 (99%)
        * Precision: 0.87 (87%)
        * Recall: 0.89 (89%)
* Model 2: 
    * Healthy Loan (0)
        * Accuracy: 1.00 (100%)
        * Precision: 1.00 (100%)
        * Recall: 1.00 (100%)
    * High-Risk Loan (1)
        * Accuracy: 1.00 (100%)
        * Precision: 1.00 (89%)

## Summary
The logistic regression model (using the original data) has shown to be not suitable in predicting both healthy loan and high-risk loan labels.  The healthy loans have a 100% in both precision and recall while the high-risk loans has 87% in precision and 89% in recall.  With credit risk as the topic for analysis, both labels should have at least a 90% in precision since precision is a more important trait in assessing risk.  Due to high-risk loans having a precision slightly below the requirement, the logistic regression model is just barely not suitable in its predictions.