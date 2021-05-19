# Santander-Customer-Transaction-Prediction

## Project Definition & Introduction
Santander Bank is a wholly-owned subsidiary of the Spanish Santander Group. As a retail bank, Santander Bank is continually working with the global data science community to explore new ways to solve one of the most challenging tasks: binary classification problems such as if a customer is satisfied, if a customer can pay the loan, or if a customer will make a transaction. 

The goal of this project is to discover the best approach to predict which customers will make a transaction in the future. This goal brings up two key challenges: first, transforming the raw data into features that better represent the underlying problem to the predictive models; second, designing a predictive model that has the best performance.  
The data provided by Santander for this project are de-identifying real data in CSV format, which have two hundred predictor variables and one target variable. The predictor variables are the historical customer data that are de-identified by Santander and the target variable is whether the customer made a transaction or not. One represents yes and zero represents no.

## Business Insights
Financial institutions want to predict whether their customers would make a specific transaction in the future, and we are helping them to identify those customers with a large amount of data representing their behaviours. The tradeoff is between the cost of promoting our product to customers and the profit of customers making transactions. We conducted cost analysis using our best performing model LightGBM and we found that we could achieve a 62.19 average profit compared with -59.51 if we randomly choose target customers. 
The threshold of minimizing the cost is 7.6%, meaning that we are targeting the customers whose probabilities of making transactions are more than 7.6% based on our predicted results. The corresponding average misclassification cost is 7.56.


## Solution Overview
Our final solution contains two major strategies, feature engineering and predictive model building. 
Our feature engineering process focuses on three major steps, detecting fake (pseudo) testing data,  adding “magic features”, and data augmenting. The detection step enabled us to remove noise records that may disturb our model training and testing process which can lead to poor model performance. The magic-feature step helped us to improve our predictive model by providing additional features that relate to the target outcome. The data augmentation step allowed us to remedy the unbalanced data in order to improve predictive accuracy. 

Our predictive-model-building process focuses on exploring and creating models that can achieve the best performance based on the ROC-AUC metric. We used the Naive Bayes model as a baseline and tried XGBoost, LightGB, neural network, and stacking models. We found that LightGB had the best performance. Knowing that the revenue or cost for each category of predicted outcome may be different, we also conducted a profitability analysis and plotted margin curves to show the impact of profitability regarding prediction thresholds.  
