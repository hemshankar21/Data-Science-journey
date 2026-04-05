# 📊 Regression Metrics in Machine Learning

---

## 📌 Introduction

**Regression metrics** are used to evaluate how well a model predicts continuous numerical values.
They measure the **difference between actual and predicted values**.

---

## 🎯 Why Metrics Matter

* 📏 Quantify prediction errors
* ⚖️ Compare different models
* 🎯 Help in model optimization
* 📊 Highlight different types of errors

---

## 📊 Types of Regression Metrics

---

## 1️⃣ Mean Absolute Error (MAE)

📌 Measures average absolute error

**Formula:**

```id="mae1"
MAE = (1/n) * Σ |yi - ŷi|
```

### ✅ Key Points

* Easy to understand
* Same unit as target
* Treats all errors equally

---

### 💻 Implementation

```python id="mae2"
from sklearn.metrics import mean_absolute_error

mae = mean_absolute_error(y_test, y_pred)
print("MAE:", mae)
```

---

## 2️⃣ Mean Squared Error (MSE)

📌 Measures average squared error

**Formula:**

```id="mse1"
MSE = (1/n) * Σ (yi - ŷi)^2
```

### ✅ Key Points

* Penalizes large errors more
* Sensitive to outliers

---

### 💻 Implementation

```python id="mse2"
from sklearn.metrics import mean_squared_error

mse = mean_squared_error(y_test, y_pred)
print("MSE:", mse)
```

---

## 3️⃣ Root Mean Squared Error (RMSE)

📌 Square root of MSE

**Formula:**

```id="rmse1"
RMSE = √[(1/n) * Σ (yi - ŷi)^2]
```

### ✅ Key Points

* Same unit as target
* Penalizes large errors

---

### 💻 Implementation

```python id="rmse2"
import numpy as np
from sklearn.metrics import mean_squared_error

rmse = np.sqrt(mean_squared_error(y_test, y_pred))
print("RMSE:", rmse)
```

---

## 4️⃣ R² Score (Coefficient of Determination)

📌 Measures how well model explains variance

**Formula:**

```id="r21"
R² = 1 - (SS_res / SS_tot)
```

### ✅ Key Points

* Range: 0 to 1
* Higher = better model

---

### 💻 Implementation

```python id="r22"
from sklearn.metrics import r2_score

r2 = r2_score(y_test, y_pred)
print("R² Score:", r2)
```

---

## 5️⃣ Mean Absolute Percentage Error (MAPE)

📌 Error in percentage form

**Formula:**

```id="mape1"
MAPE = (100/n) * Σ |(yi - ŷi) / yi|
```

### ✅ Key Points

* Easy to interpret
* Scale independent

### ⚠️ Limitation

* Not suitable when actual values ≈ 0

---

### 💻 Implementation

```python id="mape2"
import numpy as np

mape = np.mean(np.abs((y_test - y_pred) / y_test)) * 100
print("MAPE:", mape)
```

---

## 📊 Metric Comparison

| Metric | Sensitive to Outliers | Unit    | Use Case                  |
| ------ | --------------------- | ------- | ------------------------- |
| MAE    | ❌ Low                 | Same    | General use               |
| MSE    | ✅ High                | Squared | Penalize large errors     |
| RMSE   | ✅ High                | Same    | Real-world interpretation |
| R²     | ❌ No                  | Ratio   | Model fit                 |
| MAPE   | ⚠️ Medium             | %       | Business metrics          |

---

## 📈 Interpretation Example

* **MAE = 42.79** → Avg error = 42.79 units
* **MSE = 2900.19** → Large errors exist
* **RMSE = 53.85** → Typical prediction error
* **R² = 0.45** → Model explains 45% variance
* **MAPE = 37.5%** → Predictions off by ~37%

---

## 🧠 Key Takeaways

* No single best metric → depends on problem
* Use **MAE** for simplicity
* Use **RMSE** when large errors matter
* Use **R²** for model fit
* Use **MAPE** for percentage understanding

---





