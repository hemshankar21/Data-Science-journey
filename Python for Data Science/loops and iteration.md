# 🔁 Python Loops & Iteration

---

## 📖 Overview

This project covers:

- What is an Iterable
- What is an Iterator
- For Loops
- While Loops
- Loop with `else`
- Conditional Statements
- List Iteration
- Basic List Processing

---

## 📌 What is an Iterable?

An **iterable** is an object that can be looped over.

Examples:
- List
- Tuple
- Dictionary
- String
- Set

---

## 📌 What is an Iterator?

An **iterator** is a variable that moves through each element of an iterable one at a time.

Example:

```python
for i in range(1, 5):
    print(i)
```

Output:

```
1
2
3
4
```

---

## 📌 Even or Odd Number Check

```python
x = 101

if x % 2 == 0:
    print(x, "is an even number")
else:
    print(x, "is an odd number")
```

Output:

```
101 is an odd number
```

---

## 📌 For Loop with Else

Python allows an `else` block with loops.  
The `else` executes when the loop completes normally (without break).

```python
for i in range(1, 5):
    print(i)
else:
    print("For loop exhausted.")
```

Output:

```
1
2
3
4
For loop exhausted.
```

---

## 📌 List Iteration Example

```python
list_1 = ["Automobiles", "Honda", "Benz", "Maruti", "Kia"]
list_2 = []

for i in list_1:
    list_2.append(i)

print(list_2)
```

Output:

```
['Automobiles', 'Honda', 'Benz', 'Maruti', 'Kia']
```

---

## 📌 Using Loop to Store Length of Each Element

```python
list_1 = ["Automobiles", "Honda", "Benz", "Maruti", "Kia"]
list_2 = []

for i in list_1:
    list_2.append(len(i))

print(list_2)
```

Output:

```
[11, 5, 4, 6, 3]
```

---

## 🛠 Technologies Used

- Python 3
- Jupyter Notebook

---

## 🚀 How to Run

1. Install Python
2. Install Jupyter Notebook:

```
pip install notebook
```

3. Run Jupyter Notebook:

```
jupyter notebook
```

4. Open the `.ipynb` file and execute the cells.

---

## 🎯 Learning Outcomes

After completing this project, you will understand:

- How loops work in Python
- How iteration works internally
- Difference between iterable and iterator
- How to use `for` and `while` loops
- How to use `for-else`
- How to manipulate lists using loops


Beginner-level Python practice notebook focused on understanding loops and iteration concepts.
