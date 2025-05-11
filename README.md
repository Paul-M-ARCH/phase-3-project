
# Phase 3 Project: Proactive Churn Risk Modeling for Telecom Customer Retention

## Overview
Customer churn remains a critical challenge in the telecom industry, where acquiring new customers is often more expensive than retaining existing ones. This project uses supervised machine learning to build a classification model that predicts customer churn based on demographic, usage, and service-related features.
By identifying at-risk customers, telecom providers can proactively intervene to reduce churn, increase retention, and drive long-term revenue growth.

## Business Problem
The telecom company is experiencing notable revenue loss due to customer churn. The business lacks a reliable method to predict which customers are at risk of leaving. The goal is to build a model that predicts churn accurately and provides actionable insights for targeted customer retention efforts.
The key questions are:  
✅ Which customer attributes are most predictive of churn?  
✅ How well can we predict churn using machine learning models?  
✅ What is the trade-off between model accuracy, precision, and recall?  
✅ Which customer segments should be prioritized for retention efforts?  

## 💾 Dataset
Source: IBM Sample Telecom Dataset
File: telecom_churn.csv
Target Variable: churn (yes/no)
Key Features:
- Service usage (e.g., total day minutes, total night calls)
- Plans and subscriptions (e.g., international plan, voice mail plan)
- Support interactions (e.g., customer service calls)
- Account demographics (e.g., state, account length)  

## 🔍 Approach

This project follows a structured machine learning pipeline:
**1. Data Preprocessing & Cleaning
- Removed irrelevant fields (e.g., phone number)
- Converted categorical variables using one-hot encoding
- Transformed target variable (churn) to binary
**2. Exploratory Data Analysis (EDA)
- Analyzed churn distribution across features
- Identified key variables influencing churn behavior
**3. Model Development
- Baseline: Logistic Regression (scaled features)
- Tuned Model: Decision Tree Classifier (max_depth=5, min_samples_split=10)
**4. Model Evaluation
- Evaluated using Accuracy, Precision, Recall, F1-Score
- Assessed model’s ability to detect churners

## 🧪 Results
Logistic Regression
- Accuracy: 86%
- Recall (Churners): 27%
- Precision (Churners): 54%
Performs well on non-churners but poorly at identifying true churners.

## Decision Tree Classifier
- Accuracy: 91%
- Recall (Churners): 62%
- Precision (Churners): 75%
Better balance between churn prediction and overall accuracy.

## Top Features (Decision Tree)
- customer service calls
- international plan
- total day minutes

## 📌 Recommendations
- Target customers with frequent service issues or international plans for retention efforts.
- Use churn predictions to trigger automated outreach or loyalty programs.
- Explore ensemble models (e.g., Random Forest, XGBoost) to further improve performance.

## ⚠️ Limitations
- Class imbalance reduced the model’s recall for minority class (churners).
- Limited feature diversity (no customer satisfaction, billing history, or usage trends).
- Static data snapshot may not fully represent time-based churn behaviors.
- No real-world validation beyond the test split.

## 🚀 Future Improvements
- Implement SMOTE or class weighting to address imbalance
- Explore temporal features or multi-period data
- Deploy model via Flask API or integrate into a CRM system

## 📁 Project Structure
```
📂 Phase-3-Project
 ├── data/                      # Raw and processed dataset  
 ├── images/                    # Images used in README  
 ├── .gitignore  
 ├── phase-3-project.ipynb  # Jupyter Notebook with full analysis  
 ├── presentation.pdf            # Non-technical presentation  
 ├── README.md                   # Project Summary  
```
## ✅ Conclusion
The decision tree model outperformed logistic regression in identifying churners while maintaining strong overall accuracy. It identified clear churn signals such as high service usage, frequent support calls, and international plan subscriptions.



