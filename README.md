# Customer-churn-prediction

## 1. Introduction

This project was inspired in a kaggle competition where the goal is to predict potential customer churns before it comes true. In the real business world, that kind of solution can help companies to improve their retention rate when they don´t have enough capacity to monitor each client individually. With technologies like that on their hands, they can get good insights about their clients and plan preventive actions to keep their clients loyal.

## 2. Exploratory Data Analysis

The first step of the project was to do an exploration on the dataset to know the data and to get insights about it. Among some good insights, we can highlight the fact that there is a little imbalancement on the target variable.

![](https://github.com/luisgustavob78/Customer-churn-prediction/blob/master/GIF%2013-07-2020%2017-02-30.gif)

The analysis also revealed that clients with less than 15 months with the company have bigger chances to churn.

To identify the features with great predictive power, we calculated the information gain for each one of them.

## 3. Feature Engineering

The number of features are relatively big, and the high number of categorical variables could request a robust preprocessing task. As we identified with the information gain that the predictive power of these categorical variables is low, we decided to create a new feature with the number of services that a client contracted. We transformed 9 features into only one and we combined the information gain of them.

## 4. First Results

With that preliminar analysis, we got the following results:

Random Forest: AUC = 0.8
Logistic Regression: AUC = 0.84
Neural Network: AUC = 0.85

## 5. Improvements

Looking for improvements on the models' performance, two adjustments were done: hyperparameter tuning and to duplicate the rows where the target variable was the minority class to fix the imbalancement on the dataset. It increased the performance of random forest to AUC = 0.87. The other models did not show significant improvements.
