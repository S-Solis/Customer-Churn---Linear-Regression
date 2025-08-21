# Customer Churn - Logistic-Regression
Author: Stephanie Solis
## Project Brief
This is a simple logistic regression model built with Python in Jupyter Notebooks. The model predicts the likelihood that a customer of a financial institution will leave.
This project uses [scikit learn's logistic regression](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html) for the machine learning model. It uses a [dataset available on Kaggle](https://www.kaggle.com/datasets/kartiksaini18/churn-bank-customer) that contains data for 10,000 customers of an unnamed financial institution.

## Project Outline
### Part 0: Prepare the Data for Model Training
In this section, the data is loaded into a dataframe, split into the features vs. target, split into training and testing datasets (75% and 25% respectively), and one-hot encoded for all categorical features.

### Part 1: Build the Logistic Regression Model
In this section, a logistic regression model is built using sklearn.linear_model.LogisticRegression. Predictions on the test data are built using [predict_proba](https://scikit-learn.org/stable/modules/generated/sklearn.linear_model.LogisticRegression.html#sklearn.linear_model.LogisticRegression.predict_proba).

Once the predictions are calculated, [matplotlib.pyplot.hist](https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.hist.html) is used to build the below churn probability distribution:
<img width="376" height="278" alt="image" src="https://github.com/user-attachments/assets/02c0c945-178b-4a8e-a61a-0d8e8195b7d9" />

### Part 2: Build Churn Categorization Categories and Productionalize List
Based on the Churn Risk Distribution above, this section categorizes members into the below churn risk buckets:

1: Low churn risk. 0 - <.2
2: Mild churn risk. 0.2 - <0.3
3: Moderate churn risk. 0.3 - <0.4
4: High churn risk. >=0.4

The list of customers sorted by churn risk are saved as customers_by_churn_risk.csv.

## Resources
