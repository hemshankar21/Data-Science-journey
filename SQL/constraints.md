# 📊 Matplotlib Data Visualization

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Matplotlib](https://img.shields.io/badge/Library-Matplotlib-orange)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)


## 📥 Import Libraries

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
```

---

## 📊 Dataset Example

```python
Data = {
    'Year': [1920, 1930, 1940, 1950, 1960, 1970, 1980, 1990, 2000, 2010, 2020],
    'Exchange Rate': [65, 69, 71, 64, 62, 59, 72, 71, 75, 78, 81]
}

df = pd.DataFrame(Data)
```

---

## 📈 Line Plot

```python
plt.plot(df['Year'], df['Exchange Rate'])
plt.title("Year vs Exchange Rate")
plt.xlabel("Year")
plt.ylabel("Exchange Rate")
plt.show()
```

---

## 📊 Bar Chart

```python
df.plot(x='Year', y='Exchange Rate', kind='bar')
plt.show()
```

---

## 📉 Histogram

```python
plt.hist(df['Exchange Rate'])
plt.title("Histogram of Exchange Rates")
plt.show()
```

---

## 🔵 Scatter Plot

```python
plt.scatter(df['Year'], df['Exchange Rate'])
plt.title("Scatter Plot")
plt.show()
```

---

## 🥧 Pie Chart

```python
Data = {'Tasks': [100, 500, 300]}
df = pd.DataFrame(Data, index=['Pending', 'Completed', 'Ongoing'])

df.plot.pie(y='Tasks', figsize=(5,5))
plt.show()
```

---

## 📊 Real Dataset Example

```python
churn_df = pd.read_csv("your_file.csv")

# Count plot
churn_df['Exited'].value_counts().plot(kind='bar')
plt.show()

# Geography distribution
churn_df['Geography'].value_counts().plot(kind='barh')
plt.show()
```

---

## 📌 Types of Charts in Matplotlib

| Chart Type   | Description |
|-------------|------------|
| Line Plot   | Shows trends over time |
| Bar Chart   | Compares categories |
| Histogram   | Shows data distribution |
| Scatter Plot| Shows relationships between variables |
| Pie Chart   | Shows proportions |

---

## 💡 Key Functions

- `plt.plot()` → Line graph  
- `plt.bar()` → Bar chart  
- `plt.hist()` → Histogram  
- `plt.scatter()` → Scatter plot  
- `plt.pie()` → Pie chart  
- `plt.show()` → Display graph  

---

## 🧠 Conclusion

Matplotlib is a powerful visualization library used in:
- Data Analysis  
- Machine Learning  
- Data Science Projects  

It helps to understand patterns, trends, and insights from data easily.

---
