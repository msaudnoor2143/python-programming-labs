# 🗂️ Lab 09 — Dictionaries & Key Operations

## 🎯 Objective

Understand Python dictionaries and practice adding, accessing, updating, removing, and iterating over dictionary entries.

---

## 📚 Prerequisites

- Basic Python syntax
- Understanding of data types
- Familiarity with lists
- Familiarity with loops

---

## 📁 Lab Structure

```text
09-dictionaries-and-key-operations/
├── README.md
├── dictionaries.py
└── screenshots/
```

---

# 🧠 Introduction

A dictionary stores information using **key-value pairs**.

Example:

```python
user_profile = {
    "name": "Alice",
    "age": 30,
    "city": "New York"
}
```

Each key identifies a corresponding value.

---

# 🧪 Task 1 — Create a User Profile

Create the dictionary:

```python
user_profile = {
    "name": "Alice",
    "age": 30,
    "city": "New York"
}

print(user_profile)
```

---

# 🧪 Task 2 — Access and Update Values

Access the `name` value:

```python
print("User's Name:", user_profile["name"])
```

Update the age:

```python
user_profile["age"] = 31

print("Updated User Profile:", user_profile)
```

Dictionary values can be accessed and updated using their keys.

---

# 🧪 Task 3 — Remove a Key

Remove the `city` entry using `pop()`.

```python
user_profile.pop("city")

print("Profile after removing city:", user_profile)
```

The `pop()` method removes the specified key and returns its value.

---

# 🧪 Task 4 — Iterate Over Dictionary Items

Use `.items()` to access keys and values.

```python
for key, value in user_profile.items():
    print(f"{key}: {value}")
```

---

# 🧪 Task 5 — Iterate Over Dictionary Keys

Use `.keys()` to iterate through dictionary keys.

```python
for key in user_profile.keys():
    print(f"Key: {key}")
```

---

# 🔎 Dictionary Method Reference

| Operation | Purpose |
|---|---|
| `dict[key]` | Access a value |
| `dict[key] = value` | Add/update a value |
| `.pop()` | Remove a key |
| `.items()` | Iterate over key-value pairs |
| `.keys()` | Iterate over keys |

---

# 🛡️ Security Perspective

Dictionaries are extremely useful in cybersecurity because they allow information to be organized using meaningful keys.

Examples include:

```python
security_event = {
    "source_ip": "192.0.2.10",
    "severity": "high",
    "event_type": "failed_login"
}
```

Dictionaries can therefore be useful for:

- Log processing
- Security events
- Configuration data
- User information
- API responses
- JSON data

---

# 🧪 Practical Exercise

Create a dictionary representing a security event.

Include keys such as:

```text
event_type
source_ip
severity
status
```

Then:

1. Print the dictionary.
2. Access one value.
3. Update a value.
4. Remove a key.
5. Iterate through the remaining entries.

---

# 📝 Self-Check Questions

1. What is a dictionary?
2. What is a key-value pair?
3. How do you access a dictionary value?
4. How do you update a dictionary value?
5. What does `pop()` do?
6. What does `.items()` return?
7. What does `.keys()` provide?
8. Why are dictionaries useful for structured security data?

---

# ✅ Lab Completion Checklist

- [ ] I can create a dictionary.
- [ ] I understand key-value pairs.
- [ ] I can access dictionary values.
- [ ] I can update values.
- [ ] I can remove keys.
- [ ] I can iterate over dictionary items.
- [ ] I can iterate over dictionary keys.
- [ ] I completed the security-event exercise.

---

## 📸 Evidence

Recommended screenshots:

- Dictionary creation
- Updated dictionary
- Removed key
- `.items()` iteration
- `.keys()` iteration

Store evidence in:

```text
screenshots/
```

---

## 📌 Summary

This lab provided hands-on experience with Python dictionaries and their fundamental operations. Dictionaries are particularly useful for representing structured information and processing security-related data.

## 🚀 Next Lab

**Lab 10 — Basic Functions**
