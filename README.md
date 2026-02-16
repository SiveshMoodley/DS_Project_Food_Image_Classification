# Food Image Classification

## Project Overview
- 

## Code and Resources
Python Version: 3.10

Packages: pandas, numpy, matplotlib, seaborn, scikit-learn, imbalanced-learn, xgboost

Python Requirements: pip install -r requirements.txt

## Dataset
Source: MIT Professional Education

Type: Educational / Synthetic Dataset

The dataset represents images of food in .img format.
- 

The data is intended for educational and model development rather than commercial credit decisions. No personal or real customer information is included.

## Data Preprocessing
The data was cleaned such that it was usable for the model. I conducted the following process:
- 

The data was prepared and split into training and test sets, with a 20% test size. Numerical features were scaled where required and categorical variables were encoded prior to modeling.

## EDA
Conducted exploratory analysis to examine the distributions of numerical variables and the frequency of categorical features. Key observations include:
- 
  
## Model Building
Multiple classification models were trained and evaluated:
- 

To address class imbalance, SMOTE was applied to improve minority class representation during training. Hyperparameter tuning was conducted using cross-validation prior to evaluation on the test set.

## Model Performance
Models were evaluated using Accuracy, ROC-AUC, Precision, and Recall, with particular focus on recall for defaulters.

- 

## Project Evaluation
- 
