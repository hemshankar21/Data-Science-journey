# 📊 Multiple Linear Regression in Machine Learning

---

## 📌 Introduction

**Multiple Linear Regression** is an extension of linear regression that models the relationship between **one dependent variable** and **multiple independent variables**.

👉 It helps understand how multiple factors influence an outcome.

---

## 🔢 Mathematical Equation

```id="eq1"
y = β₀ + β₁X₁ + β₂X₂ + ... + βₙXₙ
```

Where:

* **y** → dependent variable
* **X₁, X₂, ... Xₙ** → independent variables
* **β₀** → intercept
* **β₁, β₂ ... βₙ** → coefficients

---

## ⚙️ Steps to Perform Multiple Linear Regression

1️⃣ Import libraries
2️⃣ Load dataset
3️⃣ Select features
4️⃣ Split data (Train/Test)
5️⃣ Train model
6️⃣ Evaluate model
7️⃣ Make predictions

---

## 🔄 Handling Categorical Data

📌 Use **Dummy Variables (One-Hot Encoding)**

Example:

* Male → 1
* Female → 0

👉 Avoid **dummy variable trap** by dropping one category

---

## ⚠️ Multicollinearity

📌 When independent variables are highly correlated

### 🔍 Detection Methods:

* Correlation Matrix
* Variance Inflation Factor (VIF)

---

## 📋 Assumptions

* ✔️ Linearity
* ✔️ Homoscedasticity
* ✔️ Normal distribution of errors
* ✔️ No multicollinearity

---

## 💻 Python Implementation

```python id="mlr1"
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
from sklearn.datasets import fetch_california_housing

# Load dataset
data = fetch_california_housing()
X = pd.DataFrame(data.data, columns=data.feature_names)
y = pd.Series(data.target)

# Select features
X = X[['MedInc', 'AveRooms']]

# Split data
X_train, X_test, y_train, y_test = train_test_split(
    X, y, test_size=0.2, random_state=42
)

# Train model
model = LinearRegression()
model.fit(X_train, y_train)

# Coefficients
print("Intercept:", model.intercept_)
print("Coefficients:", model.coef_)

# Predictions
y_pred = model.predict(X_test)
```

---

## 📊 Visualization (3D Best-Fit Plane)

* 🔵 Blue → Actual data
* 🔴 Red → Predicted surface

👉 Helps understand relationship between variables

---

## 🌍 Applications

* 🏠 House price prediction
* 📈 Sales forecasting
* 💰 Financial analysis
* 🌾 Agriculture predictions

---

## 👍 Advantages

* Captures influence of multiple variables
* Easy to interpret coefficients
* Useful for real-world problems

---

## ⚠️ Limitations

* Sensitive to multicollinearity
* Assumes linear relationship
* Needs proper preprocessing

---

## 🧠 Key Takeaways

* Extension of simple linear regression
* Handles multiple features
* Requires careful feature selection

---

## 📚 Reference

Content adapted from provided material. 

---

✨ *Happy Learning Machine Learning!* 🚀
