# bank-customer-churn-prediction
A machine learning project to predict bank customer churn using Python
# Predicting Bank Customer Churn

## 📖 Project Overview
This project aims to predict customer churn for a bank. Using machine learning, we can identify customers who are most likely to leave and understand the key factors driving their decision. This allows the bank to take proactive measures to improve customer retention.

## 📊 Dataset
The dataset contains information on 10,000 bank customers and includes features such as:
- **Demographics:** CreditScore, Geography, Gender, Age
- **Account Information:** Tenure, Balance, NumOfProducts, HasCrCard, IsActiveMember, EstimatedSalary
- **Target Variable:** `Exited` (1 if the customer closed the account, 0 otherwise)

## 🎯 Project Goals
1. **Analyze** and explore the data to find patterns and correlations with customer churn.
2. **Build** a predictive model with high accuracy and recall for the churn class.
3. **Interpret** the model using SHAP values to provide actionable business insights.
4. **Recommend** data-driven strategies to help the bank reduce customer churn.

## 🛠️ Tech Stack
- **Language:** Python
- **Libraries:** Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, XGBoost, Imbalanced-learn, SHAP
- **Environment:** Jupyter Notebook

## 📈 Key Steps
1. **Data Preprocessing:** Handled class imbalance using SMOTE and scaled numerical features.
2. **Exploratory Data Analysis (EDA):** Uncovered that customers from Germany, older customers, and inactive members have a significantly higher churn rate.
3. **Modeling:** Trained and compared multiple classifiers (Logistic Regression, Random Forest, XGBoost). XGBoost performed best.
4. **Evaluation:** Focused on precision and recall for the churn class, alongside ROC-AUC.
5. **Interpretation:** Used SHAP to explain model predictions and identify the most important features driving churn.

## 📋 Results
The final Random Forest model achieved the following results on the test set:
- **Accuracy:** 0.82
- **Precision (Churn Class):** 0.83
- **Recall (Churn Class):** 0.82
- **ROC-AUC Score:** 0.839

### Feature Importance
The top 5 most important features for predicting churn were:
1. **Age**
2. **Balance**
3. **EstimatedSalary**
4. **IsActiveMember**
5. **CreditScore**

![SHAP Summary Plot](images/shap_summary_plot.png)
## 💡 Business Insights & Recommendations
- **Senior Customer Programs:** Create tailored products and services for older customers who are at higher risk.
- **Target Inactive Members:** Launch re-engagement campaigns for customers marked as inactive.
- **Product Bundling:** Encourage customers with only one product to adopt a second product, as having more products showed stronger loyalty.

## 🚀 Installation & Usage
1. **Clone the repository:**
   ```bash
git clone https://github.com/hungngtom/bank-customer-churn-prediction.git
cd bank-customer-churn-prediction
