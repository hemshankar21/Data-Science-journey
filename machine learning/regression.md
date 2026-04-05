# 📈 Regression in Machine Learning

---

## 📌 Introduction

**Regression** is a supervised learning technique used to predict **continuous numerical values** by learning relationships between input features and a target variable.

👉 It is widely used in:

* Price prediction
* Trend forecasting
* Risk analysis
* Decision-making

---

## ⚙️ Key Characteristics

* Works with **real-valued outputs**
* Identifies relationships between variables
* Supports simple & complex models

---

## 🔍 Types of Regression

---

### 1️⃣ Simple Linear Regression

📌 Models relationship between **one input** and output using a straight line

### ✅ Example

* House price prediction based on size

### 👍 Advantages

* Easy to understand
* Highly interpretable

### ⚠️ Disadvantages

* Cannot handle complex patterns

---

### 2️⃣ Multiple Linear Regression

📌 Uses **multiple input variables**

### ✅ Example

* Price prediction using size, location, rooms

### 👍 Advantages

* Captures combined effect of features

### ⚠️ Disadvantages

* Sensitive to multicollinearity

---

### 3️⃣ Polynomial Regression

📌 Models **non-linear relationships**

### ✅ Example

* Growth trends, temperature variation

### 👍 Advantages

* Captures curves effectively

### ⚠️ Disadvantages

* Can overfit

---

### 4️⃣ Ridge & Lasso Regression

📌 Regularization techniques

* **Ridge (L2)** → Shrinks coefficients
* **Lasso (L1)** → Can remove features

### 👍 Advantages

* Reduces overfitting

### ⚠️ Disadvantages

* Harder to interpret

---

### 5️⃣ Support Vector Regression (SVR)

📌 Uses margin (epsilon tube) to fit data

### 👍 Advantages

* Works well for complex data

### ⚠️ Disadvantages

* Computationally expensive

---

### 6️⃣ Decision Tree Regression

📌 Splits data into tree structure

### 👍 Advantages

* Easy to visualize

### ⚠️ Disadvantages

* Prone to overfitting

---

### 7️⃣ Random Forest Regression

📌 Ensemble of multiple decision trees

### 👍 Advantages

* High accuracy
* Handles noise well

### ⚠️ Disadvantages

* Hard to interpret (black-box)

---

## 📊 Evaluation Metrics

| Metric     | Description             |
| ---------- | ----------------------- |
| MAE        | Mean absolute error     |
| MSE        | Mean squared error      |
| RMSE       | Root mean squared error |
| Huber Loss | Combines MAE & MSE      |
| R² Score   | Measures model fit      |

---

## 💻 Implementation (Linear Regression)

```python id="reg1"
import pandas as pd
from sklearn import linear_model
import numpy as np
import matplotlib.pyplot as plt
import matplotlib

matplotlib.use('Agg')

df = pd.read_csv("Housing.csv")

Y = df['price']
X = df['lotsize']

X = X.to_numpy().reshape(len(X), 1)
Y = Y.to_numpy().reshape(len(Y), 1)

# Split data
X_train = X[:-250]
X_test = X[-250:]
Y_train = Y[:-250]
Y_test = Y[-250:]

# Plot test data
plt.scatter(X_test, Y_test, color='black')

# Train model
model = linear_model.LinearRegression()
model.fit(X_train, Y_train)

# Plot predictions
plt.plot(X_test, model.predict(X_test), color='red', linewidth=3)

plt.savefig("regression_plot.png")
print("Plot saved as regression_plot.png")
```

---

## 🌍 Applications

* 🏠 House price prediction
* 📊 Sales forecasting
* ❤️ Medical risk analysis
* 📈 Stock market prediction

---

## 🧠 Key Takeaways

* Regression predicts **continuous values**
* Choose model based on data complexity
* Use regularization to avoid overfitting
* Evaluate using proper metrics

---
