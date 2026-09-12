# Lab 21 — List & Dictionary Comprehensions

> Learn how to use list and dictionary comprehensions to create and transform data efficiently and readably in Python.

---

## 🎯 Objective

By completing this lab, you will learn how to:

- Understand list comprehensions
- Create lists using concise expressions
- Understand dictionary comprehensions
- Generate dictionaries from existing data
- Compare comprehensions with traditional loops
- Use comprehensions for data transformation
- Understand how concise Python code can improve readability

---

## 📚 Prerequisites

Before starting this lab, you should have:

- Basic understanding of Python syntax
- Familiarity with lists and dictionaries
- Understanding of `for` loops
- Basic knowledge of Python expressions

Recommended previous labs:

- **Lab 07 — Lists & List Methods**
- **Lab 09 — Dictionaries & Key Operations**
- **Lab 06 — For & While Loops**

---

# 1. Introduction to Comprehensions

Comprehensions provide a concise way to create collections from existing iterables.

Python commonly provides:

- List comprehensions
- Dictionary comprehensions
- Set comprehensions
- Generator expressions

This lab focuses on list and dictionary comprehensions.

---

# 2. List Comprehensions

A list comprehension provides a compact way to create a list.

### General syntax

```python
[expression for item in iterable]
```

Instead of writing multiple lines with a loop, a comprehension can often express the same operation in a single readable statement.

---

# 3. Task 1 — Create a List of Squares

The objective is to generate the squares of numbers from `0` to `9`.

Create a Python file such as:

```text
list_comprehensions.py
```

Add:

```python
# Using list comprehension to generate squares
squares = [x**2 for x in range(10)]

print(squares)
```

### Expected output

```text
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]
```

### How it works

The expression:

```python
[x**2 for x in range(10)]
```

means:

1. Generate numbers from `0` through `9`
2. Store each number temporarily as `x`
3. Calculate `x**2`
4. Add the result to the new list

---

# 4. Task 2 — Dictionary Comprehension

Dictionary comprehensions use a similar concept but produce key-value pairs.

### General syntax

```python
{key_expression: value_expression for item in iterable}
```

Create a list of words:

```python
words = ["apple", "banana", "cherry", "date"]
```

Now create a dictionary where:

- The word becomes the key
- The length of the word becomes the value

```python
words = ["apple", "banana", "cherry", "date"]

lengths = {word: len(word) for word in words}

print(lengths)
```

### Expected output

```text
{'apple': 5, 'banana': 6, 'cherry': 6, 'date': 4}
```

The comprehension processes every word and creates a corresponding key-value pair.

---

# 5. Task 3 — Compare Comprehensions with Traditional Loops

The same list can be created using a traditional loop.

### Traditional loop

```python
squares_loop = []

for x in range(10):
    squares_loop.append(x**2)

print(squares_loop)
```

### List comprehension

```python
squares_comp = [x**2 for x in range(10)]

print(squares_comp)
```

Both approaches produce the same result.

---

# 6. Understanding the Difference

### Traditional loop

```python
squares = []

for x in range(10):
    squares.append(x**2)
```

### Comprehension

```python
squares = [x**2 for x in range(10)]
```

The comprehension is shorter and can be easier to read when the transformation is simple.

However, overly complicated comprehensions can reduce readability.

> **Best practice:** Prefer clarity over making code as short as possible.

---

# 7. Practical Data Transformation

Comprehensions are particularly useful when processing collections.

For example:

```python
numbers = [1, 2, 3, 4, 5]

squared_numbers = [number**2 for number in numbers]

print("Original:", numbers)
print("Squared:", squared_numbers)
```

Expected output:

```text
Original: [1, 2, 3, 4, 5]
Squared: [1, 4, 9, 16, 25]
```

---

# 🧠 Key Concepts

### List comprehension

Creates a list from an iterable.

```python
squares = [x**2 for x in range(10)]
```

### Dictionary comprehension

Creates a dictionary from an iterable.

```python
lengths = {word: len(word) for word in words}
```

### Traditional loop

Provides a more explicit approach:

```python
result = []

for item in items:
    result.append(item)
```

---

# 🛡️ Security Perspective

Comprehensions are useful in cybersecurity and automation when transforming collections of data.

Examples include:

- Processing log entries
- Extracting selected fields
- Filtering event data
- Transforming security records
- Preparing data for analysis
- Processing lists of IP addresses or filenames

For example, a simple transformation could be:

```python
log_levels = ["INFO", "WARNING", "ERROR", "ERROR"]

errors = [level for level in log_levels if level == "ERROR"]

print(errors)
```

Output:

```text
['ERROR', 'ERROR']
```

This demonstrates how Python can efficiently process structured security-related data.

---

# 📸 Evidence / Screenshots

For the GitHub portfolio, capture meaningful evidence such as:

- Running the list comprehension script
- The generated list of squares
- Dictionary comprehension output
- Comparison between loop and comprehension

Suggested structure:

```text
21-list-dict-comprehensions/
├── README.md
├── list_comprehensions.py
└── screenshots/
    └── comprehension-output.png
```

Screenshots are optional when the output is not visually meaningful, but execution evidence is useful for demonstrating completed practical work.

---

# ⚠️ Best Practices

- Keep comprehensions simple and readable.
- Avoid deeply nested comprehensions when a normal loop is clearer.
- Use meaningful variable names.
- Do not sacrifice readability just to reduce the number of lines.
- Test transformations with small datasets before processing large datasets.

---

# 📝 Self-Check

1. What is a list comprehension?
2. What is the general syntax of a list comprehension?
3. What is a dictionary comprehension?
4. How does a comprehension differ from a traditional loop?
5. Why can comprehensions improve readability?
6. When might a traditional loop be preferable?
7. How can comprehensions be used for data transformation?
8. How could comprehensions help process security logs?

---

# ✅ Lab Completion Checklist

- [ ] I understand list comprehensions.
- [ ] I can create a list using a comprehension.
- [ ] I understand dictionary comprehensions.
- [ ] I can create a dictionary using a comprehension.
- [ ] I can compare comprehensions with traditional loops.
- [ ] I understand their use in data transformation.
- [ ] I understand when readability should take priority over brevity.
- [ ] I completed the practical exercises.
- [ ] I captured meaningful execution evidence.

---

# 📌 Conclusion

List and dictionary comprehensions provide powerful and readable ways to create and transform collections in Python.

They can make code shorter and easier to maintain when used appropriately.

Understanding comprehensions also provides a stronger foundation for working with data-processing and automation tasks.

---

## 🚀 Next Lab

**Lab 22 — Reading CSV Files**
