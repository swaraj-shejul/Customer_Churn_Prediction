# Customer Churn Prediction using Machine Learning and Deep Learning

## Project Overview

Customer churn is one of the biggest challenges faced by banks and subscription-based businesses. Acquiring new customers is often more expensive than retaining existing ones. This project aims to predict whether a bank customer is likely to leave the bank (churn) based on customer demographics, account details, and banking behavior.

The project follows a complete AI/ML Learning pipeline including data cleaning, exploratory data analysis (EDA), feature engineering, model building, evaluation, and model comparison.

---

## Business Problem

Banks lose revenue when customers close their accounts and switch to competitors. 

### Objective

Predict whether a customer will churn or not so that the bank can proactively take retention actions.

### Target Variable

* Exited = 1 → Customer Churned
* Exited = 0 → Customer Retained

This is a **Binary Classification Problem**.

---

## Dataset Information

### Dataset

Bank Customer Churn Dataset

### Features

| Feature         | Description              |
| --------------- | ------------------------ |
| CreditScore     | Customer credit score    |
| Geography       | Customer country         |
| Gender          | Male/Female              |
| Age             | Customer age             |
| Tenure          | Years with bank          |
| Balance         | Account balance          |
| NumOfProducts   | Number of bank products  |
| HasCrCard       | Credit card ownership    |
| IsActiveMember  | Active membership status |
| EstimatedSalary | Estimated salary         |
| Exited          | Target Variable          |

---

## Data Cleaning

The following preprocessing steps were performed:

* Removed unnecessary columns:

  * RowNumber
  * CustomerId
  * Surname

* Checked and handled:

  * Missing values
  * Duplicate records
  * Data types

* Label Encoding:

  * Gender:

    * Male = 1
    * Female = 0

* One-Hot Encoding:

  * Geography column

---

## Exploratory Data Analysis (EDA)

Performed:

* Univariate Analysis
* Bivariate Analysis
* Feature vs Target Analysis
* Distribution Analysis
* Correlation Analysis

Visualization techniques used:

* Histograms
* Count Plots
* Box Plots
* Correlation Heatmaps

---

## Feature Engineering

* Label Encoding
* One-Hot Encoding
* Feature Selection
* Train-Test Split (80:20)

---

## Models Implemented

### 1. Single Layer Perceptron

* Accuracy: 81.2%
* Recall: 20.6%
* F1 Score: 30.0%
* ROC-AUC: 58.3%

---

### 2. Multi-Layer Perceptron (MLP)

Architecture:

Input → 22 Neurons → Output

Results:

* Accuracy: 86.1%
* Recall: 47.3%
* F1 Score: 57.7%
* ROC-AUC: 71.6%

---

### 3. Deep Neural Network (DNN)

Architecture:

Input → 22 Neurons → 11 Neurons → Output

Results:

* Accuracy: 86.3%
* Recall: 50.9%
* F1 Score: 59.3%
* ROC-AUC: 72.9%

---

### 4. Decision Tree

Best Configuration:

* Max Depth = 6

Results:

* Accuracy: 86.0%
* Recall: 45.3%
* F1 Score: 56.0%
* ROC-AUC: 70.6%

---

### 5. Random Forest

Best Configuration:

* n_estimators = 500

Results:

* Accuracy: 86.55%
* Recall: 46.8%
* F1 Score: 57.8%
* ROC-AUC: 71.5%

---

### 6. XGBoost (Final Model)

Configuration:

* n_estimators = 500
* learning_rate = 0.03
* max_depth = 4
* subsample = 0.8
* colsample_bytree = 0.8

Results:

* Accuracy: 86.7%
* Precision: 74%
* Recall: 50.1%
* F1 Score: 60.0%
* ROC-AUC: 72.9%

---

## Model Comparison

| Model         | Accuracy | Recall | F1 Score | ROC-AUC |
| ------------- | -------- | ------ | -------- | ------- |
| Perceptron    | 81.2%    | 20.6%  | 30.0%    | 58.3%   |
| MLP           | 86.1%    | 47.3%  | 57.7%    | 71.6%   |
| DNN           | 86.3%    | 50.9%  | 59.3%    | 72.9%   |
| Decision Tree | 86.0%    | 45.3%  | 56.0%    | 70.6%   |
| Random Forest | 86.55%   | 46.8%  | 57.8%    | 71.5%   |
| XGBoost       | 86.7%    | 50.1%  | 60.0%    | 72.9%   |

---

## Final Model Selection

XGBoost was selected as the final model because it achieved the best overall balance between:

* Accuracy
* Precision
* Recall
* F1 Score
* ROC-AUC

The model demonstrated strong predictive performance while maintaining good generalization on unseen data.

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-Learn
* TensorFlow / Keras
* XGBoost
* Jupyter Notebook

---

## Project Structure

```text
Customer_Churn_Prediction/
│
├── data/
│   └── Churn_Modelling.csv
|   └── cleaned_customers_churn_data.xlsx
|
│
├── notebooks/
│   ├── Data_cleaning_&_Transformation.ipynb
│   ├── Mode_l_Perceptron.ipynb
│   ├── Model_2_MLP.ipynb
│   ├── Model_3_DNN.ipynb
│   ├── Model_4_Decision_tree.ipynb
│   ├── Model_5_Random_Forest.ipynb
│   └── model_6_XGBoost.ipynb
│
├── models/
│   └── churn_model.pkl
│
├── requirements.txt
├── README.md
```

---

## Future Improvements

* Hyperparameter Optimization using GridSearchCV
* Model Deployment using Flask/FastAPI
* Docker Containerization
* Cloud Deployment
* Real-Time Churn Prediction Dashboard

---

## Author

Swaraj Shejul

AI/ML Engineering Project Portfolio