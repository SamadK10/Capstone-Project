# Credit Card Fraud Detection Project

## Problem Statement
The goal of this project is to predict fraudulent credit card transactions using machine learning models.

This project analyzes customer-level data collected during a research collaboration between Worldline and the Machine Learning Group. The dataset, sourced from Kaggle (https://www.kaggle.com/mlg-ulb/creditcardfraud), contains 284,807 transactions, of which 492 are fraudulent. Due to the highly imbalanced nature of the dataset, proper handling is necessary before model building.

## Business Problem Overview
For banks, retaining high-value customers is a top priority. However, banking fraud poses a significant threat, resulting in financial losses and reduced customer trust. According to the Nilson Report (https://nilsonreport.com/upload/content_promo/The_Nilson_Report_Issue_1164.pdf), banking fraud was estimated to reach $30 billion worldwide by 2020. With the rise of digital payment methods, fraudulent transactions are also increasing in number and sophistication.

In the banking industry, fraud detection using machine learning is crucial for proactive monitoring and fraud prevention. Machine learning helps reduce manual review efforts, costly chargebacks, and unnecessary transaction denials.

## Understanding and Defining Fraud
Credit card fraud involves unauthorized use of a credit card for financial gain. Common types of fraud include:
- Skimming: Duplicating card information from the magnetic strip.
- Manipulation or alteration of genuine cards.
- Creation of counterfeit cards.
- Stolen or lost credit cards.
- Fraudulent telemarketing.

## Data Dictionary
The dataset contains credit card transactions from European cardholders over two days in September 2013. It consists of 284,807 transactions, with only 492 classified as fraudulent. The dataset is highly imbalanced, with fraudulent transactions accounting for only 0.172% of the total.

Features:
- **Time**: Seconds elapsed between the first transaction and the current transaction.
- **Amount**: Transaction amount.
- **V1 - V28**: Principal components obtained using PCA for confidentiality.
- **Class**: Target variable (0 = legitimate transaction, 1 = fraudulent transaction).

## Project Pipeline
The project follows these key steps:

1. **Data Understanding**
   - Load and inspect the dataset.
   - Identify key features for model training.

2. **Exploratory Data Analysis (EDA)**
   - Perform univariate and bivariate analyses.
   - Check for skewness and address it if necessary.
   - Identify class imbalance and plan for mitigation.

3. **Train/Test Split**
   - Split the dataset into training and testing sets.
   - Use k-fold cross-validation to ensure balanced class representation.

4. **Model Building & Hyperparameter Tuning**
   - Train different machine learning models.
   - Fine-tune hyperparameters for optimal performance.
   - Apply resampling techniques (e.g., SMOTE) to handle class imbalance.

5. **Model Evaluation**
   - Use appropriate evaluation metrics.
   - Prioritize accurate fraud detection over overall accuracy.
   - Choose metrics that best reflect business objectives, such as precision, recall, and F1-score.

## Conclusion
By leveraging machine learning, this project aims to improve fraud detection accuracy, reduce false positives, and enhance security in credit card transactions.

