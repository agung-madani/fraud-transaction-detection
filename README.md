# Credit Card Fraud Detection using Extra Trees Classifier Model and Over Sampling ADASYN for handling Imbalanced Dataset

This repository contains code for detecting credit card fraud using an Extra Trees Classifier model and oversampling technique ADASYN to handle imbalanced datasets. The main code is adapted from [gpreda](Main-source).

## Introduction
The dataset used contains information about credit card transactions, with a target variable labeled "Class" indicating whether a transaction is legal (0) or fraudulent (1). The main goal is to build a model that can effectively detect fraudulent transactions.

## Dataset Overview
- The dataset consists of 284,807 transactions and 31 features.
- There is a significant class imbalance, with 99.83% of transactions being legal and only 0.17% being fraudulent.

## Data Preprocessing
- Duplicate samples were removed, resulting in a dataset with 283,726 entries.
- There were no missing values in the dataset.
- The data was already standardized, with mean values close to 0 and standard deviations close to 1.

## Exploratory Data Analysis
- A correlation heatmap was generated to analyze the relationships between features.
- Scatter plots were used to visualize the relationship between time, amount, and transaction class.

## Model Training
- The 'Time' and 'Amount' columns were dropped from the dataset.
- The dataset was split into training and testing sets.
- The Extra Trees Classifier model was trained on the oversampled data using the ADASYN technique.
- The model achieved a high ROC-AUC score of 0.987 on the test set, indicating good performance in detecting fraudulent transactions.

## Results
- The model achieved an ROC-AUC of 100% on the validation set and an ROC-AUC of 0.9866095505069398 on the test set.
- Precision, recall, and F1-score were calculated for both classes, showing high performance in detecting fraudulent transactions.

| Class | Precision | Recall | F1-Score | Support |
|-------|-----------|--------|----------|---------|
| 0     | 1.00      | 1.00   | 1.00     | 28,326  |
| 1     | 0.91      | 0.87   | 0.89     | 47      |
|-------|-----------|--------|----------|---------|
| **Accuracy** | | | | 1.00 |
| **Macro Avg** | 0.96 | 0.94 | 0.95 | 28,373 |
| **Weighted Avg** | 1.00 | 1.00 | 1.00 | 28,373 |


## Conclusion
The Extra Trees Classifier model trained using the ADASYN oversampling technique shows promising results in detecting credit card fraud. Further evaluation and optimization may be necessary for deployment in real-world scenarios.

