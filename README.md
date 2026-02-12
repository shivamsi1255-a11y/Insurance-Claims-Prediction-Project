# 🏥 Insurance Claims Prediction using Machine Learning  

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Regression-green.svg)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Modeling-orange.svg)
![Status](https://img.shields.io/badge/Project-Completed-brightgreen.svg)

---

## 📌 Overview  

This project builds a Machine Learning regression system to predict insurance claim amounts based on demographic and health-related factors.

Accurately predicting insurance claims helps insurers:
- Assess financial risk  
- Set fair and data-driven premiums  
- Develop targeted wellness programs  
- Improve underwriting strategies  

---

# 🎯 Project Goals  

- Perform comprehensive Exploratory Data Analysis (EDA)
- Clean and preprocess real-world data
- Train and compare multiple regression models
- Identify key drivers of insurance claims
- Generate actionable business insights

---

# 🗂️ Dataset Description  

The dataset includes insurance policyholder information:

| Feature | Description |
|----------|------------|
| Id | Unique identifier |
| age | Age of policyholder |
| gender | Male / Female |
| bmi | Body Mass Index |
| bloodpressure | Blood pressure reading |
| diabetic | Yes / No |
| children | Number of dependents |
| smoker | Yes / No |
| region | Residential region in US |
| claim | Medical insurance claim amount (Target Variable) |

---

# 🔬 Methodology  

## 1️⃣ Data Loading & Inspection  

- Loaded dataset using pandas
- Used:
  - df.head()
  - df.info()
  - df.describe()
  - df.shape()

---

## 2️⃣ Data Cleaning  

- Checked duplicates → df.duplicated().sum()
- Checked missing values → df.isna().sum()
- Missing values found in:
  - age
  - region
- Removed using:

```python
df.dropna(inplace=True)

## 3️⃣ Exploratory Data Analysis (EDA)

### 📊 Numerical Analysis

Histograms were created for:

- Age  
- BMI  
- Blood Pressure  
- Children  
- Claim Amount  

### 📈 Categorical Analysis

Count plots were generated for:

- Gender  
- Smoker  
- Diabetic  
- Region  

### 📦 Outlier Detection

- Boxplot for BMI  
- Boxplot for Claim Amount by Gender and Smoker Status  

---

# ⚙️ Feature Engineering & Preprocessing

## 🔹 Feature Selection

Selected Features:


---

## 🔹 Encoding

Categorical features encoded using `LabelEncoder`:

- gender  
- diabetic  
- smoker  

Encoders saved as `.pkl` files for deployment consistency.

---

## 🔹 Train-Test Split

- 80% Training Data  
- 20% Testing Data  
- Implemented using `train_test_split()`  

---

# 🤖 Models Implemented

- Linear Regression  
- Decision Tree Regressor  
- Random Forest Regressor  
- Gradient Boosting Regressor  

---

# 📊 Model Performance Comparison

| Model | MAE | MSE | R² Score |
|--------|--------|-------------|----------|
| Linear Regression | ~5,034 | ~38M | 0.72 |
| Decision Tree | ~5,170 | ~42M | 0.64 |
| Random Forest | ~4,089 | ~28.36M | 0.80 |
| ⭐ Gradient Boosting | ~3,847 | ~24.27M | 0.83 |

---

# 🏆 Best Model: Gradient Boosting Regressor

- Highest R² Score: **0.83**
- Lowest MAE
- Lowest MSE
- Best generalization performance

---

# 📌 Feature Importance

| Feature | Importance |
|----------|------------|
| Smoker | ~62% |
| BMI | ~21% |
| Blood Pressure | ~9% |
| Others | <5% |

---

# 💡 Business Insights

- Smoking status is the strongest predictor of insurance claims.
- BMI and Blood Pressure significantly impact medical costs.
- Ensemble models outperform simple regression models.

---

# 🚀 Installation

Install required dependencies:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn



