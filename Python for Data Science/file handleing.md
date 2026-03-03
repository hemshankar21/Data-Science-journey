# 📂 Python File Handling

This project demonstrates basic File Handling operations in Python including reading, writing, and appending data to files.

---

## 📌 Basic File Functions

- open()
- read()
- readline()
- write()
- close()

---

## 📖 Opening a File

### Syntax:
```python
file_object = open(file_name, access_mode)
```

### Example:
```python
file = open("test.txt", "r")
file.close()
```

---

# 📖 Reading a File

## 1️⃣ Reading Line by Line

```python
file = open('test.txt', 'r')

for line in file:
    print(line)

file.close()
```

### Sample Output:
```
Hello World
My name is Satyajit Pattnaik
Welcome to my Python course!!!!
```

---

## 2️⃣ Reading Entire File

```python
file = open('test.txt', 'r')
print(file.read())
file.close()
```

---

# ✍️ Writing to a File (Overwrite Mode)

⚠️ 'w' mode deletes existing content and writes new content.

```python
file = open('test.txt', 'w')
file.write("This is a write operation")
file.write("\n")
file.write("Hello!! Thanks for joining this program")
file.close()
```

### Output inside file:
```
This is a write operation
Hello!! Thanks for joining this program
```

---

# ➕ Append Operation

'a' mode adds content at the end without deleting existing data.

```python
with open('test.txt', 'a') as file:
    file.write("\n")
    file.write("This is a write operation")
```

---

# 🔄 Append and Read Mode (a+)

```python
with open('test.txt', 'a+') as file:
    file.write("\n")
    file.write("This is a write operation")
```

---

# ✅ Using with Statement (Best Practice)

Automatically closes the file after execution.

```python
with open('test.txt', 'r') as file:
    content = file.read()
    print(content)
```

---

# 📚 File Modes Summary

| Mode | Description |
|------|------------|
| r    | Read only |
| w    | Write (overwrite) |
| a    | Append |
| r+   | Read and Write |
| a+   | Append and Read |

---

# 🚀 What This Project Covers

- Opening and closing files
- Reading data from files
- Writing data to files
- Appending data
- Understanding file modes
- Using the with statement safely

---
