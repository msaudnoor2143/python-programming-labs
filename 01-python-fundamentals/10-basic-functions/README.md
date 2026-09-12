# 🧠 Lab 10 — Basic Functions

## 🎯 Objective

Learn the fundamentals of Python functions and understand how to define and call functions using parameters, default values, and keyword arguments.

---

## 📚 Prerequisites

- Basic Python syntax
- Familiarity with running Python scripts
- Python 3 environment

---

## 📁 Lab Structure

```text
10-basic-functions/
├── README.md
├── basic_functions.py
└── screenshots/
```

---

# 🧠 Introduction

A function is a reusable block of code designed to perform a specific action.

Functions help make programs:

- More modular
- Easier to understand
- Easier to maintain
- More reusable

---

# 🧪 Task 1 — Define a Function

Create:

```text
basic_functions.py
```

Define a function called `greet()`.

```python
def greet(name):
    return f"Hello, {name}!"
```

### Explanation

### Function Definition

The keyword:

```python
def
```

starts a function definition.

### Parameter

`name` is the parameter that receives input.

### Return Statement

The `return` statement sends a value back to the caller.

---

# 🧪 Task 2 — Call the Function

Call the function with different names.

```python
print(greet("Alice"))
print(greet("Bob"))
print(greet("Charlie"))
```

### Expected Output

```text
Hello, Alice!
Hello, Bob!
Hello, Charlie!
```

---

# 🧪 Task 3 — Use a Default Parameter

Modify the function so that `name` has a default value.

```python
def greet(name="Guest"):
    return f"Hello, {name}!"
```

Call it without an argument:

```python
print(greet())
```

### Expected Output

```text
Hello, Guest!
```

A default parameter is used when the caller does not provide a value.

---

# 🧪 Task 4 — Use a Keyword Argument

Call the function using the parameter name.

```python
print(greet(name="Diana"))
```

### Expected Output

```text
Hello, Diana!
```

Keyword arguments make the relationship between the argument and parameter explicit.

---

# 🔎 Function Reference

| Concept | Example |
|---|---|
| Define function | `def greet():` |
| Parameter | `def greet(name):` |
| Call function | `greet("Alice")` |
| Return value | `return value` |
| Default parameter | `name="Guest"` |
| Keyword argument | `greet(name="Diana")` |

---

# 🛡️ Security Perspective

Functions are important in cybersecurity automation because they allow repeated security tasks to be organized into reusable components.

For example, a larger security program may contain functions for:

- Processing logs
- Checking input
- Analyzing events
- Formatting alerts
- Validating data
- Performing repetitive tasks

Breaking a security script into functions makes the program easier to maintain and test.

---

# 🧪 Case Study — User Log Service

Consider a system that generates personalized messages for users.

A reusable function can provide a consistent way to generate those messages:

```python
def greet(name="Guest"):
    return f"Hello, {name}!"

print(greet("Alice"))
print(greet())
```

This demonstrates how functions can dynamically process input.

---

# 🧪 Further Exploration

Experiment with functions that:

- Accept multiple parameters
- Return multiple values
- Perform calculations
- Process lists
- Validate input

Example:

```python
def add_numbers(a, b):
    return a + b

print(add_numbers(10, 20))
```

---

# 📝 Self-Check Questions

1. What is a function?
2. Why are functions useful?
3. What does `def` do?
4. What is a parameter?
5. What does `return` do?
6. What is a default parameter?
7. What is a keyword argument?
8. What happens when `greet()` is called without an argument?

---

# ✅ Lab Completion Checklist

- [ ] I can define a function.
- [ ] I can call a function.
- [ ] I understand parameters.
- [ ] I understand return values.
- [ ] I can use default parameters.
- [ ] I can use keyword arguments.
- [ ] I completed the greeting case study.
- [ ] I experimented with another function.

---

## 📸 Evidence

Recommended screenshots:

- Function definition in VS Code
- Function execution
- Multiple greeting outputs
- Default parameter output
- Keyword argument output

Store evidence in:

```text
screenshots/
```

---

## 📌 Summary

This lab introduced reusable Python functions and demonstrated parameters, return values, default parameters, and keyword arguments.

Functions are an essential foundation for larger Python applications, automation scripts, and cybersecurity tooling.

## 🎉 Section 01 Complete

You have now completed the documentation for all **10 Python Fundamentals labs**:

1. Installing Python & Environment Setup
2. Hello World & Basic Syntax
3. Data Types & Variables
4. Arithmetic & Expressions
5. Understanding Conditionals
6. For & While Loops
7. Lists & List Methods
8. Tuples & Sets
9. Dictionaries & Key Operations
10. Basic Functions

## 🚀 Next Section

**Section 02 — Modules, Files & Error Handling**

Labs 11–16.
