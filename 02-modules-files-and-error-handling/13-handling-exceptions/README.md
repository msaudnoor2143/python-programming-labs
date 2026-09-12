# 🛡️ Lab 13 — Handling Exceptions

## 🎯 Objective

Learn how Python handles unexpected conditions through exception handling.

By completing this lab, you will learn how to:

- Identify situations that can generate exceptions.
- Use `try` blocks.
- Handle errors with `except`.
- Handle different exception types separately.
- Use `finally`.
- Build programs that respond more appropriately to invalid input.

---

## 📚 Prerequisites

Before starting this lab, you should understand:

- Basic Python syntax.
- Variables.
- Input and output.
- Basic data types.
- Functions and simple control flow.

---

## 🧠 Key Concepts

### Exception

An exception is an event that occurs during program execution and can interrupt normal program flow.

Python provides exception-handling mechanisms to respond to such conditions.

---

### `try`

The `try` block contains code that may produce an exception.

```python
try:
    ...
```

---

### `except`

The `except` block handles an exception.

```python
except ValueError:
    ...
```

---

### Multiple Exceptions

Different exceptions can be handled separately.

Examples include:

- `ValueError`
- `ZeroDivisionError`

---

# 🧪 Practical Lab

## Task 1 — Capture User Input

Prompt the user for a number:

```python
user_input = input("Enter a number: ")
```

---

## Task 2 — Handle Invalid Integer Input

Safely convert the input to an integer:

```python
try:
    number = int(user_input)
    print(f"The number is {number}.")
except ValueError:
    print("Error: Input is not a valid number. Please enter an integer.")
```

Test the program with valid and invalid input.

---

## Task 3 — Handle Multiple Exceptions

Use separate exception handlers:

```python
try:
    result = 10 / int(user_input)
    print(f"Result is: {result}")
except ValueError:
    print("Error: Please enter numeric values!")
except ZeroDivisionError:
    print("Error: Division by zero is undefined!")
```

This demonstrates how different errors can receive different responses.

---

## 🔎 What You Practiced

This lab demonstrated:

- `try`
- `except`
- Multiple exception handlers
- `ValueError`
- `ZeroDivisionError`
- Input validation
- Graceful error handling

---

## 🧠 Why Exception Handling Matters

Without appropriate exception handling, unexpected input or conditions can cause a program to terminate.

Exception handling allows a program to respond to expected problems in a controlled way.

---

## 🛡️ Cybersecurity Perspective

Exception handling is important in cybersecurity automation because security tools often process unpredictable data.

Examples include:

- Invalid log entries.
- Unexpected API responses.
- Missing files.
- Incorrect configuration values.
- Invalid user input.
- Unavailable resources.

A security automation script should distinguish expected errors from normal operation and provide useful information when something goes wrong.

---

## 📸 Evidence

Recommended evidence:

- Successful valid input.
- Invalid input being handled.
- Separate handling of `ValueError`.
- Separate handling of `ZeroDivisionError`.

---

## ⚠️ Best Practice

Avoid using overly broad exception handling when a specific exception type can be identified.

Prefer:

```python
except ValueError:
```

over unnecessarily catching every possible exception.

Specific exception handling makes programs easier to understand and troubleshoot.

---

## 📝 Self-Check

- [ ] Can I explain what an exception is?
- [ ] Do I understand `try` and `except`?
- [ ] Can I handle multiple exception types?
- [ ] Can I identify `ValueError`?
- [ ] Can I identify `ZeroDivisionError`?
- [ ] Can I explain why error handling matters?

---

## ✅ Completion Checklist

- [ ] User input implemented
- [ ] Integer conversion implemented
- [ ] `ValueError` handled
- [ ] Division example tested
- [ ] `ZeroDivisionError` handled
- [ ] Multiple exceptions tested
- [ ] Output verified
- [ ] Evidence added where useful

---

## 🏁 Conclusion

This lab introduced Python exception handling and demonstrated how `try` and `except` can be used to manage unexpected conditions.

Effective exception handling improves program robustness and is particularly valuable when building automation and security-related applications.

---

## 🚀 Next Lab

**Lab 14 — JSON Handling**
