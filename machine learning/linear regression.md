# 📈 Linear Regression in Machine Learning

---

## 📌 Introduction

**Linear Regression** is a fundamental supervised learning algorithm used to predict **continuous values** by modeling the relationship between input features and output.

👉 It uses a **best-fit straight line** to make predictions.

---

## 🎯 Key Concepts

* 📊 Assumes a **linear relationship**
* 📈 Uses a **best-fit line**
* 🔍 Predicts continuous outputs

---

## 🔗 Basic Equation

```id="eq1"
y = mx + b
```

Where:

* **y** → predicted value
* **x** → input feature
* **m** → slope
* **b** → intercept

---

## 📉 Best-Fit Line

* Minimizes error between actual & predicted values
* Uses **Least Squares Method**

```id="eq2"
Σ (yi - ŷi)²
```

👉 Goal: Minimize this error

---

## ⚙️ Hypothesis Function

### Simple Linear Regression

```id="eq3"
h(x) = β₀ + β₁x
```

---

### Multiple Linear Regression

```id="eq4"
h(x₁, x₂, ..., xₙ) = β₀ + β₁x₁ + β₂x₂ + ... + βₙxₙ
```

---

## 📊 Types of Linear Regression

### 1️⃣ Simple Linear Regression

* One input variable
* Example: Salary vs Experience

---

### 2️⃣ Multiple Linear Regression

* Multiple input variables
* Example: House price prediction

---

## ⚠️ Assumptions

* ✔️ Linearity
* ✔️ Independence of errors
* ✔️ Constant variance (Homoscedasticity)
* ✔️ Normal distribution of errors
* ✔️ No multicollinearity
* ✔️ No autocorrelation

---

## 📉 Cost Function (MSE)

```id="eq5"
J = (1/n) Σ (ŷi - yi)²
```

👉 Measures prediction error

---

## 🔄 Gradient Descent

📌 Optimization technique to minimize cost

### Steps:

1. Initialize parameters
2. Calculate error
3. Update parameters
4. Repeat until convergence

---

## 📊 Evaluation Metrics

* MAE
* MSE
* RMSE
* R² Score
* Adjusted R²

---

## 🔧 Regularization Techniques

* **Ridge (L2)** → Shrinks coefficients
* **Lasso (L1)** → Feature selection
* **Elastic Net** → Combination

---

## 💻 Python Implementation

```python id="lr1"
import numpy as np
import matplotlib.pyplot as plt
from sklearn.linear_model import LinearRegression

# Generate data
np.random.seed(42)
X = np.random.rand(50, 1) * 100
Y = 3.5 * X + np.random.randn(50, 1) * 20

# Train model
model = LinearRegression()
model.fit(X, Y)

# Predictions
Y_pred = model.predict(X)

# Plot
plt.scatter(X, Y, color='blue')
plt.plot(X, Y_pred, color='red')
plt.show()

# Parameters
print("Slope:", model.coef_[0][0])
print("Intercept:", model.intercept_[0])
```

---

## 🌍 Applications

* 🏠 House price prediction
* 📈 Stock market analysis
* 🌾 Crop yield prediction
* 🛒 Sales forecasting

---

## 👍 Advantages

* Simple and easy to understand
* Fast and efficient
* Good baseline model
* Interpretable results

---

## ⚠️ Limitations

* Assumes linear relationship
* Sensitive to outliers
* Cannot model complex patterns

---

## 🧠 Key Takeaways

* Linear regression is the **foundation of ML**
* Works best for **linear data**
* Use regularization to avoid overfitting

---

