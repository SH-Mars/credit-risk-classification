# credit-risk-classification
Week 20 Challenge: Supervised Machine Learning

## Overview of the Analysis

* For this challenge, we would like to build a supervised ML model for loan risk, based on historical lending activity.
* Column `loan_status` in the dataset is the target which we would like to predict, `0` for `healthy loan` and `1` for `high-risk loan`.
* In the historical dataset, we have `75036` of `healthy loan` and `2500` of `high-risk loan`.
* To build the model, we use Logistic Regression because the target variable is binary. We first split the dataset into training and testing data, and apply/fit the logistic regression to training data. After that, we utilize the trained model to predict the testing data then compare the predicted results and actual results to see how accurate is this model and how the model performs.
* We also use the resampling method to have the data be equally for both `healthy loan` and `high-risk loan` in our target. After the resampling, we also apply the Logistic Regrssion model to see if the resampled data would fit the model better than the original data we have.

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.

* Machine Learning Model 1:
  * The first model was built based on original data
  * Balanced Accuracy: `0.9507899694523869`
  * Precision: `0` -> 1.00 | `1` -> 0.86
  * Recall: `0` -> 1.00 | `1` -> 0.91



* Machine Learning Model 2:
  * The second model was built based on resampled data.
  * Balanced Accuracy: `0.9948356781759595`
  * Precision: `0` -> 1.00 | `1` -> 0.86
  * Recall: `0` -> 0.99 | `1` -> 1.00

## Summary

* Model 2 performs better than Model 1. Model 2 has a higher Balanced Accuracy Score, and both models have about the same Precision and Recall.
* In this case, successfully predict `1` is more important than predict `0`. Since `1` represents `high-risk loan`, if the model could predict `1` accurately, it could help the lending service company to avoid the potential risk.
