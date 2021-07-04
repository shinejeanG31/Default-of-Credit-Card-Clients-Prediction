# Default-of-Credit-Card-Clients-Prediction
**Description:** 
30000 customer data with 24 variables and a binary variable of default payment are available. 
Three models(Logistic Regression, Neural Network and Random Forests) has been built with model optimization to forecast whether the customer will become a defaulter, achieving the highest Accuracy of 0.82 and AUC of 0.763 by the Logistic Regression Model.
Data sources can be download from here [UCI](https://archive.ics.uci.edu/ml/datasets/default+of+credit+card+clients#)

** **

**Datasets:** 
- The dataset has 30000 observations with 25 variables in which there are 15 numerical variables and 10 categorical variables. The dataset contains a binary variable, default.payment.next.month (Yes = 1, No = 0) as the response variable.

** **

**Goal:** 
- This project aims to predict the potential defaulter at the case of customers default payments from the given variables through classifier model buiding.
- Besides, it is need to identify the factors contributing to defaulting activity, which will provide bank managers with risk control strategies of reducing potential defaulters, by having insight into variable with importance in models. 

** **

**Model Selection:** 
- Logistic Regression: -- Simple to implement\ Easy to interpret feature importance\ Feature scaling not required\ easy to overfit 
- Neural Network:-- "Black box" \High quality\ Good fault tolerance capacity\ Uneasy to identify feature importance\ Small data size may lead to poor performance
- Random Forests、XGboost:-- Tree-based Ensemble method\ Relatively insensitive to skewed data\ Resolution for overfitting\ Performance promotion

**Summary:** 

- All models have relatively low F1 score of 'Default' group. It seems be caused by imbalanced dataset issue due to that there are more samples in 'no Default' group.But we still compare the F1 score of 'default' due to that we more care about the classification power of 'Default' group.

- Comparing f1-score of 'Default', AUC and accuracy of each model, Xgboost model shows the highest performance and Ensemble method show slightly better performance than logistic regression and Neural Network model. The accuracy of each model has little difference while AUC of each one grows slightly from Logistic Regreesion to XGboost.

- PAY_0,BILL_AMT1, PAY_AMT2, and LIMIT_BAL, are considered as the most important features from features importance comparison.we can suggest the features with which clients are more likely to be defaulters, including higher limit balance, high bill amount and low pay amount in the latest few months.

**Discussion:**
- Plotting ROC curve to find the optimal threshold for binary clasification model will improve model performance evaluated by metric AUC primarily.
- Cross validation and hyperparameters tunning for models can actually improve model performance.
- Neural Network has limitation for small size data and uneasy to interpret the feature importance.
- Ensemble method will be good selection for binary classification model buiding.

# Getting Started
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

# Running the tests
- The main script is "Default_of_credit_card_clients.ipynb" notebook, which includes the codes and documentation of exploring the dataset. 
- For more information about model building and optimization, please check notebook.

