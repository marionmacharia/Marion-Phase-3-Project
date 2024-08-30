# Predicting Customer Churn at Syriatel
#### A machine learning project analyzing data from Syriatel to build a model that predicts from various features whether a customer would stick or churn.
#### By [Collin Owino](https://github.com/Collin9726)

### [Presentation Slides](https://docs.google.com/presentation/d/1QGBBiOypnkWMqDr_5NoNe7-nTs7kkcNRxPJwgoYJq-4/edit?usp=sharing)


## Description

<table>
<tr>
<td>
Syriatel is a telecommunications company providing mobile network services in Syria. The company seeks to be able to predict which customers are likely to drop them as their mobile network provider so as to put measures forehand to incentivize them. They have records in their database detailing customer mobile services usage over the past couple of years and whether they churned or not. Using this data, we were tasked to do an analysis and develop a machine learning model that will predict whether a customer will drop their services or not.
</td>
</tr>
</table>

#### Latest updated version is on 29th Aug 2024.

## Technologies used

1. Python v3.10
2. Jupyter Notebook
3. Scikit-learn
4. Logistic Regression
5. Decision Trees

## The Data

We used data from Syriatel's database with relevant features collated in the ```syriatel_customer_churn.csv``` that can be viewed [here](./data/syriatel_customer_churn.csv). This data contains multiple features that we were to analyze to predict whether a customer would continue using Syriatel services or would churn. These features include number and length of calls made by a customer at various times and which plans they have subscribed to. The target feature is the churn column which tells us whether or not the customer churned.

## Preprocessing
The csv data was split into training and test sets. The train set was preprocessed in various ways including dropping features with high correlations to others, one-hot encoding categorical variables and standardizing continuous features. These transformations were later also applied to the test set for its use in testing the models.

## Modelling
Two modelling techniques were used to develop binary classifiers that predict whether a customer would churn or not.

#### Decison Trees
We started with vanilla Decision Tree model applying the entropy function. We fit this into the preprocessed train data and generated predictions for both train and test sets. With a perfect train AUC score of 1.0 and a significantly less AUC value of 0.83 on the test set, the model was deemed overfitting.

We then tuned various hyperparameters to optimize the model. We applied a range of values to maximum depth minimum samples split, minimum sample leaf and maximum feature size, and investigated their optimal values. The final model had a train AUC score of 0.867 and a test score 0.860 showing that we had reduced overfitting and had improved our models ability to predict "unseen" data.

#### Logistic Regression
We built a basic Logistic Regression model using the liblinear solver. This gave us train and test AUC scores of 0.79 and 0.81 respectively. We then tuned the model to try improve its performance. We compared the results of using different regularization levels and found an optimal C reqularization value of 10. To address the class imbalance in the target, we applied Synthetic Minority Oversampling (SMOTE) and consequently got an improvement of the test AUC score to 0.83.

#### Final model
We selected the final model as the one that performed best, i.e. the tuned Decision Tree classifier which had a test AUC of 0.86 and an accuracy score of 0.941.

##### Confusion matrix
<img src="images/final_model_conf_matrix.png"
     alt="Confusion matrix"
     style="width=100%;" />

##### ROC curve using test data
<img src="images/final_model_roc_curve.png"
     alt="ROC curve using test data"
     style="width=100%;" />

## Evaluation
The final model generated following an iterative approach of trying to improve previous model performances showed a good AUC score of 0.86 on the test data. Its accuracy score on "unseen" test data means that 94% of the time, this model will give the correct prediction on whether a customer would churn or not. Given the business problem of trying to catch customers likely to churn so as to incentivize them, this model adequately addresses that need. Syriatel will be able to use this model to predict from customer mobile services usage the likelihood of a customer dropping them albeit occasional false positives and false negatives.


## Contribution
To contribute to this project follow these easy steps:

- Fork the repo
- Create a new branch in your terminal (git checkout -b improve-feature)
- Make appropriate changes in file(s)
- Add the changes and commit them (git commit -am "Improve App")
- Push to the branch (git push origin improve-app)
- Create a Pull request

## Support and contact details
For any queries, issues, ideas or concerns contact [Collin Owino](owino.collin@gmail.com). Your feedback is highly appreciated.
### [License](LICENSE)
MIT license
Copyright (c) 2024 **Collin Owino**