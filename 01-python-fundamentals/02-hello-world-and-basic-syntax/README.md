# 🐍 Lab 02 — Hello World & Basic Syntax

## 🎯 Objective

This lab introduces the basic structure and execution of a Python program.

By completing this lab, you will:

- Create a simple Python script.
- Execute a Python script from the command line.
- Understand Python indentation.
- Understand how indentation defines code blocks.
- Experiment with a basic `if` statement.
- Identify and resolve an `IndentationError`.

---

## 📚 Prerequisites

- Python 3 installed and verified.
- Basic command-line navigation.
- A text editor or IDE such as Visual Studio Code.
- Completion of **Lab 01 — Installing Python & Environment Setup**.

---

## 🗂️ Lab Structure

```text
02-hello-world-and-basic-syntax/
├── README.md
└── hello.py
```

---

## 🧪 Task 1 — Create a Simple Python Script

Create a file named:

```text
hello.py
```

Add the following code:

```python
print("Hello, World!")
```

This demonstrates the basic use of Python's `print()` function to display information in the terminal.

---

## ▶️ Task 2 — Run the Python Script

Navigate to the lab directory:

```bash
cd ~/python-programming-labs/01-python-fundamentals/02-hello-world-and-basic-syntax
```

Run the program:

```bash
python3 hello.py
```

Expected output:

```text
Hello, World!
```

The Python interpreter reads the `.py` file and executes its instructions.

---

## 🧱 Task 3 — Experiment with Indentation

Python uses indentation to define code blocks.

Example:

```python
if True:
    print("This will always print because the condition is True.")

print("Hello, World!")
```

The `print()` statement inside the `if` block is indented.

The indentation tells Python that the statement belongs to the `if` block.

---

## ⚠️ Task 4 — Observe an Indentation Error

Incorrect indentation:

```python
if True:
print("This will cause an IndentationError.")
```

Running this code produces an `IndentationError` because the statement belonging to the `if` block is not indented.

The corrected version is:

```python
if True:
    print("This will always print because the condition is True.")
```

### Key Lesson

Indentation in Python is part of the language syntax.

It is not simply visual formatting.

---

## 🔬 Practical Exercise

Modify `hello.py` so that it contains:

1. A Hello World message.
2. A simple `if` block.
3. A second message outside the `if` block.

Example:

```python
print("Hello, World!")

if True:
    print("This message is inside the if block.")

print("This message is outside the if block.")
```

Run the program:

```bash
python3 hello.py
```

Expected output:

```text
Hello, World!
This message is inside the if block.
This message is outside the if block.
```

---

## 🔎 Command Reference

| Command | Purpose |
|---|---|
| `cd <directory>` | Change directory |
| `python3 hello.py` | Execute the Python script |
| `pwd` | Display the current directory |
| `ls` | List directory contents |

---

## 🧠 Key Concepts

### `print()`

The `print()` function displays information in the terminal.

```python
print("Hello, World!")
```

### `if`

The `if` statement is used to conditionally execute a block of code.

```python
if True:
    print("Condition is true.")
```

### Indentation

Python uses indentation to define code blocks.

```python
if True:
    print("Inside the block.")
```

The indented statement belongs to the `if` block.

### `IndentationError`

Python reports an `IndentationError` when required indentation is missing or incorrectly structured.

---

## 🛡️ Security Perspective

Understanding Python syntax and indentation is important when developing cybersecurity automation and defensive security tools.

Security scripts commonly contain:

- Conditional checks.
- Log-processing logic.
- Validation routines.
- File-processing operations.
- Detection rules.
- Automation workflows.

A simple indentation mistake can prevent a security script from executing correctly.

Reliable syntax, testing, and code organization are therefore important when developing security automation.

---

## 📸 Evidence

Screenshots should be added when they provide useful evidence of the lab work.

Recommended evidence includes:

- Successful execution of `hello.py`.
- Terminal output showing the program result.
- The `IndentationError` experiment.
- Corrected execution after fixing the indentation.

Screenshots should demonstrate actual work rather than being added purely for decoration.

---

## 📝 Self-Check Questions

1. How do you execute a Python script from the Linux terminal?
2. What does the `print()` function do?
3. Why is indentation important in Python?
4. What happens when required indentation is missing?
5. How does an `if` statement define a code block?

---

## 🏁 Lab Completion Checklist

- [ ] Created `hello.py`.
- [ ] Successfully executed the Python script.
- [ ] Practiced Python indentation.
- [ ] Observed an `IndentationError`.
- [ ] Corrected the indentation.
- [ ] Completed the practical exercise.
- [ ] Added useful evidence screenshots.

---

## 📌 Summary

In this lab, you created and executed a basic Python program and learned how indentation defines code blocks.

You also practiced using an `if` statement and identified how incorrect indentation produces an `IndentationError`.

These fundamentals provide the foundation for the more advanced Python concepts covered in later labs.

---

## 🚀 Next Lab

**Lab 03 — Data Types & Variables**
