# SYRIATEL CUSTOMER CHURN

![Image of cell tower](Cell-Tower.jpg)


## Business understanding



 Syriatel is a Telecommunication company providing mobile network services in Syria.The objective of this project is to build a classifier that predicts whether a customer will  stop doing business with SyriaTel.Our primary goal is to  build a classification model that accurately identifies customers who are likely to churn, allowing the business to take measures to retain them.





## The Data Understanding

The data contains various features that we shall analyze to predict whether a customer would continue using Syriatel services or would churn. 
The target variable, churn, is a binary categorical variable where:
`True`:indicates the customer churned 
`False`:indicates the customer did not churn.

## Preprocessing
The csv data was split into training and test sets. The train set was preprocessed in various ways including dropping features with high correlations to others, one-hot encoding categorical variables and standardizing continuous features. These transformations were later also applied to the test set for its use in testing the models.

## Modelling
modelling techniques were used to develop binary classifiers that predict whether a customer would churn or not through:

Decision Trees
Linear Models
Logistic Regression: Used for binary classification problems. It estimates the probability of a binary outcome based on one or more predictor variables.
Linear Regression: Used for predicting continuous outcomes based on one or more predictor variables. It assumes a linear relationship between predictors and the outcome.


#### Decison Trees
These models split the data into subsets based on feature values, leading to a tree-like structure of decisions. They can be used for both classification and regression tasks.



#### Logistic Regression
We had train and test AUC scores of 0.79 and 0.81 respectively. 
We tuned the model to try improve its performance by comparing  the results of using different regularization levels and found an optimal C reqularization value of 10.
 In class imbalance , we applied Synthetic Minority Oversampling and  got an improvement of the test AUC score to 0.83.
 
## final model
The final model that performed best,was the tuned Decision Tree classifier which had a test AUC of 0.86 and an accuracy score of 0.941.

Here is the presentation of the final model: [Presentation slides](https://www.canva.com/design/DAGPOmwWMjk/jkxWr9zsSb-HaRG9aS1P5w/edit?utm_content=DAGPOmwWMjk&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)



### EVALUATION

The final model, refined through iterative improvements, achieved a strong AUC score of 0.86 on test data and an accuracy of 94% for predicting customer churn. This performance is well-suited for Syriatel’s goal of identifying at-risk customers for targeted retention efforts. While the model effectively predicts churn risk based on mobile service usage, it may occasionally produce false positives or negatives.



## RECOMMENDATIONS

# Improve Customer Service and Experience Quality

By Understanding Customer Expectations

Gather Feedback: Use surveys, reviews, and direct feedback to understand what customers expect from your service.
Analyze Data: Look at customer behavior and preferences to identify trends and common issues.

 Enhance Communication Channels
Multi-Channel Support: Provide multiple ways for customers to reach you (e.g., phone, email, live chat, social media).
Responsiveness: Ensure quick and effective responses to customer inquiries and issues.

## Identify and Strengthen Relationships with  Customers

Identify: Recognize who your customers are, including their preferences, behaviors, and needs. This might involve collecting and analyzing data from various sources such as customer feedback, purchase history, and interaction logs.

Strengthen Relationships: Build and maintain strong, positive connections with your customers. This could involve personalized communication, loyalty programs, or offering exceptional support. The goal is to make customers feel valued and understood, enhancing their overall experience with your brand.

## Focus on At-Risk Customers

At-Risk Customers: These are customers who are likely to churn or disengage from your business. Identifying them early is crucial. They might show signs of dissatisfaction or reduced engagement.

Focus: Implement strategies to re-engage these customers. This could involve personalized offers, special attention from customer service, or resolving issues that are causing dissatisfaction. The aim is to address their concerns and prevent them from leaving.


## Design Targeted Marketing Campaigns

Targeted Marketing: Create marketing campaigns that are specifically tailored to different customer segments based on their interests, behaviors, or demographics.

Design: Develop campaigns that speak directly to the needs and preferences of these segments. This could involve personalized emails, targeted ads, or special promotions. The goal is to make your marketing efforts more effective by reaching the right people with the right message.

## Allocate Resources Efficiently

Allocate Resources: Ensure that your time, money, and personnel are being used in the most effective way possible.

Efficiently: This involves prioritizing areas that have the highest impact on customer satisfaction and experience. For instance, investing in training for customer service reps, improving technology for better customer interaction, or focusing marketing efforts where they yield the most return. The goal is to optimize resource use to maximize customer satisfaction and business outcomes.

## Regularly Review Model Performance

Review Model Performance: Assess how well your strategies and systems are performing in terms of improving customer service and experience.

Regularly: Conduct these reviews on a consistent basis to ensure that your approaches are still effective and relevant. This might involve analyzing customer feedback, tracking key performance indicators (KPIs), or reviewing service metrics. The goal is to make data-driven adjustments and improvements to continually enhance the quality of service and customer experience.

## Conclusions

By integrating these practices, you ensure that your predictive analytics are both robust and aligned with your business needs, ultimately driving better decision-making and achieving strategic goals.
