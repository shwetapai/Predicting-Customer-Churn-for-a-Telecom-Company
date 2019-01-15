# Project 3: Using Supervised Machine Learning to Predict Customer Churn

**Objective**

Customer churn occurs when customers stop doing business with a company.As the cost of retaining an existing customer is far less than acquiring a new one, maintaining a healthy customer base is important for the success of any business.As customers have multiple options in the telecom industry, the churn rate is particularly high in this industry.Individualized customer retention is difficult because businesses usually have a lot of customers and cannot afford to spend much time on one. The costs would be too high and would outweigh the extra revenue.But if a company could predict in advance which customers are at risk of leaving, they could focus customer retention efforts by directing them solely toward such  "high risk" customers.

The main objective of my project was to build a predictive model to generate a  prioritized list of customers most vulnerable to churn.

**Method**

I used the IBM telecom dataset available from [kaggle.com](https://www.kaggle.com/blastchar/telco-customer-churn).The raw data contained 7043 rows (customers) and 21 columns (features). The “Churn” column was my target variable.The classification goal was to predict whether the customer will churn(1/0).

Predict variable (desired target): y — has the customer churned? (binary: “1”, means “Yes”, “0” means “No)

I cleaned the dataset to remove the missing variables and hot encoded several categorical variables. I explored the  correlation between several features and the target variable.I then used a correlation matrix to explore if there was any correlation between different features.I included all features to predict the target variable (customer churn).

My target variable was unbalanced.So I balanced the target variable with SMOTE (Synthetic Minority Oversampling Technique). With my training data created, I up-sampled minority sample( in our case the 'yes_churn' (customers who churn) sample using the SMOTE algorithm. 


**Model**

After testing several models, I fit a logistic regression model using all of the features.The AUC for the model was 0.84. I used recall (sensitivity) as my main metric.The sensitivity, which is a measure of the true positive rate (TP/(TP+FN)), was 79%.This tells us that the model has correctly identified 79% of customers that actually churned.

**Cost Evaluation**

 I was interested in exploring the cost implications of implementing, vs. not implementing a predictive model.There were costs associated with the model erroneously assigning false positives and false negatives. It was important to look at similar costs associated with correct predictions of true positives and true negatives. Because the choice of the threshold affects all four of these statistics,it was important to consider the relative costs to the business for each of these four outcomes for each prediction.

I  made the following cost assumptions to explore the cost implications of implementing the model.

1. I assigned the true negatives the cost of USD 0. My model essentially correctly identified a happy customer in this case, and I don’t need to do anything.

2. False negatives were the most problematic, because they incorrectly predict that a churning customer will stay. I will lose the customer and will have to pay all the costs of acquiring a replacement customer, including foregone revenue, advertising costs, administrative costs, etc. I will assume USD 500. This is the cost of false negatives.

3. Finally, for customers that my model identifies as churning, I will assume a retention incentive in the amount of USD 100.This is the cost of both true positive and false positive outcomes.In the case of false positives (the customer is happy,but the model mistakenly predicted churn),I will “waste” the USD 100 concession.

It’s clear that false negatives are substantially more costly than false positives. Instead of optimizing for total error,I selected a model that minimized a cost function ( basically minimized the number of false negatives)  that looks like this:

**500∗FN(C)+0TN(C) + 100∗FP(C)+100TP(C)**

C:Count


**Conclusion**

In order to maintain their current customer base, using the current logistic regression model will save the company USD 135,800 in a month.So its worth investing in optimizing the model further to increase cost savings.I used a default threshold of 0.5 for my logistic regression model.if we lower the threshold further, the cost per customer decreases (from $148 to $90).This results in further cost savings.


**Future Work**

I want to optimize the sensitivity of the model (further decrease the number of false negatives).If I had more time, I would invest more in feature engineering and try and include more important features from other datasets.Fot future work, I also want identify the root causes as to why customers leave as it would help in fine tuning re-acquisition strategies.







