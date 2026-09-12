# 🐍 Lab 03 — Data Types & Variables

## 🎯 Objective

Understand Python variables and common data types, learn how to inspect variable types, and practice implicit and explicit type casting.

By completing this lab, you will work with:

- Strings
- Integers
- Booleans
- Floating-point numbers
- Variables
- `type()`
- Implicit type casting
- Explicit type casting

---

## 📚 Prerequisites

- Basic understanding of Python programming
- Python 3 installed
- Ability to create and run Python scripts

---

## 📁 Lab Structure

```text
03-data-types-and-variables/
├── README.md
├── data_types_variables.py
└── screenshots/
```

---

# 🧪 Lab Tasks

## Task 1 — Understanding and Creating Variables

Create variables using different Python data types.

```python
# Creating variables of different data types

name = "John Doe"
age = 25
is_student = True
height = 175.5

print("Name:", name, "Type:", type(name))
print("Age:", age, "Type:", type(age))
print("Is Student:", is_student, "Type:", type(is_student))
print("Height:", height, "Type:", type(height))
```

### Expected Concepts

| Variable | Data Type |
|---|---|
| `name` | `str` |
| `age` | `int` |
| `is_student` | `bool` |
| `height` | `float` |

The `type()` function can be used to determine the type of a value.

---

## Task 2 — Implicit vs Explicit Type Casting

### Implicit Casting

Python can automatically convert compatible numeric types when performing operations.

```python
a = 10
b = 10.5

result = a + b

print("Result:", result)
print("Type:", type(result))
```

The integer is automatically handled as part of a floating-point calculation.

### Explicit Casting

Explicit casting means manually converting a value from one type to another.

```python
age = 25

age_str = str(age)

print("Age as string:", age_str)
print("Type:", type(age_str))
```

Convert a string to an integer:

```python
number_str = "100"

number_int = int(number_str)

print("Number:", number_int)
print("Type:", type(number_int))
```

Other common conversion functions include:

```python
int()
float()
str()
bool()
```

---

# 🧪 Task 3 — Case Study: Customer Data Intake

Consider a system that receives customer information.

Some values may initially arrive as strings and need to be converted before processing.

```python
customer_name = "Alice Johnson"
customer_age = "30"
customer_membership = "True"

customer_age = int(customer_age)
customer_membership = customer_membership == "True"

print("Customer Name:", customer_name, "Type:", type(customer_name))
print("Customer Age:", customer_age, "Type:", type(customer_age))
print("Customer Membership Status:", customer_membership, "Type:", type(customer_membership))
```

### Why This Matters

Applications frequently receive data as strings from:

- User input
- Files
- APIs
- Forms
- Configuration data

Correct type conversion allows programs to process that information appropriately.

---

# 🔎 Command Reference

| Function | Purpose |
|---|---|
| `type()` | Checks the type of a value |
| `int()` | Converts a value to an integer |
| `float()` | Converts a value to a floating-point number |
| `str()` | Converts a value to a string |
| `bool()` | Converts a value to a Boolean |

---

# 🧠 Key Concepts

### Variables

Variables store values that can be used throughout a program.

```python
name = "John"
age = 25
```

### Data Types

Python provides different built-in data types for representing different kinds of information.

```python
text = "Python"
number = 10
decimal = 10.5
active = True
```

### Type Inspection

```python
print(type(number))
```

### Type Casting

Type casting converts a value from one data type to another.

```python
number = int("100")
```

---

# 🛡️ Security Perspective

Data types and type conversion are important when handling information from external sources.

Security-sensitive applications should not blindly assume that incoming data has the expected type.

For example, data received from:

- Users
- Network requests
- Files
- APIs
- Configuration sources

should be validated and converted carefully before processing.

---

# 📝 Self-Check Questions

1. What is a variable?
2. What is the difference between `int` and `float`?
3. What data type represents text?
4. What does `type()` do?
5. What is implicit type casting?
6. What is explicit type casting?
7. What does `int("100")` produce?
8. Why is type conversion important when processing external data?

---

# ✅ Lab Completion Checklist

- [ ] I can create Python variables.
- [ ] I understand common Python data types.
- [ ] I can use `type()`.
- [ ] I understand implicit casting.
- [ ] I can perform explicit casting.
- [ ] I can convert strings into numbers.
- [ ] I understand why data types matter when processing data.
- [ ] I completed the customer data case study.

---

## 📸 Evidence

Recommended screenshots:

- Python script in VS Code
- Terminal showing the program output
- Output showing the detected data types
- Customer data case study output

Store meaningful evidence inside:

```text
screenshots/
```

---

## 📌 Summary

In this lab, you worked with Python variables and common data types. You also explored implicit and explicit type casting and applied these concepts to a customer data intake example.

## 🚀 Next Lab

**Lab 04 — Arithmetic & Expressions**
