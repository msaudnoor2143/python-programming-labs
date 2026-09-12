# 📦 Lab 11 — Modules & Packages

## 🎯 Objective

Understand how Python modules and packages organize code into reusable components.

By completing this lab, you will learn how to:

- Create a Python module.
- Define functions inside a module.
- Import and use a custom module.
- Understand Python packages.
- Create a package using `__init__.py`.
- Import modules from a package.
- Improve code organization and reusability.

---

## 📚 Prerequisites

Before starting this lab, you should have:

- Basic Python programming knowledge.
- Understanding of functions and variables.
- Python 3.x installed.
- A text editor or IDE such as VS Code.

---

## 🧠 Key Concepts

### Module

A module is a Python file containing definitions and statements that can be reused by another Python program.

A module normally uses the `.py` extension.

Example:

```python
def add(a, b):
    return a + b
```

---

### Package

A package is a directory used to organize related Python modules.

A basic package structure can look like:

```text
project/
├── main.py
└── mypackage/
    ├── __init__.py
    └── mymodule.py
```

The `__init__.py` file is used as part of the package structure.

---

# 🧪 Practical Lab

## Task 1 — Create and Use a Python Module

Create a file named:

```text
mymodule.py
```

Add the following function:

```python
def add(a, b):
    """Returns the sum of two numbers."""
    return a + b
```

Create another file named:

```text
main.py
```

Import the module and use its function:

```python
import mymodule

result = mymodule.add(5, 3)

print(f"The sum of 5 and 3 is {result}")
```

Run the program:

```bash
python main.py
```

Expected output:

```text
The sum of 5 and 3 is 8
```

---

## Task 2 — Create a Python Package

Create the following structure:

```text
project/
├── main.py
└── mypackage/
    ├── __init__.py
    └── mymodule.py
```

Move `mymodule.py` into the `mypackage` directory.

The package can contain the same function:

```python
def add(a, b):
    """Returns the sum of two numbers."""
    return a + b
```

Update `main.py`:

```python
from mypackage import mymodule

result = mymodule.add(5, 3)

print(f"The sum of 5 and 3 is {result}")
```

Run:

```bash
python main.py
```

Expected output:

```text
The sum of 5 and 3 is 8
```

---

## 🔎 What You Practiced

This lab demonstrated:

- Creating modules.
- Importing modules.
- Calling functions from another file.
- Creating packages.
- Organizing modules into packages.
- Reusing Python code.

---

## 🛡️ Cybersecurity Perspective

Modules and packages are important when building larger cybersecurity projects.

For example, a security automation project could be organized into separate components:

```text
security_tool/
├── main.py
├── scanner/
│   ├── __init__.py
│   └── network.py
├── logging/
│   ├── __init__.py
│   └── security_logs.py
└── utilities/
    ├── __init__.py
    └── helpers.py
```

This type of organization makes security scripts easier to maintain, test, and extend.

---

## 📸 Evidence

Recommended evidence:

- Module execution showing the expected result.
- Package structure.
- Successful execution of the package-based version.

Avoid screenshots that do not provide meaningful technical evidence.

---

## 🧠 Key Takeaways

- A module is a reusable Python file.
- Packages organize related modules.
- `import` allows functionality to be reused.
- Good code organization improves maintainability.
- Modular design becomes increasingly important as projects grow.

---

## 📝 Self-Check

- [ ] Can I create a Python module?
- [ ] Can I import my own module?
- [ ] Can I create a package?
- [ ] Can I import a module from a package?
- [ ] Can I explain why modular code is useful?

---

## ✅ Completion Checklist

- [ ] `mymodule.py` created
- [ ] `add()` function implemented
- [ ] `main.py` created
- [ ] Module successfully imported
- [ ] Package created
- [ ] `__init__.py` added
- [ ] Package import tested
- [ ] Output verified
- [ ] Evidence added where useful

---

## 🏁 Conclusion

This lab introduced Python modules and packages as mechanisms for organizing and reusing code.

Understanding modular structure provides an important foundation for developing larger Python applications and automation projects.

---

## 🚀 Next Lab

**Lab 12 — File I/O Basics**
