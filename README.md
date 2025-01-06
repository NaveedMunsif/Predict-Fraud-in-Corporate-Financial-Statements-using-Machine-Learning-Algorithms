# Predicting Fraud in Corporate Financial Statements

## Overview
This project implements a machine learning solution for detecting financial fraud in **Canadian publicly traded companies** using an ensemble of **XGBoost** and **Random Forest**.

## Problem Context
Financial fraud causes significant losses annually. Traditional methods struggle with sophisticated fraud schemes. Machine learning helps by identifying subtle patterns in financial data.

## Dataset
The **WLU-CompustatSEC Dataset** was created using:
1. **Compustat Daily Updates (2024)**: Standardized financial data (income statements, balance sheets, cash flows).
2. **Accounting and Auditing Enforcement Releases (AAER, 2021)**: Detailed financial reports ensuring data consistency.

Dataset details:
- **66,920 firm-year records** (1990-2018)
- **45 financial features** (e.g., assets, liabilities, cash flows)
- **Imbalanced class distribution**: 419 fraud cases (0.6%) vs. 66,501 non-fraud cases (99.4%)

## Challenges
1. **Class Imbalance**: Only 0.6% fraud cases, leading to potential model bias.
2. **Asymmetric Costs**: False negatives are costlier than false positives.
3. **Feature Complexity**: Complex relationships between financial metrics and temporal dependencies.

## Methodology
### Why Ensemble Learning?
- Captures complex fraud patterns
- Reduces overfitting risk

### Models:
- **XGBoost**: Handles non-linear relationships, provides feature importance.
- **Random Forest**: Robust to outliers, captures feature interactions.

### Class Imbalance Handling
- Combination of **class weights** and **SMOTE sampling**.

### Performance Metrics
- **AUC-ROC**: Overall discrimination
- **Precision-Recall Curve**: Minority class performance
- **False Positive Rate**: Measures investigation workload
- **Recall**: Priority metric for fraud detection

## Results
- **69% recall** for fraud detection
- **False positive rate below 11%**
- **Overall accuracy: 75%**

## Conclusion
This machine learning solution effectively addresses financial fraud detection in Canadian corporations. Ensemble learning and advanced handling of class imbalance contribute to its robust performance.

---
Explore the code and dataset in this repository!

