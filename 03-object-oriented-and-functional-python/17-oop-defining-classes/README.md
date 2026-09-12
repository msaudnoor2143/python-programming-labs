# 🧩 Lab 17 — OOP: Defining Classes

## 🎯 Objective

Learn the fundamentals of Object-Oriented Programming (OOP) in Python by defining classes and creating objects.

By completing this lab, you will learn how to:

- Define a Python class.
- Create objects from a class.
- Define attributes.
- Define methods.
- Use the `__init__()` constructor.
- Access and modify object attributes.
- Understand the relationship between classes and objects.

---

## 📚 Prerequisites

Before starting this lab, you should understand:

- Python variables and data types.
- Functions.
- Function parameters.
- Basic control flow.
- Basic Python syntax.

---

## 🧠 Key Concepts

### Object-Oriented Programming

Object-Oriented Programming is a programming approach that organizes code around objects containing data and behavior.

A class acts as a blueprint for creating objects.

---

### Class

A class defines the structure and behavior of objects.

Example:

```python
class Student:
    pass
```

---

### Object

An object is an instance of a class.

Example:

```python
student1 = Student()
```

---

### Attributes

Attributes represent data associated with an object.

Example:

```python
self.name = name
self.age = age
```

---

### Methods

Methods are functions defined inside a class.

Example:

```python
def introduce(self):
    print(f"My name is {self.name}.")
```

---

### Constructor

The `__init__()` method is commonly used to initialize object attributes when an object is created.

---

# 🧪 Practical Lab

## Task 1 — Create a Class

Create a file:

```text
student.py
```

Define a `Student` class:

```python
class Student:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def introduce(self):
        print(f"My name is {self.name} and I am {self.age} years old.")
```

---

## Task 2 — Create Objects

Create objects from the class:

```python
student1 = Student("Alice", 20)
student2 = Student("Bob", 22)
```

Call the method:

```python
student1.introduce()
student2.introduce()
```

Expected output:

```text
My name is Alice and I am 20 years old.
My name is Bob and I am 22 years old.
```

---

## Task 3 — Access Attributes

Access individual attributes:

```python
print(student1.name)
print(student1.age)
```

Expected output:

```text
Alice
20
```

---

## Task 4 — Modify an Attribute

Modify an object's attribute:

```python
student1.age = 21

print(student1.age)
```

Expected output:

```text
21
```

This demonstrates that an object's attributes can be changed after creation.

---

## 🔎 What You Practiced

This lab demonstrated:

- Classes.
- Objects.
- Constructors.
- Attributes.
- Methods.
- Object creation.
- Attribute access.
- Attribute modification.

---

## 🧠 Class vs Object

A useful way to understand the relationship is:

```text
Class
 │
 ├── Object 1
 │
 ├── Object 2
 │
 └── Object 3
```

The class provides the blueprint, while each object represents an individual instance of that blueprint.

---

## 🛡️ Cybersecurity Perspective

OOP is useful for building larger cybersecurity applications.

For example, a security monitoring application could represent different entities as objects:

```text
SecurityTool
 ├── Scanner
 ├── LogAnalyzer
 └── AlertManager
```

Classes can help organize:

- Security events.
- Network devices.
- Users.
- Alerts.
- Log records.
- Security tools.

This becomes particularly useful as cybersecurity projects become larger and more complex.

---

## 📸 Evidence

Recommended evidence:

- Class definition.
- Successful object creation.
- Method execution.
- Attribute modification.
- Program output.

Screenshots should demonstrate meaningful execution results.

---

## 📝 Self-Check

- [ ] Can I define a class?
- [ ] Can I create an object?
- [ ] Can I explain what `self` represents?
- [ ] Can I use `__init__()`?
- [ ] Can I define a method?
- [ ] Can I access an object's attributes?

---

## ✅ Completion Checklist

- [ ] `Student` class created
- [ ] `__init__()` implemented
- [ ] Attributes created
- [ ] Method implemented
- [ ] Multiple objects created
- [ ] Methods executed
- [ ] Attributes accessed
- [ ] Attribute modification tested
- [ ] Output verified
- [ ] Evidence added where useful

---

## 🏁 Conclusion

This lab introduced the fundamentals of Object-Oriented Programming in Python.

Classes and objects provide a structured way to represent data and behavior and form the foundation for building larger Python applications.

---

## 🚀 Next Lab

**Lab 18 — OOP: Inheritance Basics**
