# ⚙️ Feature Engineering in Machine Learning

## 📊 Scaling, Normalization & Standardization

---

## 📌 Introduction

**Feature Engineering** is the process of creating, transforming, or selecting important features from raw data to improve machine learning model performance.

👉 It helps models:

* Learn patterns better
* Improve prediction accuracy
* Reduce overfitting
* Enhance interpretability

---

## 🚀 Why Feature Engineering Matters

* 📈 Better pattern learning
* 🎯 Improved accuracy
* 🛡️ Reduces noise and overfitting
* 🔍 Makes models easier to understand

---

## 🔧 Feature Scaling Techniques

### 1️⃣ Absolute Maximum Scaling

📌 Scales data between **-1 and 1**

**Formula:**

```
X_scaled = Xi / max(|X|)
```

### ✅ Key Points

* Sensitive to outliers
* Best for clean datasets

---

### 💻 Implementation

```python id="absmax1"
import pandas as pd
import numpy as np

df = pd.read_csv('Housing.csv')
df = df.select_dtypes(include=np.number)

max_abs = np.max(np.abs(df), axis=0)
scaled_df = df / max_abs

print(scaled_df.head())
```

---

## 2️⃣ Min-Max Scaling

📌 Scales data between **0 and 1**

**Formula:**

```
X_scaled = (Xi - Xmin) / (Xmax - Xmin)
```

### ✅ Key Points

* Preserves distribution
* Sensitive to outliers

---

### 💻 Implementation

```python id="minmax1"
from sklearn.preprocessing import MinMaxScaler
import pandas as pd

scaler = MinMaxScaler()
scaled_data = scaler.fit_transform(df)

scaled_df = pd.DataFrame(scaled_data, columns=df.columns)
print(scaled_df.head())
```

---

## 3️⃣ Normalization (Vector Normalization)

📌 Scales each row to unit length (norm = 1)

**Formula:**

```
X_scaled = Xi / ||X||
```

### ✅ Key Points

* Focuses on direction, not magnitude
* Useful in text classification & clustering

---

### 💻 Implementation

```python id="norm1"
from sklearn.preprocessing import Normalizer
import pandas as pd

scaler = Normalizer()
scaled_data = scaler.fit_transform(df)

scaled_df = pd.DataFrame(scaled_data, columns=df.columns)
print(scaled_df.head())
```

---

## 4️⃣ Standardization (Z-Score Scaling)

📌 Transforms data to:

* Mean = 0
* Variance = 1

**Formula:**

```
X_scaled = (Xi - μ) / σ
```

### ✅ Key Points

* Works well with normally distributed data
* Used in most ML algorithms

---

### 💻 Implementation

```python id="std1"
from sklearn.preprocessing import StandardScaler
import pandas as pd

scaler = StandardScaler()
scaled_data = scaler.fit_transform(df)

scaled_df = pd.DataFrame(scaled_data, columns=df.columns)
print(scaled_df.head())
```

---

## 5️⃣ Robust Scaling

📌 Uses median and IQR (less sensitive to outliers)

**Formula:**

```
X_scaled = (Xi - median) / IQR
```

### ✅ Key Points

* Handles outliers well
* Suitable for skewed data

---

### 💻 Implementation

```python id="robust1"
from sklearn.preprocessing import RobustScaler
import pandas as pd

scaler = RobustScaler()
scaled_data = scaler.fit_transform(df)

scaled_df = pd.DataFrame(scaled_data, columns=df.columns)
print(scaled_df.head())
```

---

## 📊 Comparison of Scaling Techniques

| Method          | Description         | Outlier Sensitivity | Use Case           |
| --------------- | ------------------- | ------------------- | ------------------ |
| Absolute Max    | Divide by max value | High                | Simple scaling     |
| Min-Max         | Scale to 0–1        | High                | Neural networks    |
| Normalization   | Unit vector scaling | N/A                 | Text, similarity   |
| Standardization | Mean=0, Var=1       | Moderate            | Most ML models     |
| Robust Scaling  | Median & IQR        | Low                 | Outlier-heavy data |

---

## ✅ Advantages of Feature Scaling

* 🚀 Improves model performance
* ⚡ Speeds up training
* ⚖️ Prevents feature dominance
* 🔒 Increases numerical stability
* 🤖 Required for algorithms like:

  * SVM
  * KNN
  * Neural Networks

---

## 🧠 Key Takeaways

* Always scale features before training
* Choose method based on data type
* Use Robust Scaling for outliers
* Standardization is most commonly used

---

## 📚 Reference

Content adapted from provided material. 

---

✨ *Happy Learning Machine Learning!* 🚀
