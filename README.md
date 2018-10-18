# Project 3:
## Analyzing customer behavior to predict customer churn rate for a telecom company

**Objective**
Customer churn occurs when customers stop doing business with a company.As customers have multiple options in the telecom industry, predicting customer churn rates are useful in this industry.
Customer churn could be voluntary or involuntary.Voluntary churn occurs due to a decision by the customer to switch to another company, while involuntary churn occurs due to circumstances beyoond the control of the company such as a customer's relocation to a long-term care facility, death, illness etc.I plan to exclude involuntary churn from my analysis.As the cost of retaining an existing customer is far less than acquiring a new one, my model aims to generate a small prioritized list of customers most vulnerable to churn.That way the company can modify their advertising strategy to retain those customers.

**Method**
I plan to use the IBM telecom dataset available from [kaggle.com](https://www.kaggle.com/blastchar/telco-customer-churn).The raw data contains 7043 rows (customers) and 21 columns (features). The “Churn” column is my target variable.I plan to include the following features to predict voluntary customner churn rate.

gender (female, male)

SeniorCitizen (Whether the customer is a senior citizen or not (1, 0))

Partner (Whether the customer has a partner or not (Yes, No))

Dependents (Whether the customer has dependents or not (Yes, No))

tenure (Number of months the customer has stayed with the company)

PhoneService (Whether the customer has a phone service or not (Yes, No))

MultipleLines (Whether the customer has multiple lines r not (Yes, No, No phone service)

InternetService (Customer’s internet service provider (DSL, Fiber optic, No)

OnlineSecurity (Whether the customer has online security or not (Yes, No, No internet service)

OnlineBackup (Whether the customer has online backup or not (Yes, No, No internet service)

DeviceProtection (Whether the customer has device protection or not (Yes, No, No internet service)

TechSupport (Whether the customer has tech support or not (Yes, No, No internet service)

streamingTV (Whether the customer has streaming TV or not (Yes, No, No internet service)

streamingMovies (Whether the customer has streaming movies or not (Yes, No, No internet service)

Contract (The contract term of the customer (Month-to-month, One year, Two year)

PaperlessBilling (Whether the customer has paperless billing or not (Yes, No))

PaymentMethod (The customer’s payment method (Electronic check, Mailed check, Bank transfer (automatic), Credit card (automatic)))

MonthlyCharges (The amount charged to the customer monthly — numeric)

TotalCharges (The total amount charged to the customer — numeric)
