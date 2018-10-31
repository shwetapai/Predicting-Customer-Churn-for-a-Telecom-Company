# Project 3: Summary

## Using Supervised Machine Learning to Predict Customer Churn

**Objective**
Customer churn occurs when customers stop doing business with a company.As customers have multiple options in the telecom industry, predicting customer churn rates are useful in this industry.As the cost of retaining an existing customer is far less than acquiring a new one, my model generates a small prioritized list of customers most vulnerable to churn.That way the company can modify their advertising strategy to retain those customers.

**Method**
I plan to use the IBM telecom dataset available from [kaggle.com](https://www.kaggle.com/blastchar/telco-customer-churn).The raw data contains 7043 rows (customers) and 21 columns (features). The “Churn” column is my target variable.The classification goal is to predict whether the customer will churn(1/0).

Predict variable (desired target): y — has the customer churned? (binary: “1”, means “Yes”, “0” means “No)

I cleaned the dataset to remove the missing variables and hot encoded several categorical variables. I used tableau (link included) to explore the relation between several features andthe target variable.I included all features to predict the target variable (customer churn).

My target variable was unbalanced.So I balanced the target variable with SMOTE (Synthetic Minority Oversampling Technique). With my training data created, I up-sampled minority sample( in our case the 'yes_churn' (customers who churn) sample using the SMOTE algorithm. 



**Model**



