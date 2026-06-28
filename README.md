# 🏦 Bank Customer Churn Prediction

A machine learning project to predict which bank customers 
are likely to leave (churn) using classification models.

## 📊 Dataset
- **Source:** BankChurners dataset (Kaggle)
- **Rows:** 10,127 customers
- **Features:** 19 features including age, income, 
  transaction count, credit limit, etc.

## 🛠️ Tools & Libraries
- Python, Pandas, NumPy
- Scikit-learn
- XGBoost
- Imbalanced-learn (SMOTE)
- Matplotlib, Seaborn

## 🔄 Project Pipeline
1. Data Cleaning & Preprocessing
2. Exploratory Data Analysis (EDA)
3. Label Encoding of categorical features
4. Train/Test Split (80/20)
5. Class Imbalance handling using SMOTE
6. Model Training (Random Forest & XGBoost)
7. Model Evaluation
8. Feature Importance Analysis

## 📈 Results

| Model | Accuracy | ROC-AUC |
|-------|----------|---------|
| Random Forest | 95% | 0.9828 |
| XGBoost | 97% | 0.9902 |

✅ XGBoost performed best with 97% accuracy and 0.99 ROC-AUC

## 🔑 Key Findings
- Total transaction count is the strongest predictor of churn
- Customers with fewer products are more likely to leave
- Inactive customers over 3 months have higher churn risk