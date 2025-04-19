# 📊 Loan Default Prediction using Machine Learning

## 🧠 Overview
This project aims to predict the likelihood of a borrower defaulting on a loan using historical loan data. Through extensive data preprocessing, exploratory data analysis, feature engineering, and model building, the goal is to identify patterns that distinguish defaulters from fully paid loans.

---

## 📁 Dataset
The dataset includes borrower and loan-level information such as:
- **Loan Amount**, **Term**, **Interest Rate**, **Employment Length**
- **Income**, **Home Ownership**, **Grade/Subgrade**
- **Loan Status** (Target: Fully Paid or Charged Off)

> The dataset is imbalanced, with a higher proportion of fully paid loans compared to defaults.

---

## 🧹 Data Preprocessing
- **Missing Values:** Handled appropriately across all key features.
- **Categorical Encoding:** Used Label Encoding and One-Hot Encoding.
- **Feature Scaling:** Applied Standard Scaler on numerical features.
- **Feature Selection:** Removed unnecessary zip codes and transformed data types as needed.

---

## 📊 Exploratory Data Analysis
Used **hvPlot** to create interactive visualizations:
- Loan Amount and Installment distribution by loan status
- Loan status breakdown by Grade, Sub-grade, and Home Ownership
- Income and Employment Length analysis
- Distribution of annual income with highlight on high-income borrowers

---

## ⚖️ Handling Class Imbalance
To address the imbalance between fully paid and defaulted loans:
- **SMOTE (Synthetic Minority Over-sampling Technique)** was applied to balance the classes.
- Class distribution post-SMOTE:
  - **Charged Off:** 50%
  - **Fully Paid:** 50%

---

## 🤖 Model Building
Trained multiple machine learning models to evaluate performance:

### ✅ Best Performing Model
- **Random Forest Classifier**
  - Balanced accuracy: **~87.4%**
  - Precision (Fully Paid): **~87.8%**
  - Precision (Charged Off): **~66.7%**

📉 **Confusion Matrix (Test Set):**
```
[[18687  6793]
 [16591 88352]]
```

---

## ⚙️ Installation & Usage
### Requirements
Make sure the following packages are installed:
```bash
pip install pandas numpy scikit-learn imbalanced-learn hvplot matplotlib seaborn
```

### Run Instructions
1. Clone the repository:
```bash
git clone https://github.com/NoumanYousaf14/Loan-Defualt-prediction.git
cd Loan-Defualt-prediction
```
2. Open and run the Jupyter notebook:
```bash
jupyter notebook loan_default.ipynb
```

---

## 🚀 Future Enhancements
- Integrate deep learning models (e.g., Neural Networks, Autoencoders)
- Deploy the model as a REST API for real-time prediction
- Build an interactive dashboard using Streamlit or Dash
- Improve feature engineering with domain-specific insights
- Incorporate additional financial behavior indicators

---

