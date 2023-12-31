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
        1. Imported the accuracy score, confusion matrix, and classification report modules and used them to gather their respective values.

* Model 2: Resampled Training Data
    1. Resample the training data from model 1.
    2. Repeat steps ii. and iii. from model 1 and use the resampled training data for ii. b.


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
        * Precision: 0.87 (87%)
        * Recall: 1.00 (100%)

## Summary
Both logistic regression models have shown that they are not suitable in predicting both healthy loan and high-risk loan labels.  Both models were very good at predicting healthy loans as they have 100% in both precision and recall with the only difference being that model 1 had 99% accuracy while model 2 had 100% accuracy.  The issue comes from their respective values for high-risk loans.  The bar of acceptance for the model to be useful was at least 90% for both precision and recall due to the importance of correctly predicting who are and aren't credit risks.  Both models have at least one trait below 90% (model 1 having 2 and model 2 having 1) which is not acceptable in the case of this topic.  In conclusion, although model 2 is the superior, both of these models are not fit to be used in practice.