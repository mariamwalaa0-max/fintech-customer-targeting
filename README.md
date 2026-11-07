# Smart Customer Targeting — FinTech Machine Learning

## Project Overview

This project uses machine learning to predict customer subscription to a bank term deposit and support data-driven marketing decisions.

The main objective is to identify customers with higher subscription propensity, allowing financial institutions to prioritize outreach when marketing resources are limited.

## Business Problem

A financial institution has thousands of customers but a limited marketing budget.

Instead of contacting every customer, the institution wants to identify the top 20% most likely to subscribe to a financial product.

**Goal:** Build a binary classification model that predicts subscription probability and ranks customers for targeted marketing.

## Dataset

**Source:** [UCI Bank Marketing Dataset](https://archive.ics.uci.edu/dataset/222/bank%2Bmarketing)

- 45,211 observations
- 16 original input features
- Target: `y` (yes/no)
- Domain: Banking and Direct Marketing

The dataset is publicly available and contains historical marketing campaign information.

## Technologies Used

- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- Jupyter Notebook

## Methodology

1. **Exploratory Data Analysis:** Studied customer characteristics, account balances, loans, and previous campaign history.
2. **Data Preprocessing:** Handled unknown values, applied One-Hot Encoding and Standard Scaling.
3. **Model Training:** Trained Logistic Regression and Random Forest classifiers.
4. **Model Evaluation:** Compared Accuracy, Precision, Recall, F1 Score, Average Precision, and Precision@20%.
5. **Feature Importance:** Used permutation importance to investigate predictive features.

## Model Results

Results on the validation dataset:

| Metric | Logistic Regression | Random Forest |
|---|---:|---:|
| Accuracy | 0.894 | 0.894 |
| Precision | 0.675 | 0.697 |
| Recall | 0.175 | 0.165 |
| F1 Score | 0.278 | 0.267 |
| Average Precision | 0.348 | 0.397 |
| Precision@20% | 27.36% | 30.09% |

**Selected model (preliminary): Random Forest**

Random Forest achieved stronger customer-ranking performance, with a Precision@20% of 30.09%, compared to a validation baseline subscription rate of approximately 11.71%.

This represents a Lift@20% of approximately 2.57x.

## Key Findings

- Previous campaign outcomes were particularly important for predicting subscriptions.
- Customers with higher account balances generally showed higher subscription rates.
- Customers without housing or personal loans showed higher subscription rates.
- Subscription behavior varied across age groups and customer occupations.

These findings represent statistical associations rather than causal effects.

## Limitations and Future Improvements

- Results are currently based on a random validation split.
- Final evaluation on the held-out test set is pending.
- The dataset represents historical banking campaigns and may not reflect current FinTech customer behavior.
- Further work includes pipeline consolidation, temporal validation review, model tuning, and fairness assessment.

## Author

Mariam Walaa Gamal

Machine Learning & Data Science Portfolio Project