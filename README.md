# Predicting Customer Churn at Syriatel



## Business understanding

<table>
<tr>
<td>
Syriatel is a telecommunications company providing mobile network services in Syria. Project Overview
This project aims to predict customer churn for Syriatel, a telecommunications. The primary goal is to build a classification model that accurately identifies customers who are likely to churn, allowing the business to take measures to retain them. 
</td>
</tr>
</table>



## The Data

We used data from Syriatel's database . 
This data contains  features that we were to analyze to predict whether a customer would continue using Syriatel services or would churn.

## processing
The csv data was split into training and test sets. The train set was preprocessed in various ways including dropping features with high correlations to others, one-hot encoding categorical variables and standardizing continuous features. These transformations were later also applied to the test set for its use in testing the models.

## Modelling
modelling techniques were used to develop binary classifiers that predict whether a customer would churn or not.

#### Decison Trees




#### Logistic Regression
We built a basic Logistic Regression model using the liblinear solver. This gave us train and test AUC scores of 0.79 and 0.81 respectively. We then tuned the model to try improve its performance. We compared the results of using different regularization levels and found an optimal C reqularization value of 10. To address the class imbalance in the target, we applied Synthetic Minority Oversampling (SMOTE) and consequently got an improvement of the test AUC score to 0.83.

#### Final model
We selected the final model as the one that performed best, i.e. the tuned Decision Tree classifier which had a test AUC of 0.86 and an accuracy score of 0.941.

##### Confusion matrix


##### ROC curve using test data


## Evaluation
The final model generated following an iterative approach of trying to improve previous model performances showed a good AUC score of 0.86 on the test data. Its accuracy score on "unseen" test data means that 94% of the time, this model will give the correct prediction on whether a customer would churn or not. Given the business problem of trying to catch customers likely to churn so as to incentivize them, this model adequately addresses that need. Syriatel will be able to use this model to predict from customer mobile services usage the likelihood of a customer dropping them albeit occasional false positives and false negatives.


RECOMMENDATIONS
