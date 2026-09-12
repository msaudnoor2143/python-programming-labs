# 🔀 Lab 05 — Understanding Conditionals (`if`, `elif`, `else`)

## 🎯 Objective

Understand how conditional statements control program flow and practice using `if`, `elif`, and `else` to handle multiple conditions.

---

## 📚 Prerequisites

- Basic Python syntax
- Familiarity with variables
- Understanding of basic data types
- Python 3 installed

---

## 📁 Lab Structure

```text
05-conditionals/
├── README.md
├── conditionals.py
└── screenshots/
```

---

# 🧪 Lab Tasks

## Task 1 — User Input and Number Classification

Create a program that determines whether a number is:

- Positive
- Negative
- Zero

```python
number = float(input("Enter a number: "))

if number > 0:
    print("Positive")
elif number < 0:
    print("Negative")
else:
    print("Zero")
```

### How It Works

The `if` statement checks whether the number is greater than zero.

The `elif` statement checks whether it is less than zero.

The `else` statement handles the remaining case, where the number is zero.

---

# 🧪 Task 2 — Multiple Conditions with `elif`

Create a simple grading system.

```python
score = int(input("Enter your score: "))

if score >= 90:
    print("Grade: A")
elif score >= 80:
    print("Grade: B")
elif score >= 70:
    print("Grade: C")
elif score >= 60:
    print("Grade: D")
else:
    print("Grade: F")
```

### Key Concept

`elif` allows a program to evaluate multiple conditions.

Once a true condition is found, the remaining `elif` and `else` blocks are skipped.

---

# 🧠 Understanding Conditional Flow

A basic conditional structure is:

```python
if condition:
    # code
elif another_condition:
    # code
else:
    # code
```

Python uses indentation to identify the code belonging to each condition.

---

# 🔎 Conditional Reference

| Keyword | Purpose |
|---|---|
| `if` | Tests the first condition |
| `elif` | Tests another condition |
| `else` | Handles remaining cases |

---

# 🛡️ Security Perspective

Conditional logic is fundamental to security-related programming.

Security applications frequently make decisions based on conditions such as:

- Authentication status
- Access permissions
- Risk levels
- Alert thresholds
- Input validation
- System states

For example, a monitoring program may generate an alert when a security value exceeds a defined threshold.

Correct conditional logic is therefore important for reliable security automation.

---

# 🧪 Practical Exercise

Modify the grading example so that it also rejects invalid scores outside the expected range.

Think about:

```text
Negative score
Score above 100
Valid score
```

---

# 📝 Self-Check Questions

1. What does an `if` statement do?
2. What is the purpose of `elif`?
3. When is `else` executed?
4. Can a program contain multiple `elif` statements?
5. Why is indentation important in Python conditionals?
6. What happens after Python finds a true `elif` condition?

---

# ✅ Lab Completion Checklist

- [ ] I understand conditional logic.
- [ ] I can use `if`.
- [ ] I can use `elif`.
- [ ] I can use `else`.
- [ ] I can classify numerical input.
- [ ] I can create multiple conditions.
- [ ] I understand how Python evaluates conditional branches.

---

## 📸 Evidence

Recommended screenshots:

- Conditional script
- Positive number test
- Negative number test
- Zero test
- Grading system output

Store evidence in:

```text
screenshots/
```

---

## 📌 Summary

This lab introduced conditional programming using `if`, `elif`, and `else`. These statements allow Python programs to make decisions based on conditions.

## 🚀 Next Lab

**Lab 06 — For & While Loops**
