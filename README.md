# Customer Churn Analysis & Prediction

## Overview

This project analyzes banking customer data to explore churn patterns
and build machine-learning models for predicting whether a customer will
leave the bank.

The dataset contains **10,000 customer records** with demographic,
financial, and account-related attributes. The project includes
exploratory data analysis, data preprocessing, visualization, model
development, and model evaluation.

## Dataset

The original dataset contains customer attributes including:

-   Credit Score
-   Geography
-   Gender
-   Age
-   Tenure
-   Account Balance
-   Number of Products
-   Credit Card Ownership
-   Active Membership Status
-   Estimated Salary
-   Exited (churn target)

The target variable, **Exited**, represents whether a customer left the
bank:

-   `0` --- Customer stayed
-   `1` --- Customer exited

The dataset contains **7,963 customers who stayed** and **2,037
customers who exited**.

## Project Workflow

### 1. Exploratory Data Analysis

The project explores the structure and characteristics of the customer
dataset by:

-   Inspecting dataset dimensions, columns, data types, and unique
    values
-   Identifying numerical and categorical variables
-   Examining customer churn distribution
-   Performing correlation analysis
-   Creating a correlation heatmap
-   Exploring distributions of customer attributes

### 2. Data Preprocessing

Data preparation includes:

-   Removing identifier/non-analytical columns such as `RowNumber`,
    `CustomerId`, and `Surname`
-   Encoding categorical variables
-   Performing feature selection
-   Scaling features for selected machine-learning models
-   Splitting data into training and testing sets
-   Applying SMOTE in selected model pipelines to address class
    imbalance

### 3. Data Visualization

Matplotlib and Seaborn are used to explore customer characteristics and
feature distributions, including:

-   Credit Score
-   Age
-   Tenure
-   Balance
-   Geography
-   Number of Products
-   Credit Card Ownership
-   Active Membership
-   Customer Churn

### 4. Machine-Learning Models

The project experiments with multiple classification approaches:

-   Decision Tree
-   Random Forest
-   Support Vector Machine (SVM)
-   Logistic Regression
-   K-Nearest Neighbors (KNN)
-   XGBoost

Selected models use preprocessing pipelines, SMOTE, and GridSearchCV for
model tuning.

## Model Evaluation

Models are evaluated using metrics such as:

-   Accuracy
-   Precision
-   Recall
-   F1-score
-   Confusion Matrix
-   Classification Report

### Saved Test Results

  ------------------------------------------------------------------------
  Model         Test Accuracy          Churn   Churn Recall Churn F1-Score
                                   Precision                
  ------------ -------------- -------------- -------------- --------------
  XGBoost              85.00%           0.65           0.61           0.63

  Random               84.03%           0.61           0.61           0.61
  Forest                                                    

  Decision             79.73%           0.50           0.68           0.58
  Tree                                                      

  SVM                  77.53%           0.47           0.74           0.57

  Logistic             73.30%           0.37           0.45           0.41
  Regression                                                

  KNN                  49.15%           0.20           0.47           0.28
  ------------------------------------------------------------------------

Among the saved model outputs, **XGBoost achieved the best overall test
accuracy at 85%**, with a churn-class F1-score of **0.63**.

> **Note:** The KNN notebook contains implementation limitations, so its
> reported performance should not be treated as directly comparable with
> the other models.

## Technologies Used

-   Python
-   Pandas
-   NumPy
-   Matplotlib
-   Seaborn
-   Scikit-learn
-   XGBoost
-   imbalanced-learn / SMOTE
-   Jupyter Notebook

## Repository Files

  ------------------------------------------------------------------------
  File                                 Description
  ------------------------------------ -----------------------------------
  `Churn_Modelling.csv`                Original customer churn dataset

  `churn_data.csv`                     Processed customer dataset

  `Data_Analysis.ipynb`                Exploratory data analysis and
                                       preprocessing

  `Data_Vizualisation.ipynb`           Data visualization

  `DecisionTree_Modelling.ipynb`       Decision Tree modeling

  `RandomForest_Modelling.ipynb`       Random Forest modeling

  `SVM_Modelling.ipynb`                Support Vector Machine modeling

  `LinearRegression_Modelling.ipynb`   Custom logistic-regression
                                       classification implementation

  `KNN_Modelling.ipynb`                KNN experiment

  `XGBoost_Modelling.ipynb`            XGBoost modeling and evaluation
  ------------------------------------------------------------------------

## Key Result

The project demonstrates an end-to-end analytical workflow from customer
data exploration and visualization through classification modeling and
evaluation. Among the saved model results, **XGBoost produced the
strongest overall performance with 85% test accuracy**.

## Skills Demonstrated

-   Exploratory Data Analysis (EDA)
-   Data Preprocessing
-   Data Visualization
-   Correlation Analysis
-   Classification
-   Model Evaluation
-   Feature Scaling
-   Class-Imbalance Handling
-   Hyperparameter Tuning

## Disclaimer

This project is an educational machine-learning analysis. Model results
are based on the supplied dataset and saved notebook outputs and should
not be interpreted as production performance on future banking
customers.
