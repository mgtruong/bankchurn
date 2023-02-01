# bankchurn
This is the final project for my data mining course. The purpose was to predict customer churn based on a bank dataset by creating a predictive model in R.

# Introduction
This project analyzes a dataset on customer churn in a bank. Customer churn is defined as the rate at which customers stop shopping at a company within a specific time frame. For banks, it’s interpreted as a client who shuts down their bank account. Predicting the customer churn in a bank will be helpful to understand what factors are most significant in contributing to customers closing their bank accounts. 

## Objective
The objective of this project is to predict whether a customer leaves the bank or not, and which variables are most significant concerning that. This will help banks anticipate potential customer churners and give them time to prevent this.

## About the Dataset
The used dataset was received from [Kaggle.com](https://www.kaggle.com/mathchi/churn-for-bank-customers). The dataset contains 10,000 observations and 14 variables about customers. Some variables do not affect the problem, such as row number, customer ID, and surname, so they should be deleted. Now, there are 11 variables. There are 6 quantitative variables and 5 categorical variables, including the binary response variable. For the categorical variables, only geography and gender will be converted into factors since they have a non-numeric output.

The quantitative variables are credit score, age, tenure, balance, number of products, and estimate salary. The number of products refers to how many items a customer has bought through this bank. The categorical variables are geography (1 = France, 2 = Germany, 3 = Spain), gender (1 = female, 2 = male), if a customer has a credit card (1 = has a credit card, 0 = doesn’t have a credit card), and if they are an active member (1 = active, 0 = inactive). The response variable is whether the customer has left the bank or not (1 = left, 0 = stayed).

## Used Data Mining Techniques
This project was able to utilize different data mining techniques to create and compare different predictive models to understand customer churn better. The data mining techniques used in this project are exploratory data analysis, logistic regression, decision trees, and random forest. After conducting logistic regression, the variables that have a statistically significant relationship with the response variable were revealed. Alongside the logistic regression model, a classification decision tree and random forest model were constructed and compared to see which is the best predictive model. 

# Outcome
After creating the three different predictive models, the results conclude that random forest is the most suitable model to use. It has the most correctly predicted outcomes based on the observed values with the smallest prediction error. Thus, the bank should use the random forest model to forecast whether a certain customer is going to leave their bank or not.

There are two measures that determine which variables are most important. The first one is the mean decrease in accuracy, which is based on how accurate a model is when a variable is excluded. The second one is the mean decrease in Gini, which shows the total decrease in node impurity. Node impurity explains the measurement of homogeneity of the nodes and the importance of a certain variable. When conducting both of these measures, it was concluded that age is one of the variables with more predictive power. It was also concluded that whether a customer has a credit card or not is one of the variables with the least predictive power.
