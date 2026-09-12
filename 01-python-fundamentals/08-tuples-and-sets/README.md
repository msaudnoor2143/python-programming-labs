# 🧩 Lab 08 — Tuples & Sets

## 🎯 Objective

Understand the properties and practical uses of tuples and sets in Python.

By completing this lab, you will work with:

- Tuples
- Tuple immutability
- Sets
- Unique values
- Duplicate handling
- Membership-oriented data structures

---

## 📚 Prerequisites

- Basic Python programming
- Familiarity with lists
- Understanding of basic data structures
- Python 3 installed

---

## 📁 Lab Structure

```text
08-tuples-and-sets/
├── README.md
├── tuples_sets.py
└── screenshots/
```

---

# 🧠 Introduction

Python provides several built-in data structures.

This lab focuses on two of them:

### Tuple

A tuple is an immutable sequence of elements.

### Set

A set is a collection that maintains unique elements and is useful for membership-related operations.

---

# 🧪 Task 1 — Working with Tuples

## Subtask 1.1 — Create a Tuple

Create a tuple representing coordinates.

```python
coordinates = (10, 20, 30)

print("Coordinates Tuple:", coordinates)
```

Tuples are commonly written using parentheses:

```python
()
```

---

## Subtask 1.2 — Confirm Tuple Immutability

Attempt to modify a tuple element.

```python
try:
    coordinates[0] = 100
except TypeError as e:
    print("Error:", e)
```

This demonstrates that tuple elements cannot be modified after the tuple is created.

### Key Concept

**Immutability** means that the tuple's elements cannot be altered.

---

# 🧪 Task 2 — Working with Sets

## Subtask 2.1 — Create a Set

Create a set containing numbers.

```python
number_set = {1, 2, 3, 4, 5}

print("Initial Set:", number_set)
```

Sets use curly braces:

```python
{}
```

---

## Subtask 2.2 — Add a Duplicate

Attempt to add an existing value.

```python
number_set.add(3)

print("Set after adding duplicate:", number_set)
```

The duplicate does not create another copy of the value.

---

# 🧠 Tuple vs Set

| Feature | Tuple | Set |
|---|---|---|
| Mutable | No | Yes |
| Allows duplicates | Yes | No |
| Primary use | Fixed collections | Unique membership |
| Common syntax | `(1, 2, 3)` | `{1, 2, 3}` |

---

# 🛡️ Security Perspective

Tuples and sets can be useful when processing security data.

### Tuples

Can represent fixed pieces of information such as:

```python
connection = ("192.0.2.10", 443)
```

### Sets

Can be useful for maintaining unique values, such as unique IP addresses or identifiers.

```python
unique_ips = {
    "192.0.2.10",
    "192.0.2.20",
    "192.0.2.10"
}
```

Sets automatically maintain unique membership.

---

# 📝 Self-Check Questions

1. What is a tuple?
2. What does immutable mean?
3. Can tuple elements normally be modified?
4. What is a set?
5. Can a set contain duplicate values?
6. What is one practical use of a tuple?
7. What is one practical use of a set?
8. What is the difference between tuple and set syntax?

---

# ✅ Lab Completion Checklist

- [ ] I can create a tuple.
- [ ] I understand tuple immutability.
- [ ] I can create a set.
- [ ] I understand unique membership.
- [ ] I can add values to a set.
- [ ] I understand how duplicates are handled.
- [ ] I understand practical uses for tuples and sets.

---

## 📸 Evidence

Recommended screenshots:

- Tuple creation output
- Tuple immutability error
- Set creation
- Set duplicate behavior

Store evidence in:

```text
screenshots/
```

---

## 📌 Summary

This lab demonstrated two important Python data structures. Tuples provide immutable collections, while sets provide collections focused on unique membership and duplicate elimination.

## 🚀 Next Lab

**Lab 09 — Dictionaries & Key Operations**
