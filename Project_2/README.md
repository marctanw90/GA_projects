# Project 2 - Ames Housing Data and Kaggle Challenge

## Table of Contents
1. [Problem Statement](#1-Problem-Statement)  
2. [Data Dictionary](#2-Data-Dictionary)
4. [Model Evaluation](#3-Model-Evaluation)
5. [Recommendations and Conclusion](#4-Recommendations-and-Conclusion)

## 1. Problem Statement

We are WEM general insurance based in Ames, Iowa specializing in home insurance.

Customers come to us looking to get their homes insured. A part of getting their homes insured requires the valuation of their property.

We have noticed through feedback forms that customers find our application forms:
Tedious and overly complicated
Usually take more than an hour for customers to fill up (total of 80 questions)
Customers do not want to spend more than 10 mins.

Due to the high dropout rates, management is concerned with the loss of revenue and share of customers to our competitors, who offer quicker and more accurate processing times.

Where data science plays a part?
Through the use of machine learning models (Linear Regression models for this excercise), we are able to effectively simplify the process by performing EDA & Feature Engineering to cut down on unnecessary features to predict the price valuation of homes to be insured. In turn, getting rid of the conventional 80 question application form.

The predictive valuation model will help to:

* Effectively predict the valuation of the property
* Improve efficiencies and the overall customer end-to-end experience
* Increasing take-up rate due to quicker turnaround times through quicker processing times


## 2. Data Dictionary

The data set includes a population of 2930 homes that were sold in Ames, Iowa from 2006 – 2010 with 80 explanatory variables describing each (all of which includes information such as sales price, lot size, pool area, condition, overall quality, etc) which would go into assess home values within that market. Review the [data description](http://jse.amstat.org/v19n3/decock/DataDocumentation.txt).



## 3. Model Evaluation
From the results above, we see that our lasso model performed the best amognst the others. The lasso model has a lower RMSE score as well as a lower % difference between the train and test samples. Indicative of good generalization where the model is able to adapt new and previously unseen data, drawn from the same distribution as the one used to create the model.

From our LINE assumptions test, we can see that there are some violations such as multicollinearity present with high VIF values. Homoscedasticity also shows randomness with some outliers.

Of the models tested, all the models have performed relatively well at generalization. Even the Linear Regression model showed little to no signs of overfitting thus regularization wouldn't have played a major role here. This is likely due to thanks to the EDA & Feature Engineering performed. Lasso performs the best given the dataset. Regardless, We will propose using the lasso model based on the results presented. 

## 4. Recommendations and Conclusion
From our initial dataset, there were around 80 columns/features. Real-life production models utalize around 30 - 50 features. Having considered the possiblity of an overfitted model and its inefficiencies, we looked to trim the dataset.

To address our problem statement, feature engineering and EDA has been performed to narrow the features down to around 35 columns. In turn, fulfilling what our predictive valuation model was set out to do in our problem statement above.

Ideally, the features of the model may be trimmed further. From our multicollinearity test, there are still many features which share collinearity amongst each other. Further work may be considered to categorize the features according to unique features such as Size, Profile, Time factors, Features, Finishing and Quality. These features would be sufficient to efficiently predict the house prices for the purpose of our problem statement. (Our presentation slides/model uses 17 features)

As for higher valued homes which the model may not perform as well in, it would be advisable that an on-site valuation be handled by human intervention as the model does not perform too well when prices exceed roughly USD 300,000 and up. Though, it is worth noting that the majority of the prices of properties fall under the ~ USD 300,000 price mark. (Given that the data is representative of all properties Ames). Alternatively, gathering of data for the higher valued homes will also help in assisting the model to better predict home prices in excess of USD 300,000.