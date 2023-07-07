# Credit Risk Classification - Module 20 Challenge
In this Challenge, you’ll use various techniques to train and evaluate a model based on loan risk. You’ll use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers.

## Overview of the Analysis

The analysis incorporated various factors to examine the data, including:

* Loan Size: The size of the loan provided to borrowers.
* Interest Rate: The rate at which the loan was charged.
* Borrower's Income: The income of the borrower.
* Debt-to-Income Ratio: The ratio of the borrower's debt to their income.
* Number of Accounts: The total number of accounts held by the borrower.
* Derogatory Marks: Any negative remarks or records against the borrower.
* Total Debt: The overall debt amount accumulated by the borrower.

These factors were considered to gain insights and make informed assessments based on the available data.

The dataset, consisting of 77,536 data points, was divided into training and testing sets. The training set was utilized to construct an initial logistic regression model, referred to as Logistic Regression Model 1. Subsequently, Logistic Regression Model 1 was applied to the testing dataset to assess the risk level (low or high) of loans extended to borrowers. The summary of the results is provided below.

The original dataset contained 75,036 data points classified as low-risk loans and 2,500 data points classified as high-risk loans. In order to balance the training data and ensure an equal representation of both low-risk and high-risk loans in the logistic regression model, the training set data underwent resampling using the `RandomOverSampler` module. This resampling process generated 56,277 data points for each category: low-risk (0) and high-risk (1), based on the original dataset.

The resampled data was employed to construct a new logistic regression model, denoted as Logistic Regression Model 2. Its purpose was to predict the risk level (low or high) of loans extended to borrowers in the testing set. The summarized results of Logistic Regression Model 2 are provided below.

## Results

<strong>Logistic Regression Model 1:</strong>

The model's performance can be summarized as follows:

- Precision: The precision of the model was 93%. When predicting low-risk loans, the model achieved a precision of 100%, indicating that all the loans predicted as low-risk were indeed low-risk. However, when predicting high-risk loans, the precision decreased to 87%, meaning that some loans predicted as high-risk were actually low-risk.

- Accuracy: The accuracy of the model was 94%. This indicates that the model correctly classified 94% of the loans in the testing set as either low-risk or high-risk.

- Recall: The recall of the model was 95% on average. When predicting low-risk loans, the model achieved a recall of 100%, meaning that it correctly identified all the low-risk loans in the testing set. However, when predicting high-risk loans, the recall was 89%, indicating that the model missed identifying some of the high-risk loans.

These performance metrics provide an assessment of the model's ability to predict the risk level of loans, highlighting its strengths and areas for improvement.

<strong>Logistic Regression Model 2:</strong>

The performance evaluation of the model yielded the following results:

- Precision: The model achieved an overall precision of 93%. It demonstrated a perfect precision rate of 100% when predicting low-risk loans, meaning that all the loans classified as low-risk were indeed low-risk. However, when predicting high-risk loans, the precision dropped to 87%, indicating that some loans classified as high-risk were actually low-risk.

- Accuracy: The model achieved an accuracy rate of 100%. This means that all the loans in the testing set were correctly classified as either low-risk or high-risk, resulting in an accurate prediction for every loan.

- Recall: The model exhibited a perfect recall rate of 100% on average. It successfully identified all the low-risk loans in the testing set, resulting in a recall of 100% for that category. Similarly, it achieved a recall rate of 100% for high-risk loans, indicating that all the high-risk loans were correctly identified.

These performance metrics indicate a highly effective model in terms of accuracy, recall, and precision, particularly for low-risk loans. However, there is room for improvement in the precision of predicting high-risk loans.

## Summary

Compared to Logistic Regression Model 1, Logistic Regression Model 2 demonstrates a reduced likelihood of false negatives, meaning it is less likely to incorrectly classify high-risk loans as low-risk. However, when examining the confusion matrices of both models, it is evident that Logistic Regression Model 2 made slightly more false positive predictions, classifying some high-risk loans as low-risk.

Considering the objective of identifying high-risk loans, neither model achieves a precision above 90%. However, Logistic Regression Model 2 outperforms in terms of overall accuracy and recall, with fewer erroneous predictions on the testing data. Therefore, based on its higher accuracy and recall rates, Logistic Regression Model 2 is the recommended choice for this task.
