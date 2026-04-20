# 📊 Loan Payback Prediction (End-to-End Machine Learning Project)

## 📌 Overview

This project builds a **loan default prediction system** using a large-scale financial dataset. The objective is to predict whether a borrower will repay a loan based on demographic and financial features.

The project demonstrates a **complete machine learning pipeline**, including data preprocessing, feature engineering, model training, evaluation, and deployment-ready prediction.

---

## 🎯 Problem Statement

Accurately predicting loan repayment is critical for:

* Reducing financial risk
* Improving credit decision-making
* Identifying high-risk applicants

This is a **binary classification problem**:

* **1 → Loan Paid Back**
* **0 → Default**

---

## 📂 Dataset

* Source: Kaggle
* Size: **~594,000 rows × 13 features**
* Type: Mixed (numerical + categorical)

### Key Features:

* Annual Income
* Credit Score
* Debt-to-Income Ratio
* Loan Amount
* Interest Rate
* Employment Status
* Loan Purpose
* Credit Grade

### Target:

* `loan_paid_back` (binary)

---

## 🔍 Key Challenges

* **Class imbalance (80% paid / 20% default)**
* Mixed data types (categorical + numerical)
* Real-world noisy financial data

---

## ⚙️ Data Processing & Feature Engineering

### ✔ Data Cleaning

* Standardized categorical values
* Removed duplicates
* Verified no missing values

### ✔ Feature Engineering

* Converted credit grade (`grade_subgrade`) → numerical scale
* Created **default indicator**
* Engineered combined categorical features (`employment + grade`)
* Introduced **sample weighting** to handle imbalance

---

## 🧠 Machine Learning Pipeline

### 🔧 Preprocessing

* Numerical features → **StandardScaler**
* Categorical features → **OneHotEncoder**
* Combined using **ColumnTransformer**

### 🚀 Models Trained

* Logistic Regression
* Decision Tree
* Random Forest
* Gradient Boosting
* **XGBoost (Best Model)**

---

## ⚖️ Handling Imbalanced Data

* Applied **sample weighting (w)**
* Used **scale_pos_weight in XGBoost**
* Ensured fair model evaluation

---

## 🔍 Model Evaluation

### Metrics Used:

* Accuracy
* Precision
* Recall
* F1-score
* **ROC-AUC (primary metric)**

---

## 🏆 Results

| Model               | Accuracy | F1 Score | ROC-AUC  |
| ------------------- | -------- | -------- | -------- |
| Logistic Regression | 0.84     | 0.89     | 0.91     |
| Decision Tree       | 0.86     | 0.91     | 0.90     |
| Random Forest       | 0.84     | 0.90     | 0.91     |
| Gradient Boosting   | 0.84     | 0.90     | 0.92     |
| **XGBoost**         | **0.87** | **0.91** | **0.92** |

### ✅ Best Model: XGBoost

* **ROC-AUC: 0.92**
* Strong balance between precision and recall
* Best performance on imbalanced dataset

---

## 📈 Model Insights

* Credit score, income, and loan grade are key predictors
* Higher-grade loans → higher repayment probability
* Model effectively distinguishes high-risk borrowers

---

## 💡 Interactive Prediction System

The project includes a **custom prediction function**:

### Features:

* Accepts user input (loan application details)
* Outputs:

  * Approval / Denial decision
  * Repayment probability

### Example Output:

```
RESULT: ✅ APPROVED  
REPAYMENT CONFIDENCE: 92.70%
```

👉 Simulates a real-world **loan approval system**

---

## 🛠️ Tech Stack

* Python
* Pandas, NumPy
* Scikit-learn
* XGBoost
* Matplotlib, Seaborn

---

## 🚀 How to Run

```bash
# Clone repo
git clone https://github.com/quocbao2301/Loan-Payback-Prediction

# Install dependencies
pip install -r requirements.txt

# Run notebook or script
```

---

## 📌 Key Takeaways

* Built a **production-style ML pipeline**
* Handled **large-scale real-world data**
* Addressed **class imbalance effectively**
* Applied **model comparison and tuning**
* Delivered **interpretable and deployable solution**

---

## 🔮 Future Improvements

* Add SHAP for model explainability
* Deploy as a Streamlit web app
* Optimize threshold for business risk control
* Integrate real-time prediction API

---

## 👤 Author

**Bao Quoc Tran**

* Applied Statistics Undergraduate
* Interested in Machine Learning & Financial Data Analysis

---

## ⭐ If you found this useful

Give this repo a star ⭐ and feel free to connect!
