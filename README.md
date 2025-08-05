# IRANIAN TELECOM CUSTOMER CHURN PREDICTION
## Goals

This notebook goal is to come up with a machine learning model to **predict the churn status** of customer

## Dataset

The dataset, collected randomly from an Iranian telecom company's database over 12 months, consists of 3150 rows representing customers, with information of their usage of the service across 13 fields. Notably, all attributes, except *churn*, present aggregated data for the initial 9 months. Churn labels indicate customer states after 12 months, with a designated 3-month planning gap.

**Data Attributes:**

- **`Call Failures`**: Number of call failures
- **`Complains`**: Complain status to show whether the customer complained or not (0: No complaint, 1: Complaint)
- **`Subscription Length`**: Total subscription months of the customer
- **`Charge Amount`**:
- **`Seconds of Use`**: Total seconds that the customer called
- **`Frequency of Use`**: Total number of calls made
- **`Frequency of SMS`**: Total text messages made
- **`Distinct Called Numbers`**: Total distinct phone calls
- **`Age Group`**: Customer age group
- **`Tariff Plan`**: Tariff Plan of the customer
- **`Status`**: Customer active status
- **`Churn`**: Customer churn status
- **`Customer Value`**: Calculated customer value


## Machine Learning Models

### Logistic Regression

#### Default 
<p align="center">
  <img src="https://github.com/tringuyenbao/Iranian-Telecom-Customer-Churn-Prediction/blob/main/images/linear-regression-score.png?raw=true" alt="logistic-regression-score"/>
</p>

#### Hyperparameter tuned
<p align="center">
  <img src="https://github.com/tringuyenbao/Iranian-Telecom-Customer-Churn-Prediction/blob/main/images/hyperparameter-tuned-linear-regression-score.png?raw=true" alt="hyperparameter-tuned-linear-regression-score"/>
</p>

### K-Nearest Neighbors

#### Default 
<p align="center">
  <img src="https://github.com/tringuyenbao/Iranian-Telecom-Customer-Churn-Prediction/blob/main/images/knn-score.png?raw=true" alt="knn-score"/>
</p>

#### Hyperparameter tuned
<p align="center">
  <img src="https://github.com/tringuyenbao/Iranian-Telecom-Customer-Churn-Prediction/blob/main/images/hyperparameter-tuned-knn-score.png?raw=true" alt="hyperparameter-tuned-knn-score."/>
</p>

Use **AUC** value as the ultimate metrics since it shows which models can make the prediction better independently.


| Models      | ROC AUC|
|-------------|----|
| **1. Logistic Regression** | 0.692 |
| **2. Logistic Regression with Hyperparameter Tuning** | 0.8383 |
| **3. k-Nearest Neighbors** | 0.859 |
| **4. k-Nearest Neighbors with Hyperparameter Tuning** | 0.8866 |

**model 4** has the highest AUC value of all. On the other hand, according to the confusion matrix, **model 4** also predicts *both Churn classes* better.

*Assignment 2 of COSC2999 - Practical Data Science With Python RMIT 2024*
