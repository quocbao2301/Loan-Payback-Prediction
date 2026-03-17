# 📊 Loan Payback Prediction Using Machine Learning

## 📌 Project Overview
This project aims to predict whether a borrower will successfully repay a loan using machine learning techniques. The goal is to support financial decision-making by identifying high-risk applicants and reducing potential losses.

This is a **binary classification problem**, where:
- `1` = Loan Paid Back
- `0` = Loan Not Paid Back

---

## 🎯 Objectives
- Perform exploratory data analysis (EDA) to understand the dataset
- Handle imbalanced data effectively
- Train and compare multiple machine learning models
- Select the best model based on evaluation metrics
- Provide insights for financial risk prediction

---

## 📂 Dataset
- **Number of observations:** ~594,000  
- **Number of features:** 13  

### 🔑 Key Features:
- `income` — Annual income of the borrower  
- `loan_amount` — Amount of the loan  
- `interest_rate` — Interest rate of the loan  
- `credit_score` — Borrower's credit score  
- `dti` — Debt-to-income ratio  
- `employment_status` — Employment condition  
- `loan_paid_back` — Target variable  

---

## 📊 Exploratory Data Analysis (EDA)
- Checked missing values and data types  
- Visualized feature distributions using histograms and boxplots  
- Analyzed correlations between variables  
- Identified **class imbalance**:
  - ~80% loans paid back  
  - ~20% loans not paid back  

---

## ⚙️ Data Preprocessing
- One-hot encoding for categorical variables  
- Feature scaling using StandardScaler  
- Train-test split (stratified)  
- Handled class imbalance using:
  - `scale_pos_weight` (for XGBoost)
  - Class weighting techniques  

---

## 🤖 Machine Learning Models
The following models were trained and compared:

- Logistic Regression  
- Decision Tree  
- Random Forest  
- Gradient Boosting  
- XGBoost  

---

## 📈 Model Evaluation
Models were evaluated using:

- Accuracy  
- Precision  
- Recall  
- F1-score  
- ROC-AUC  

⚠️ Due to class imbalance, **F1-score and ROC-AUC** were the most important metrics.

---

## 🏆 Best Model: XGBoost
XGBoost achieved the best performance:

- Highest ROC-AUC (~0.92)  
- Strong F1-score  
- Better handling of imbalanced data  

### ✅ Why XGBoost?
- Uses boosting to improve difficult predictions  
- Handles non-linear relationships effectively  
- Includes regularization to prevent overfitting  
- Supports `scale_pos_weight` for imbalanced datasets  

---

## 📊 Visualizations
The project includes:
- ROC Curve  
- Confusion Matrix Heatmap  
- Model Comparison Bar Chart  

---

## 🧠 Key Insights
- Class imbalance significantly affects model performance  
- Ensemble methods outperform simple models  
- XGBoost provides the most balanced and reliable predictions  

---

## 🚀 Future Improvements
- Hyperparameter tuning using GridSearchCV  
- Try additional models (e.g., LightGBM, CatBoost)  
- Feature engineering for better performance  
- Deploy model as a web application  

---

## 🛠️ Technologies Used
- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- XGBoost  
- Matplotlib & Seaborn  

---

## 📎 Project Structure
├── data/
├── notebooks/
│ └── Loanpayback_Prediction.ipynb
├── images/
├── README.md

---
## 📊 Results Visualization
![ROC Curve](images/roc_curve.png)
![Confusion Matrix](images/confusion_matrix.png)
![Model Comparison](images/model_comparison.png)

---

## 🙋 Author
**Trần Quốc Bảo**  
Bachelor of Applied Statistics  
Interested in Machine Learning & Financial Risk Modeling  
