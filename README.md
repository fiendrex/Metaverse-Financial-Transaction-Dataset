# Metaverse-Financial-Transaction-Dataset
## Project Overview

This repository contains the analysis and machine learning model development for detecting anomalous and high-risk transactions within a simulated Metaverse environment. The goal is to classify transactions based on various features to identify potential fraud or suspicious activity.

---

## Dataset Description

The analysis is based on the `metaverse_transactions_dataset.csv` file. It contains features related to the transaction itself, the users involved, and behavioral metrics.

| Column Name | Data Type | Description |
| :--- | :--- | :--- |
| `timestamp` | Object | Date and time of the transaction. |
| `hour_of_day` | Integer | Hour (0-23) when the transaction occurred. |
| `sending_address` | Object | Unique wallet address of the sender. |
| `receiving_address` | Object | Unique wallet address of the receiver. |
| `amount` | Float | The value of the transaction. |
| `transaction_type` | Object | Type of transaction (e.g., 'transfer', 'purchase', 'sale'). |
| `location_region` | Object | Geographic region where the transaction originated. |
| `ip_prefix` | Float | Anonymized IP address prefix for location tracking. |
| `login_frequency` | Integer | Frequency of the user's logins. |
| `session_duration` | Integer | Duration of the user's session in the Metaverse (e.g., in minutes). |
| `purchase_pattern` | Object | Categorization of the user's purchase behavior (e.g., 'focused', 'high_value'). |
| `age_group` | Object | Age categorization of the user (e.g., 'established', 'veteran', 'new'). |
| `risk_score` | Float | Pre-calculated numerical risk score associated with the transaction. |
| **`anomaly`** | Object | **Target Variable:** The final risk classification ('low_risk', 'moderate_risk', 'high_risk', 'anomaly'). |

---

## Machine Learning Model Summary

The following classification models were developed and evaluated for predicting transaction risk based on the **`anomaly`** target variable.

| Model | Task | Key Preprocessing Steps | Accuracy Score | F1-Score (Anomaly Class) | Notes |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Logistic Regression** | Classification | (Include details like Scaling, Encoding) | 97% | (Score Here) | A strong baseline linear model. |
| **Support Vector Machine (SVM)** | Classification | (Include details like Scaling, Encoding) | 93% | (Score Here) | Performed slightly lower than other models. |
| **K-Nearest Neighbors (KNN)** | Classification | (Include details like Scaling, Encoding) | **98%** | (Score Here) | **One of the top-performing models.** |
| **Gradient Boosting** | Classification | (Include details like Hyperparameter Tuning) | **98%** | (Score Here) | **One of the top-performing models.** |
| **Naive Bayes** | Classification | (Include details like Feature Transformation) | 85% | (Score Here) | The lowest performing model, likely due to feature dependency assumptions. |

---

## Conclusion

The **K-Nearest Neighbors (KNN)** and **Gradient Boosting** models achieved the highest performance with an **Accuracy Score** of **98%** on the validation dataset. Further focus should be placed on evaluating the **F1-Score** for the minority 'anomaly' class to ensure effective detection of high-risk transactions.

