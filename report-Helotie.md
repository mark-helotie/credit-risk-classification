# Module 20 Report

## Overview of the Analysis

The overall purpose of this analysis is to evaluate the performance of two logistic regression machine learning models to predict the credit risk associated with loans. The analysis was conducted on financial data of loan sizes, interest rates, borrowers income, debt-to-income ratios, number of accounts, derogatory marks, and total debt. The objective was to predict the loan status, being either a healthy loan (`0`) or high-risk loan (`1`).

Stages of machine learning process used in this analysis
1. Split the data into training/testing datasets
2. Create/fit a logistic regression model with the original data
3. Evaluate the performance of this model by the accuracy, precision, recall and F1-scores
4. Resample the data using RandomOverSampler to adjust the imbalance
5. Create/fit a logistic regression model, this time using the resampled data
6. Evaluate the performance of this resampled model and see how it compares to the original predictions

(The first method used in this analysis was LogisticRegression, and for the resampled data RandomOverSampling method was used.)

## Results

## Machine Learning Model 1: Logistic Regression on original data
- The overall accuracy is good at 0.99
- The healthy loans have a perfect precision, recall and F1-score of 1.00
- The scores on the high-risk loans are lacking at 0.87, 0.89 and 0.88 respectively

## Machine Learning Model 2: Logistic Regression on resampled data
- The overall accuracy continues to be good at 0.99
- The healthy loans (0) have a precision, recall and F1-score of 0.99
- The scores on the high-risk loans have significantly improved to 0.99 each


## Summary

In this above example, Logistic Regression model trained with resampled data (Model 2) is a better fit than the one trained with original data (Model 1), especially when it pertains to predicting high-risk loans. While Model 1 is very good at predicting healthy loans with low false positives and low false negatives, Model 2 has better precision and recall scores for high-risk loans which can be helpful in overcoming financial losses for the lender.

Oversampling the dataset greatly increased the accuracy of prediction for both the healthy and high-risk loans, making it a clear choice.

