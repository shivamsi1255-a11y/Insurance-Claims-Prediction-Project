*🏥 Insurance Claims Prediction using Machine Learning








📌 Overview

This project builds a Machine Learning regression system to predict insurance claim amounts based on demographic and health-related factors.

Accurately predicting insurance claims helps insurers:

Assess financial risk

Set fair and data-driven premiums

Develop targeted wellness programs

Improve underwriting strategies

🎯 Project Goals

Perform comprehensive Exploratory Data Analysis (EDA)

Clean and preprocess real-world data

Train and compare multiple regression models

Identify key drivers of insurance claims

Generate actionable business insights

🗂️ Dataset Description

The dataset includes insurance policyholder information:

Feature	Description
Id	Unique identifier
age	Age of policyholder
gender	Male / Female
bmi	Body Mass Index
bloodpressure	Blood pressure reading
diabetic	Yes / No
children	Number of dependents
smoker	Yes / No
region	Residential region in US
claim	Medical insurance claim amount (Target Variable)
🔬 Methodology
1️⃣ Data Loading & Inspection

Loaded dataset using pandas

Used:

df.head()

df.info()

df.describe()

df.shape

2️⃣ Data Cleaning

Checked duplicates → df.duplicated().sum()

Checked missing values → df.isna().sum()

Missing values found in:

age

region

Since missing values were minimal → removed using:

df.dropna(inplace=True)

3️⃣ Exploratory Data Analysis (EDA)
📊 Numerical Analysis

Histograms for:

Age

BMI

Blood Pressure

Children

Claim Amount

📈 Categorical Analysis

Count plots for:

Gender

Smoker

Diabetic

Region

📦 Boxplots

BMI Outlier Detection

Claim Distribution by:

Gender

Smoker Status

Diabetic Status

🔎 Key Observation

Smokers showed significantly higher claim amounts compared to non-smokers.

⚙️ Feature Engineering & Preprocessing
🔹 Feature Selection

Selected Features:

['age', 'gender', 'bmi', 'bloodpressure', 'diabetic', 'children', 'smoker']


Target Variable:

claim

🔹 Encoding

Categorical features encoded using LabelEncoder:

gender

diabetic

smoker

Encoders saved as .pkl files for deployment consistency.

🔹 Train-Test Split

80% Training

20% Testing

Used train_test_split()

🤖 Models Implemented

Four regression models were trained:

Linear Regression

Decision Tree Regressor

Random Forest Regressor

Gradient Boosting Regressor

📊 Model Performance Comparison
Model	MAE	MSE	R² Score
Linear Regression	~5,034	~38M	0.72
Decision Tree	~5,170	~42M	0.64
Random Forest	~4,089	~28.36M	0.80
⭐ Gradient Boosting	~3,847	~24.27M	0.83
🏆 Best Model: Gradient Boosting Regressor

Highest R² Score: 0.83

Lowest MAE

Lowest MSE

Best generalization performance

Ensemble methods clearly outperformed individual models.

📌 Feature Importance Analysis

Using Random Forest & Gradient Boosting:

Feature	Importance
🚬 Smoker	~62%
🧮 BMI	~21%
❤️ Blood Pressure	~9%
👶 Children	~3%
🎂 Age	~2%
🩺 Diabetic	~2%
👤 Gender	~1%
🔥 Key Insight

Smoking status is the dominant predictor of insurance claims.

This single factor accounts for over half of the predictive power.

💡 Business Insights for Insurance Industry
🎯 Risk-Based Pricing

Premiums can be adjusted more accurately based on:

Smoking status

BMI

Blood pressure

🏃 Preventive Health Programs

Wellness initiatives targeting:

Weight management

Blood pressure control

Smoking cessation

🧠 Model Recommendation

Deploy Gradient Boosting Regressor for production use.

🚀 Installation & Usage
1️⃣ Install Dependencies
pip install pandas numpy matplotlib seaborn scikit-learn

2️⃣ Run Notebook

Download insurance.csv

Place in project folder

Open Jupyter/Colab

Run cells sequentially

🔮 Future Enhancements

Hyperparameter tuning (GridSearchCV)

Add XGBoost / LightGBM

Advanced feature engineering (interaction terms)

Deploy using Streamlit or Flask

Build REST API for real-time predictions

🧾 Final Project Summary

This project successfully:

✔ Cleaned and analyzed real-world insurance data
✔ Built and compared multiple regression models
✔ Identified key health and lifestyle risk factors
✔ Achieved 83% variance explanation using Gradient Boosting
✔ Generated actionable business intelligence insights

The project demonstrates the power of ensemble machine learning models in solving real-world financial prediction problems.

📚 Tech Stack

Python

Pandas

NumPy

Matplotlib

Seaborn

Scikit-Learn

Jupyter Notebook

👨‍💻 Developed By

Shivam Singh
Data Science & Machine Learning Enthusiast
