# Overview of the Analysis

## Background
Credit risk poses a classification problem that’s inherently imbalanced. This is because healthy loans easily outnumber risky loans. This analysis compares various techniques to train and evaluate models with imbalanced classes. Historical datasets of peer-to-peer lending services companies are used to build a model that can identify the creditworthiness of borrowers.

Logistic regression models are used to compare two versions of the dataset. First, the original dataset then second, a resampled version using the RandomOverSampler module from the imbalanced-learn library.

For both cases, we'll review teh target classes, train a logistic regression classifier, calculate the balanced accuracy score, generate a confusion matrix, and generate a classification report.

## Results

* Machine Learning Model 1:
  * Balanced Accuracy: Balanced accuracy is the equally weighted percision score of the positive and negative results. This model produced a 95.2% balanced accuracy score. While this score is quite good, it does not explain if the model performed well overall. 
  * Precision: This measures the total number of correct identifications divided by the total number of events. This model had a 99% percision rate. Considering the difference between the balanced accuracy and the percision rate, we can already identify a difference in the true postives and true negative's accuracy. 
  * Recall scores:  This is the number of correct identifications for a class divided by the total number for that class. For this model the postive results were identified 99.5% of the time, compared to negative results which were identified only 85% of the time. Because the data was squewed toward postive results the model was more accurate in identifying those results. 



* Machine Learning Model 2:
  * Balanced Accuracy: Balanced accuracy is the equally weighted percision score of the positive and negative results. This model produced a 99.4% balanced accuracy score.
  * Precision: This measures the total number of correct identifications divided by the total number of events. This model had a 99.4% percision rate.
  * Recall scores:  This is the number of correct identifications for a class divided by the total number for that class. For this model both the postive and negative results were identified 99.4% of the time.

## Summary

Result Summary:
* In almost all scores the model trained with resampled data peformed better. There was a slight decrease in percision related to finding correct positive outcomes, however this decrease was not significant given the increase in total accuracy. 
* In addition, the banks priary goal is to idenfity risky loans. A model that is more accurate in idenitying high risk loans provides signifiant value for two reasons. First it reduces risk by idenfity high risk loans, and second by default if a loan is not high is is considered low risk. This means that as the accuracy of idenfity high risk loans increases so does the accuracy of low risk loans.   

Because of this the model trained with resampled data is clearly preferred over the original model. 