# 🧠 OOPs in Python

This project demonstrates the core concepts of **Object-Oriented Programming (OOP)** in Python with practical examples.

---

# 📚 What This Project Covers

- Classes and Objects
- Constructors (`__init__`)
- Instance Variables
- Class Variables
- Adding Methods to Classes
- Inheritance
- Method Overriding
- Polymorphism
- Using `__str__()` method
- Real-world example with Shape, Circle, Rectangle

---

# 1️⃣ Creating Classes and Objects

## ✅ Defining a Class

```python
class Rectangle:
    def __init__(self):
        self.length = 10
        self.breadth = 5
```

### 🔹 Creating Object

```python
rect = Rectangle()
print(rect.length)
print(rect.breadth)
```

---

# 2️⃣ Constructor (`__init__`)

A constructor is a special method that runs automatically when an object is created.

```python
class Rectangle:
    def __init__(self, length, breadth):
        self.length = length
        self.breadth = breadth
```

### 🔹 Instantiating Class

```python
rect = Rectangle(40, 20)
print(rect.breadth)
```

### Output:
```
20
```

---

# 3️⃣ Class Variables and Instance Variables

```python
class Circle:
    pi = 3.14   # Class Variable

    def __init__(self, radius):
        self.radius = radius   # Instance Variable
```

### 🔹 Accessing Variables

```python
circle_1 = Circle(5)
circle_2 = Circle(2)

print("Radius =", circle_1.radius, "pi =", circle_1.pi)
print("Radius =", circle_2.radius, "pi =", circle_2.pi)
```

---

# 4️⃣ Adding a Method to Class

```python
class Rectangle:
    def __init__(self, length, breadth):
        self.length = length
        self.breadth = breadth

    def calculate_area(self):
        return self.length * self.breadth
```

### 🔹 Calling Method

```python
r = Rectangle(5, 10)
print("Area =", r.calculate_area())
```

### Output:
```
Area = 50
```

---

# 5️⃣ Inheritance

```python
class Employee:
    def function1(self):
        print("hello world")

class Department(Employee):
    pass
```

### 🔹 Using Inherited Method

```python
dept = Department()
dept.function1()
```

### Output:
```
hello world
```

---

# 6️⃣ Polymorphism with Shape Example

```python
class Shape:
    def set_color(self, color):
        self.color = color

    def calculate_area(self):
        pass

    def color_the_shape(self):
        color_price = {"red": 10, "blue": 15, "green": 5}
        return self.calculate_area() * color_price[self.color]
```

---

## 🔵 Circle Class (Child Class)

```python
class Circle(Shape):
    pi = 3.14

    def __init__(self, radius):
        self.radius = radius

    def calculate_area(self):
        return Circle.pi * self.radius
```

---

## 🔶 Rectangle Class (Method Overriding)

```python
class Rectangle(Shape):
    def __init__(self, length, breadth):
        self.length = length
        self.breadth = breadth

    # Overriding user defined method
    def calculate_area(self):
        return self.length * self.breadth

    # Overriding Python default method
    def __str__(self):
        return "area of rectangle = " + str(self.calculate_area())
```

---

# 🚀 Example Usage

```python
c = Circle(5)
c.set_color("red")
print("Circle area =", c.calculate_area())
print("Colored cost =", c.color_the_shape())

r = Rectangle(5, 10)
print(r)
```

---

# 🧠 Key OOP Concepts

| Concept | Description |
|---------|------------|
| Class | Blueprint for objects |
| Object | Instance of a class |
| Constructor | Special method `__init__` |
| Encapsulation | Binding data and methods together |
| Inheritance | One class derives from another |
| Polymorphism | Same method name, different behavior |
| Method Overriding | Redefining parent method in child class |

---

 Project
