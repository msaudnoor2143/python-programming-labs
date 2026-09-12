# 📋 Lab 07 — Lists & List Methods

## 🎯 Objective

Understand Python lists and practice creating, modifying, sorting, and iterating over list elements.

---

## 📚 Prerequisites

- Basic programming knowledge
- Familiarity with Python syntax
- Python 3 installed

---

## 📁 Lab Structure

```text
07-lists-and-list-methods/
├── README.md
├── lists_example.py
└── screenshots/
```

---

# 🧠 Introduction

A list is a Python data structure used to store multiple values.

Lists can contain multiple elements and can be modified after creation.

Example:

```python
fruits = ["apple", "banana", "cherry"]
```

---

# 🧪 Task 1 — Create a List

Create a list containing fruits.

```python
fruits = ["apple", "banana", "cherry"]

print("Initial list of fruits:", fruits)
```

---

# 🧪 Task 2 — Append a New Item

Use `append()` to add an item to the end of the list.

```python
fruits.append("orange")

print("List after appending 'orange':", fruits)
```

The new element is added to the end of the list.

---

# 🧪 Task 3 — Remove an Item

Use `remove()` to remove an item by value.

```python
fruits.remove("banana")

print("List after removing 'banana':", fruits)
```

The specified element must exist for `remove()` to work successfully.

---

# 🧪 Task 4 — Sort the List

Use `sort()` to arrange the list.

```python
fruits.sort()

print("Sorted list of fruits:", fruits)
```

By default, the method sorts items in ascending order.

---

# 🧪 Task 5 — Iterate Over the List

Use a `for` loop to process each element.

```python
for fruit in fruits:
    print("Fruit:", fruit)
```

The loop visits each element sequentially.

---

# 🔎 List Method Reference

| Method | Purpose |
|---|---|
| `append()` | Adds an item to the end |
| `remove()` | Removes an item by value |
| `sort()` | Sorts the list |
| `insert()` | Adds an item at a specific position |
| `pop()` | Removes and returns an item |

---

# 🛡️ Security Perspective

Lists are frequently used in cybersecurity programs for storing collections of:

- IP addresses
- Log entries
- File names
- Security events
- User records
- Indicators
- Scan results

For example:

```python
blocked_ips = [
    "192.0.2.10",
    "192.0.2.20",
    "192.0.2.30"
]
```

Understanding list operations is therefore useful when developing security automation and analysis scripts.

---

# 🧪 Practical Exercise

Create a list containing several security-related items, such as:

```python
security_tools = [
    "Wireshark",
    "Nmap",
    "Wazuh",
    "Suricata"
]
```

Then:

1. Add another tool.
2. Remove one tool.
3. Sort the list.
4. Print each item using a loop.

---

# 📝 Self-Check Questions

1. What is a list?
2. How do you create a list?
3. What does `append()` do?
4. What does `remove()` do?
5. What does `sort()` do?
6. How can you iterate over a list?
7. Name two additional list methods.

---

# ✅ Lab Completion Checklist

- [ ] I can create a list.
- [ ] I can add elements using `append()`.
- [ ] I can remove elements using `remove()`.
- [ ] I can sort a list.
- [ ] I can iterate through a list.
- [ ] I understand common list methods.
- [ ] I completed the practical exercise.

---

## 📸 Evidence

Recommended screenshots:

- List creation and output
- Appending an element
- Removing an element
- Sorted list
- Iteration output

Store evidence in:

```text
screenshots/
```

---

## 📌 Summary

In this lab, you created and manipulated Python lists using common built-in methods. Lists are fundamental data structures and are widely used in automation, data processing, and cybersecurity scripts.

## 🚀 Next Lab

**Lab 08 — Tuples & Sets**
