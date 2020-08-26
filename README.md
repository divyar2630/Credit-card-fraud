# Credit-card-fraud

## Background

It is important that credit card companies are able to recognize fraudulent credit card transactions
so that customers are not charged for items that they did not purchase.

The original data set comes from Kaggle: https://www.kaggle.com/mlg-ulb/creditcardfraud. The datasets contains transactions made by credit cards in September 2013 by european cardholders.
This dataset presents transactions that occurred in two days
The original dataset contains roughly 280K observations. I have simplified down to roughly 3000 observations. The aim of this project is to compare a few ML models and compare..

## Introduction

The dataset contains only numerical input variables which are the result of a PCA transformation.  Features V1, V2, … V28 are the principal components obtained with PCA, the only features which have not been transformed with PCA are 'Time' and 'Amount'.
Feature 'Time' contains the seconds elapsed between each transaction and the first transaction in the dataset. The feature 'Amount' is the transaction Amount, this feature can be used for example-dependant cost-senstive learning. Feature 'Class' is the response variable and it takes value 1 in case of fraud and 0 otherwise.

In this project, we will fit and compare the following 5 classification models to predict credit card fraud or not:

Logistic Regression <br>
Decision Tree <br>
Bagged Trees <br/>
Random Forest <br/>
Boosted Trees<br/>

The dataset is highly imbalanced, hence accuracy is not a good metric to evaluate the performance. We will use F1-score as the evaluation metric. ROC curve and AUC score is used to compare multiple classification algorithms.

**Result**

The classification model and the F1 score is listed below:<br/>

Logistic Regression	0.893773<br/>
Random Forest-0.891386<br/>
Boosted Trees-0.889706<br/>
Bagged Trees-0.885609<br/>
Decision Tree-0.878229<br/>

Logistic regression has the best performance, followed by random forest then boosted trees then bagged trees. As expected, a single decision tree doesn't perform too well. <br/>

The classification model and the AUC score is listed below:<br/>
  
Boosted Trees-0.973840 <br/>
Logistic Regression-0.972617<br/>
Bagged Trees-0.967590<br/>
Random Forest-0.964048<br/>
Decision Tree-0.927321<br/>

Boosted tree has the highest AUC score, followed by Logistic and decision tree is the worst.
