# Project 3:
## Detecting fraudulent reviews in Amazon's customer reviews through Sentiment Analysis using Supervised Machine Learning.

**Objective**
E-commerce websites such as Amazon use a large number of customer reviews on almost everything that is sold on their website.The main aim of including reviews is to help other customer in making their buying decision. As customer reviews are an important source of information for future consumers and they have the potential to  increase or decrease the reputation of products or websites.As customer reviews have an huge impact on product sales, there is an incentive for fraudulent actors to post false reviews in order to push their reputation unfairly.So the main aim of my project is to detect such false or unfair reviews.

**Method**
I plan to use Amazon Reviews collection dataset ( available on AWS public dataset).I will focus on reviews for a specific product category.I plan to use StringToWordVector filter to analyze the the main text and classify it as either positive, negative or neutral, depending on presence or absence of particular words in the text.I then plan to use supervised classifiers to classify reviews as positive, negative, or neutral. I aim to predict the models output on the test data and then generating a confusion matrix that classifies the reviews into positive,negative or neutral ones.
I will then use the confuison matrix to find fair and unfair reviews using the following attributes:

• **True Positive Reviews (TPR)**

• **False Positive Reviews (FPR)**

• **True Negative Reviews (TNR)**

• **False Negative Reviews (FNR)**

• **True Neutral Reviews (TNR)**

• **False Neutral Reviews (FNR)**
