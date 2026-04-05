# 📊 Data Splitting in Machine Learning



## 🔍 Why Data Splitting is Important

* Helps evaluate model performance
* Prevents overfitting and underfitting
* Ensures model generalization to unseen data
* Provides reliable accuracy metrics

---

## ⚙️ Common Data Splitting Techniques

### 1️⃣ Train-Test Split

* Dataset divided into:

  * **Training Set** (70–80%)
  * **Testing Set** (20–30%)
* Training → used to train model
* Testing → used to evaluate performance

---

### 2️⃣ Train-Validation-Test Split

* Dataset divided into:

  * **Training Set**
  * **Validation Set**
  * **Testing Set**

👉 Usage:

* Training → model learning
* Validation → hyperparameter tuning
* Testing → final evaluation

---

### 3️⃣ K-Fold Cross Validation

* Dataset split into **K equal parts (folds)**
* Model trained **K times**
* Each fold used once for testing

👉 Benefits:

* More reliable results
* Reduces variance

---

### 4️⃣ Stratified Sampling

* Maintains class distribution in all splits
* Useful for **imbalanced datasets**

---

### 5️⃣ Time-Based Split

* Used for **time-series data**
* Data split based on chronological order

---

## 📊 Data Split Ratios

### 🧾 Traditional Approach

* Train → 80%
* Dev → 20%
* Test → 20%

---

### 🚀 Big Data Approach

* Train → 98%
* Dev → 1%
* Test → 1%

👉 Even 1% can be large in big datasets

---

## 🛠️ Example using TuriCreate

```python
import turicreate as tc

# Load data
data = tc.SFrame("data.csv")

# Split into train (80%) and test (20%)
train_data_set, test_data = data.random_split(.8, seed=0)

# Split test into dev and test (50%-50%)
test_data_set, dev_set = test_data.random_split(.5, seed=0)

# Train model
model = tc.linear_regression.create(
    train_data_set,
    target="XYz",
    validation_set=dev_set
)

# Prediction
model.predict(test_data_set[1])
```

---

## 📌 Big Data Split Example

```python
import turicreate as tc

data = tc.SFrame("data.csv")

# 98% train, 2% test
train_data_set, test_data = data.random_split(.98, seed=0)

# Split remaining into dev & test
test_data_set, dev_set = test_data.random_split(.5, seed=0)

model = tc.linear_regression.create(
    train_data_set,
    target="XYz",
    validation_set=dev_set
)

model.predict(test_data_set[1])
```

---

## ⚠️ Handling Mismatched Data Distribution

### Problem:

Train and test data may come from different sources.

### Example:

* Train → Web images
* Dev/Test → Camera images

### ✅ Best Practice:

* Focus dev/test set on **real-world data you care about**

---

## 🔄 When to Change Dev/Test Set

Change dev/test set when:

* Metrics don’t match real-world expectations
* Model performs well but fails in practical use

👉 Example:

* Model A → Low error but allows unwanted data
* Model B → Higher error but better real-world behavior

---

## 🧠 Key Takeaways

* Always split data before training
* Dev & Test should come from **same distribution**
* Train set can be slightly different
* Choose split based on dataset size
* Focus on real-world relevance



