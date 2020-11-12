# loan risk
This project aims to develop a robust module for predicting your chances of loan approval. The features used for prediction are considered to be available at the time of loan origination. The prediction model has been built separately for Individual Applicants and Joint Applicants with a maximum accuracy. Few highly correlated features such as Grade, Sub Grade, Interest Rate are estimated using the provided FICO score by the applicant. 

# Report
The aim of the project is develop and end to end application that helpls a user to determine his chances of getting a loan.

* Data Overview
The  data was acquired from kaggle and consist of 2,195,670 rows and 151 columns. The target column was identied as loan_status. 
For this analysis only Fully Paid Laons and Charged off/Default Loans have been taken into consideration, which reduced the data set to 1,344,251 rows and 151 columns.

* Data Cleaning
Missing Data: The threshold value for missing data was set to 50%. 
For categorical features: Features with the same 1 category in the data set would not have provided any information to the model hence their removal.
This reduced the number of features from 31 to 26.
For numerical features: Any feature with very little variance would not be very informative for the model.

* Feature Engineering
Series of manipulations were done and new few features were enginered based on domain knowledge.

* Feature Scaling
The data was normalized by taking the mean and standard deviation of each feature based on the first 2 digits of the zip codes.

* Deployment and Machine Learning 
There are 18 variables and 1 response variable, however some features were removed based on their f-score. 
Machinel learning models applied:
1.Logistic Regression
2.Gradient Boosting Classifier
3.Random Forest Classifier
4.XGBoost Classifier
5.Support Vectore Classifier
6. K-Nearest Classifier

Metrics used to compare Machine learning models:
1. AUC Score and ROC curve, hyperparameter tuning was done to the model which increased the AUC score from 0.69 to 0.71
2. Precision-Recall Curve

The model is saved into .pkl type which can be loaded anywhere.

The website was built using flask web framework and deployed to heroku server.

The visualization was done in Tableau.

