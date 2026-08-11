# 🏦 Bank Customer Churn Prediction

A machine learning project to predict which bank customers are likely to leave (churn) using classification models — helping banks take proactive steps to retain valuable customers before it is too late.

---

## 📌 Why This Matters

Customer churn costs banks millions every year. Acquiring a new customer is 5 to 7 times more expensive than retaining an existing one. By predicting which customers are likely to leave before they actually do, banks can intervene with targeted offers, improved service, or personalised outreach — saving both the customer relationship and significant revenue.

This project builds a model that identifies at-risk customers with 97% accuracy using real transaction and demographic data.

---

## 📊 Dataset

- **Source:** BankChurners dataset (Kaggle)
- **Rows:** 10,127 customers
- **Features:** 19 features including age, income, transaction count, credit limit, months on book, and total relationship count
- **Class Imbalance:** Only ~16% of customers churned — handled using SMOTE oversampling

---

## 🛠️ Tools and Libraries

- Python, Pandas, NumPy
- Scikit-learn
- XGBoost
- Imbalanced-learn (SMOTE)
- Matplotlib, Seaborn

---

## ⚙️ Project Pipeline

1. Data Cleaning and Preprocessing
2. Exploratory Data Analysis (EDA)
3. Label Encoding of categorical features
4. Train/Test Split (80/20)
5. Class Imbalance handling using SMOTE
6. Model Training — Random Forest and XGBoost
7. Model Evaluation
8. Feature Importance Analysis

---

## 📈 Results

| Model | Accuracy | ROC-AUC |
|-------------|----------|---------|
| Random Forest | 95% | 0.9828 |
| XGBoost | 97% | 0.9902 |

✅ XGBoost performed best with **97% accuracy** and **0.99 ROC-AUC**

---

## 🔍 Key Findings

- **Total Transaction Count** was the single strongest predictor of churn — customers with fewer transactions in the last 12 months were significantly more likely to leave
- **Total Revolving Balance** and **Total Relationship Count** were also among the top predictors — customers with low engagement across products churned at much higher rates
- **Age and Income** had relatively low predictive power compared to behavioural features, suggesting that what customers *do* matters far more than who they *are*
- Class imbalance (only 16% churners) was a key challenge — SMOTE oversampling was critical to prevent the model from simply predicting everyone stays

---

## 📉 Model Evaluation Detail

**XGBoost — Final Model**

| Metric | Churned (1) | Not Churned (0) |
|--------|------------|-----------------|
| Precision | 0.96 | 0.97 |
| Recall | 0.95 | 0.98 |
| F1 Score | 0.95 | 0.97 |

**Interpretation:** The model correctly identifies 95% of customers who will actually churn — meaning the bank would catch 19 out of every 20 customers at risk before they leave.

---

## 🚀 How to Run This Project

**Step 1 — Clone the repository**
```bash
git clone https://github.com/rifathunzai/Bank-churn-prediction.git
cd Bank-churn-prediction
```

**Step 2 — Install required libraries**
```bash
pip install -r requirements.txt
```

**Step 3 — Open the notebook**
```bash
jupyter notebook notebook.ipynb
```

**Step 4 — Run all cells** from top to bottom. The notebook will load the dataset, preprocess it, train both models, and display all evaluation results and visualisations.

---

## 🔮 Future Improvements

- **Hyperparameter tuning** using GridSearchCV or Optuna to push accuracy further
- **SHAP values** for more interpretable feature importance explanations
- **Deploy as a web app** using Streamlit so bank analysts can input customer data and get a real-time churn probability score
- **Test additional models** — LightGBM and CatBoost for comparison
- **Add a cost-benefit analysis** — calculate the actual financial value of correctly identifying one churning customer versus the cost of unnecessary retention offers

---

## 👩‍💻 About

Built by **Rifat Mansoor** — BS Business Analytics student at FAST-NUCES Islamabad.

This project is part of an ongoing portfolio in data analytics and machine learning.

📧 rifathunzai288@gmail.com
🔗 [GitHub Profile](https://github.com/rifathunzai)

---

*Dataset source: [Kaggle — Credit Card customers](https://www.kaggle.com/datasets/sakshigoyal7/credit-card-customers)*
