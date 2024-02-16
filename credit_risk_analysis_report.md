# Module 12 Report Template

## Overview of the Analysis

The Credit Risk analysis aims to predict borrower outcomes by using two different classification models. The goal is to successfully identify risky or safe borrowers. The dataset consists of borrower and loan characteristics such as income, loan size, the ratio of debt to income, number of accounts, derogatory marks, total debt, and interest rates. Our outcome variable, `loan_status`, is either 0 for a healthy loan, or 1 for a high-risk loan. In the dataset, we have 75036 records of healthy loans, and 2500 high-risk loans. 

The machine learning process began by dividing the data into the labels and features, or y and X, columns. The `train_test_split` function created training and testing data subsets to use in the analysis. For this challenge, we ran logistic regressions, and employed the `RandomOverSampler` model to rebalance our data. 

## Results

Using bulleted lists, describe the balanced accuracy scores and the precision and recall scores of all machine learning models.
https://www.scikit-yb.org/en/latest/api/classifier/classification_report.html
https://www.statology.org/sklearn-classification-report/\
http://scikit-learn.org/stable/modules/generated/sklearn.metrics.balanced_accuracy_score.html

* Machine Learning Model 1:
  * Model 1 had a precision score of 100% for the healthy loans and 85% for the high-risk loans. This indicates that of the loans that the model identified as high-risk, 85% actually were. 
  * The recall score was 99% and 91% respectively, which means the model was pretty successful at correctly classifying both types of loans. For instance, for all high-risk loans, 91% were classified as high-risk by the model. This was 99% for healthy loans. 
  * The balanced accuracy score returns the weighted average based on each class in success of predicting healthy and high-risk loans. So, the model correctly predicted the status of 99.2% of the loans. 


* Machine Learning Model 2:
  * The precision score for model 2 was slightly lower for high-risk loans, but still 100% for healthy loans. 
  * The recall for both classes was 99%, indicating more success in classifying truely high-risk loans as `high-risk`. 
  * The balanced accuracy score increased slightly to 99.4%, reflecting the increases seen in successful classifications of high-risk loans. 

## Summary

Summarize the results of the machine learning models, and include a recommendation on the model to use, if any. 
* Model 2, the model using the resampled data, was more successful than the model ran on the original data. This is apparent in the balanced accuracy score, which increased alongside the recall score. 
* Performance does depend on the problem we are tackling. In this case, if the client is the lender, it would be more important to correctly identify high-risk loans. A false 'healthy' loan would be more costly for a bank than identifying a loan as high-risk when it is actually healthy since there may be more risk of defaulting or failing to pay on time. However, in other cases, the client may have different priorities. The precision did fall with model 2, indicating that of the loans the model identified as high-risk only 84% were accurate. This would mean that if over-identification of high-risk loans was more harmful than catching a high percentage of actually high-risk loans, then model 1 would be preferable.




