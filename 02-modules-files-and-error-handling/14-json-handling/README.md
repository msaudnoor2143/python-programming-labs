# 🔄 Lab 14 — JSON Handling

## 🎯 Objective

Learn how Python works with JSON data and understand how JSON can be used for storing and exchanging structured information.

By completing this lab, you will learn how to:

- Create Python dictionaries.
- Convert Python data into JSON.
- Write JSON data to a file.
- Read JSON data from a file.
- Understand `json.dumps()`.
- Understand `json.load()`.
- Recognize common uses of JSON.

---

## 📚 Prerequisites

Before starting this lab, you should have:

- Basic Python programming knowledge.
- Understanding of dictionaries and lists.
- Basic knowledge of file handling.

---

## 🧠 Key Concepts

### JSON

JSON is a text-based format commonly used to represent structured data.

A Python dictionary can be converted into a JSON representation.

---

### `json.dumps()`

`json.dumps()` converts a Python object into a JSON string.

Example:

```python
import json

data_json = json.dumps(data, indent=4)
```

---

### `json.load()`

`json.load()` reads JSON data from a file and converts it into a Python object.

Example:

```python
with open("data.json", "r") as json_file:
    data = json.load(json_file)
```

---

# 🧪 Practical Lab

## Task 1 — Create a Python Dictionary

Create employee information:

```python
employee_data = {
    "name": "John Doe",
    "age": 30,
    "department": "Engineering",
    "skills": ["Python", "Django", "Machine Learning"]
}
```

---

## Task 2 — Convert the Dictionary to JSON

Import the JSON module:

```python
import json
```

Convert the dictionary:

```python
employee_data_json = json.dumps(employee_data, indent=4)

print(employee_data_json)
```

The `indent=4` argument makes the resulting JSON easier to read.

---

## Task 3 — Store JSON in a File

Write the JSON string to:

```text
employee_data.json
```

Example:

```python
with open("employee_data.json", "w") as json_file:
    json_file.write(employee_data_json)
```

---

## Task 4 — Read JSON From the File

Read the JSON file:

```python
with open("employee_data.json", "r") as json_file:
    data = json.load(json_file)

print(data)
```

This converts the JSON data back into a Python object.

---

## 🔎 Data Flow

The process can be summarized as:

```text
Python Dictionary
       │
       ▼
   json.dumps()
       │
       ▼
   JSON String
       │
       ▼
   JSON File
       │
       ▼
    json.load()
       │
       ▼
Python Object
```

---

## 🧠 What You Practiced

This lab demonstrated:

- Python dictionaries.
- JSON serialization.
- JSON deserialization.
- `json.dumps()`.
- `json.load()`.
- Writing JSON files.
- Reading JSON files.

---

## 🛡️ Cybersecurity Perspective

JSON is widely encountered in cybersecurity and cloud environments.

Examples include:

- Security tool output.
- API responses.
- Cloud configuration data.
- Security event data.
- Automation configuration.
- Structured application data.

Many security tools and APIs use JSON because it provides a structured way to represent information.

---

## 📸 Evidence

Recommended evidence:

- Printed JSON output.
- Generated `employee_data.json`.
- Successful JSON file reading.
- Python object reconstructed from JSON.

---

## ⚠️ Best Practice

When working with JSON configuration or security-related data:

- Validate data before using it.
- Avoid exposing sensitive information.
- Keep configuration organized.
- Handle invalid or missing data appropriately.

---

## 📝 Self-Check

- [ ] Can I create a Python dictionary?
- [ ] Can I convert it to JSON?
- [ ] Do I understand `json.dumps()`?
- [ ] Can I write JSON to a file?
- [ ] Can I read JSON using `json.load()`?
- [ ] Can I explain why JSON is useful?

---

## ✅ Completion Checklist

- [ ] Employee dictionary created
- [ ] `json` module imported
- [ ] Dictionary converted to JSON
- [ ] JSON formatted with indentation
- [ ] JSON file created
- [ ] JSON file read successfully
- [ ] Data verified
- [ ] Evidence added where useful

---

## 🏁 Conclusion

This lab introduced JSON handling in Python and demonstrated how structured Python data can be converted into JSON, stored in a file, and read back into Python.

JSON handling is an important skill for modern applications, APIs, automation, cloud systems, and cybersecurity tooling.

---

## 🚀 Next Lab

**Lab 15 — Basic Debugging Techniques**
