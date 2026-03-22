# 🏠 Bengaluru House Price Prediction

## 📌 Overview

This is a machine learning project where I tried to predict house prices in Bengaluru using features like location, total square footage, number of bathrooms, and BHK.
The goal was to understand the full ML workflow from data cleaning to model building.

---

## 🔍 What I did

### 1. Data Cleaning & EDA

* Handled missing values in columns like `bath` and `total_sqft`
* Converted different units (Sq. Meter, Acres, etc.) into square feet
* Removed unrealistic values (like very high price per sqft, too many bathrooms, etc.)
* Extracted **BHK** from the `size` column
* Cleaned location names (removed spaces, duplicates, inconsistencies)

---

### 2. Feature Engineering

* Grouped locations using a **Top-120 approach** to reduce too many categories
* Created a new feature: **price_per_sqft**
* Applied **One Hot Encoding** on location
* Prepared final dataset for model training

---

### 3. Model Building

I tried multiple models and compared their performance:

* Linear Regression (baseline)
* Ridge & Lasso Regression
* Decision Tree
* Random Forest
* XGBoost

Evaluation metrics used:

* R² Score
* MAE (Mean Absolute Error)
* RMSE

---

### 🏆 Final Result

* **Random Forest Regressor** performed the best
* Further improved using **GridSearchCV**
* Achieved stable performance (~0.75–0.77 R²)

---

## 💡 Key Learnings

* Data cleaning is the most important part of any ML project
* Location plays a major role in house pricing
* Scaling didn’t affect linear models much in this case
* Tree-based models handled non-linearity better
* Cross-validation gives a more realistic performance than a single test split

---

## 🛠️ Tools & Libraries

* Python
* Pandas, NumPy
* Scikit-learn
* XGBoost

---

## 📁 Project Structure

```
BENGALURU-HOUSE-PREDICTION/
│
├── data/
│   ├── Bengaluru_House_Data.csv
│   ├── cleaned_data.csv
│
├── notebooks/
│   ├── 01_eda.ipynb
│   ├── 02_feature_engineering.ipynb
│   ├── 03_model_building.ipynb
│
├── house_price_model.pkl
└── README.md
```

---

## 🚀 Future Improvements

* Build a simple web app (Streamlit)
* Try better feature engineering for location
* Deploy the model online

---

## 🙌 Final Note

This project helped me understand how raw data is converted into a working ML model.
It also gave me hands-on experience with preprocessing, feature engineering, and model comparison.
