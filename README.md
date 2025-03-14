# FindDefault - Credit Card Fraud Detection

## Problem Statement
Credit card fraud is a significant issue in the financial sector, leading to financial losses and reduced consumer trust. The objective of this project is to develop a machine learning model that accurately identifies fraudulent credit card transactions.

## Dataset Source
The dataset used in this project contains transactions made by European cardholders in September 2013. It consists of 284,807 transactions, of which only 492 are fraudulent (0.172%). The features have been transformed using Principal Component Analysis (PCA) to maintain confidentiality.

Dataset Source: [Credit Card Fraud Detection Dataset](https://kh3-ls-storage.s3.us-east-1.amazonaws.com/DS%20Project%20Guide%20Data%20Set/creditcard.csv)

## Data Dictionary
- **Time**: Seconds elapsed since the first transaction.
- **Amount**: Transaction amount.
- **V1 - V28**: Anonymized numerical features from PCA transformation.
- **Class**: Target variable (0 = Legitimate, 1 = Fraudulent).

## Project Pipeline
1. **Data Understanding**
   - Load and explore the dataset.
   - Identify missing values and data inconsistencies.
2. **Exploratory Data Analysis (EDA)**
   - Analyze class imbalance using visualizations.
   - Study statistical distributions of features.
3. **Data Preprocessing**
   - Standardize the "Amount" feature using StandardScaler.
   - Drop the "Time" column.
   - Address class imbalance using Synthetic Minority Over-Sampling Technique (SMOTE).
4. **Train-Test Split**
   - Split the dataset into training (80%) and testing (20%) sets.
5. **Model Selection & Training**
   - Evaluate multiple models:
     - Logistic Regression
     - Random Forest Classifier
     - Support Vector Machine (SVM)
     - XGBoost
   - Perform hyperparameter tuning using GridSearchCV.
6. **Model Evaluation**
   - Metrics Used:
     - Accuracy
     - Precision
     - Recall (Sensitivity)
     - F1-Score
     - ROC-AUC Score
   - Best Model: Random Forest Classifier
   - Hyperparameters tuned: `n_estimators = 100`, `max_depth = None`

## Results
- **Accuracy**: 99.6%
- **Precision**: 92%
- **Recall**: 91%
- **F1-Score**: 91%
- **ROC-AUC Score**: 98%

## Conclusion & Future Work
### Key Takeaways:
- The Random Forest Classifier performed best in detecting fraudulent transactions.
- Feature scaling and data preprocessing significantly improved model performance.
- The F1-score of 91% indicates strong predictive capability.

### Future Improvements:
- Implement real-time fraud detection using streaming data.
- Experiment with deep learning techniques (e.g., LSTMs, Autoencoders).
- Deploy the model via a cloud-based API for real-time transaction monitoring.

## Project Deliverables
- **Notebook Folder**: Contains the Jupyter Notebook with exploratory data analysis and model building.
- **Visuals Folder**: Contains graphs and visualizations of the dataset.
- **Data Folder**: Contains the dataset.
- **Model Folder**: Stores the trained model in `.pkl` format.
- **FindDefault_Report**: Detailed project report.


