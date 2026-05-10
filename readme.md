# 📊 Customer Churn Prediction & Risk Analytics Dashboard (ML + Power BI)

## 🧠 Project Overview

This project focuses on predicting customer churn using Machine Learning and visualizing insights through an interactive Power BI dashboard. The goal is to identify high-risk customers and enable proactive retention strategies for business decision-making.

The system combines:
- Data preprocessing (Python)
- Machine Learning (XGBoost model)
- Feature importance analysis
- Power BI dashboard for business insights

---

## 🎯 Business Problem

Telecom companies face significant revenue loss due to customer churn. The objective is to:
- Predict which customers are likely to churn
- Identify key factors driving churn
- Enable targeted retention strategies

---

## 📂 Dataset Description

The dataset contains customer-level information:

| Column | Description |
|--------|------------|
| customerID | Unique customer identifier |
| tenure | Number of months with company |
| MonthlyCharges | Monthly billing amount |
| TotalCharges | Total billing amount |
| Contract | Type of contract |
| InternetService | Internet service type |
| PaymentMethod | Payment method used |
| Churn | Target variable (0 = No, 1 = Yes) |

---

## 🛠️ Technologies Used

### 🐍 Python
- Pandas
- NumPy
- Scikit-learn
- XGBoost
- Label Encoding

### 📊 Power BI
- Data Modeling
- DAX Measures
- Interactive Visualizations

---

## 🔄 Project Workflow

### 1. Data Preprocessing
- Handled missing values in `TotalCharges`
- Converted categorical variables using Label Encoding
- Ensured binary encoding for target variable (Churn)

### 2. Feature Selection
Selected important features:
- tenure
- MonthlyCharges
- TotalCharges
- Contract
- InternetService
- PaymentMethod

---

### 3. Model Building (XGBoost)

- Train-test split with stratification
- XGBoost classifier used for prediction
- Output:
  - Churn Probability
  - Predicted Churn
  - Risk Level classification

---

### 4. Model Evaluation

| Metric | Score |
|--------|------|
| Accuracy | ~0.77 |
| ROC-AUC | ~0.81 |
| Recall (Churn) | ~0.51 |

✔ Strong ability to separate churn vs non-churn customers

---

## ⚠️ Key Insight from Model

- Contract type is the strongest predictor of churn
- Month-to-month customers have higher churn risk
- Higher monthly charges increase churn probability

---

## 📊 Power BI Dashboard Design

### 🟦 Page 1: Executive Overview
- Total Customers
- Churn Rate
- High Risk Customers
- Avg Churn Probability

Visuals:
- Churn distribution
- Risk segmentation
- Contract vs Churn analysis

---

### 🟦 Page 2: Machine Learning Insights
- Feature Importance (XGBoost)
- Churn Probability distribution
- Model performance metrics:
  - Accuracy
  - ROC-AUC
  - Recall

---

### 🟦 Page 3: Customer Risk Analysis
- High Risk Customer Table
- Filters by Risk Level
- Contract and service segmentation

---

## 📌 Key KPIs Used in Power BI

- Total Customers → COUNT(customerID)
- Churn Rate → AVERAGE(Churn)
- High Risk Count → CALCULATE(COUNT(customerID), Risk_Level = "High Risk")
- Avg Churn Probability → AVERAGE(Churn_Probability)

---

## 📤 Output Files

- `telco_ml_output.csv` → ML predictions + risk scoring
- `feature_importance.csv` → Feature importance from XGBoost

---

## 💡 Key Learnings

- Importance of data preprocessing in ML success
- Handling class imbalance in churn datasets
- Integration of ML outputs into BI tools
- Business interpretation of model predictions
- Importance of ROC-AUC over accuracy in classification problems

---

## 📈 Final Outcome

This project delivers a full end-to-end pipeline:

✔ Clean dataset  
✔ Predictive ML model (XGBoost)  
✔ Customer risk segmentation  
✔ Interactive Power BI dashboard  
✔ Business-ready insights  

---

## 🚀 Future Improvements

- SMOTE for class imbalance improvement
- Hyperparameter tuning for XGBoost
- Real-time dashboard integration
- Automated model retraining pipeline

---

## 👨‍💻 Author

**Nasir Hussain**  
Data Science & Analytics Portfolio Project  
