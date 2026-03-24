# 📊 Seaborn Tutorial (Jupyter Notebook)

## 📌 Overview
This project demonstrates how to use **Seaborn**, a powerful Python data visualization library built on top of Matplotlib.  
It simplifies creating attractive and informative statistical graphics.

> “If Matplotlib tries to make easy things easy and hard things possible, Seaborn makes hard things easy.”

---

## 🚀 Installation

Install Seaborn using pip:

```bash
pip install seaborn
```

---

## 📥 Import Libraries

```python
import seaborn as sns
import pandas as pd
import matplotlib.pyplot as plt
```

---

## 📊 Load Dataset

Seaborn provides built-in datasets. Example using the **Iris dataset**:

```python
df = sns.load_dataset('iris')
print(df.head())
```

### Sample Output

| sepal_length | sepal_width | petal_length | petal_width | species |
|-------------|------------|--------------|-------------|---------|
| 5.1         | 3.5        | 1.4          | 0.2         | setosa  |
| 4.9         | 3.0        | 1.4          | 0.2         | setosa  |

---

## 🔢 Data Analysis

### Count Values

```python
df.species.value_counts()
```

Output:

```
setosa        50
versicolor    50
virginica     50
```

---

## 📈 Visualization Examples

### 1️⃣ KDE Plot (Distribution Plot)

```python
sns.kdeplot(df['sepal_length'], shade=True)
plt.show()
```

👉 KDE (Kernel Density Estimation) shows the distribution of data smoothly.

---

### 2️⃣ Pair Plot

```python
sns.pairplot(df)
plt.show()
```

👉 Displays pairwise relationships between all numerical features.

---

## 📚 Additional Concepts

### 🔹 Pairplot
- Shows relationships between variables
- Useful for exploratory data analysis (EDA)

### 🔹 KDE Plot
- Smooth version of histogram
- Helps understand data distribution

---

## 🧠 Alternative Dataset (Sklearn)

```python
from sklearn.datasets import load_iris

iris = load_iris()
print(iris)
```

---

## 🎨 Seaborn Gallery

Seaborn supports multiple plots like:
- Scatter Plot
- Line Plot
- Bar Plot
- Box Plot
- Violin Plot
- Heatmap
- Histogram

---

## 🛠 Requirements

- Python 3.x
- seaborn
- matplotlib
- pandas
- scikit-learn

---

## 📌 Conclusion

Seaborn makes data visualization:
- ✅ Easy  
- ✅ Beautiful  
- ✅ Powerful  

It is widely used for **Data Science, Machine Learning, and EDA**.

---

## ⭐ If you like this project

Give it a ⭐ on GitHub!
