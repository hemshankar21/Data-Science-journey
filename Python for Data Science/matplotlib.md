# 📊 Matplotlib Data Visualization

![Python](https://img.shields.io/badge/Python-3.x-blue?logo=python)
![Matplotlib](https://img.shields.io/badge/Library-Matplotlib-orange)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)

---

## 🚀 Project Overview

This project demonstrates how to use **Matplotlib** for data visualization in Python.
It covers different types of plots used in **Data Science and EDA (Exploratory Data Analysis)**.

---

## 📌 Features

* 📈 Line Plot
* 📊 Bar Chart
* 📉 Histogram
* 🔵 Scatter Plot
* 🥧 Pie Chart
* 📂 Real Dataset Visualization

---

## 🛠️ Tech Stack

* Python
* Pandas
* NumPy
* Matplotlib

---

## 📦 Installation

```bash
pip install matplotlib pandas numpy
```

---

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

df.plot
```
