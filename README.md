# Credit_Risk_Analysis

## Overview

### Purpose

This analysis was inteded to how certain factors help rpeditct whether someone is at a high or low credit risk status. Training and evaluating models with unabalanced classes, imbalanced-learn and scikit-learn libraries where used to build and evaluate these models using resampling. Credit card data from LendingCLub services was ovresampled with RandomOverSampler and SMOTE algorithims, and undersampled with ClusterCentroids algorithm. A combinational method of over-and undersampling using SMOTEENN algorithm was also implemented finally comparing two new machine learning models which reduce bias (BalancedRandomForestClassifeier and EasyEnsembleClassifier) to predict credit risk. 

## Results

- Balanced accuracy score and the precision and recall scores of all six machine learning models

### Naive Random Oversampling

![naive](https://user-images.githubusercontent.com/94864663/166157534-871fac32-5026-4a4b-b78d-b4e46f1ddfd0.png)

- Balanced Accuracy: calculated score of about 0.6403
- Precision: Low precision of 0.01 for high risk, high precision of 1.00 for low risk. 
- Recall: 0.66 for high risk, 0.62 for low risk; ratio high to low is 0.66/0.62 = 1.06

<br>


### SMOTE Oversampling

![SMOTE](https://user-images.githubusercontent.com/94864663/166157535-222a09d6-cc33-4bc3-a3c5-c00c4f9fad6c.png)

- Balanced Accuracy: calculated score of about 0.6515
- Precision: Low precision of 0.01 for high risk, high precision of 1.00 for low risk.
- Recall: 0.61 for high risk, 0.69 for low risk; ratio high to low is 0.61/0.69 = 0.884

<br>

### Undersampling

![Under](https://user-images.githubusercontent.com/94864663/166157538-0f48657c-fd39-4897-8958-1f03ca7a787d.png)

- Balanced Accuracy: calculated score of about 0.6515
- Precision: Low precision of 0.01 for high risk, high precision of 1.00 for low risk.
- Recall: 0.61 for high risk, 0.69 for low risk; ratio high to low is 0.61/0.69 = 0.884

<br>

### Combination (Over and Under) Sampling

![Combo](https://user-images.githubusercontent.com/94864663/166157545-9d45b812-a18f-4da7-b5ba-11b91dd90c37.png)

- Balanced Accuracy: calculated score of about 0.6515
- Precision: Low precision of 0.01 for high risk, high precision of 1.00 for low risk.
- Recall: 0.71 for high risk, 0.57 for low risk; ratio high to low is 0.71/0.57 = 1.25

<br>

### Balanced Random Forest Classifier

![Balanced](https://user-images.githubusercontent.com/94864663/166157550-9217a3aa-4396-4fd5-ab96-82d8ddd70888.png)

- Balanced Accuracy: calculated score of about 0.8012
- Precision: Low precision of 0.04 for high risk, high precision of 1.00 for low risk.
- Recall: 0.71 for high risk, 0.89 for low risk; ratio high to low is 0.71/0.89 = 0.798

<br>

### Easy Ensemble AdaBoost Classifier

![Easy](https://user-images.githubusercontent.com/94864663/166157553-56397c13-8273-4b2b-a6ac-35ce102bf4a9.png)

- Balanced Accuracy: calculated score of about 0.9179
- Precision: Low precision of 0.09 for high risk, high precision of 1.00 for low risk.
- Recall: 0.89 for high risk, 0.94 for low risk; ratio high to low is 0.89/0.94 = 0.947

<br>

## Summary

Based on the results in terms of balanced accuracy, the score closest to 1 is the ideal model for machine learnining. This means with a score around 0.92, the Easy Ensemble AdaBoost Classifier is the best model to choose. The Balanced Random Forest Classfier model comes in close with a balanced accuracy score of about 0.80, however the combination sampling, undersampling, and SMOTE oversampling models all have similar scores of about 0.65.  With a balanced accuracy score of roughly 0.64, the Naive Random Oversampling model is not too far behind, but it appears to be the weakest among the six models tested. 

The choice of best recommendation is also supported when we take a look at recall scores which should also be close to 1 for the best model. With a recall score of 0.89 for high risk and 0.94 for low risk, the results show that the Easy Ensemble AdaBoost Classifier model also had the highest recall scores between the six machine learning models we tested. Looking at precision, it is evident that these scores are fairly similar amongst all six models with a low precision for high risk and a high precision for low risk. 

For an ideal model, we should also expect high F1 scores. These scores combine precision and recall metrics to sum up the predicitve performace of the model. With an F1 score of 16%, the Easy Ensemble AdaBoost Classifier is solidfied as the best choice when comapred to scores of 7% fro the Balanced Random Forest Classfier model, and 2% for the combination sampling, undersampling, SMOTE oversampling, and naive random oversampling models. Therfore, based on the balanced accuracy score, the recall scores, and even F1 scores the best machine learning model in this case would be the Easy Ensemble AdaBoost Classifier model. 

