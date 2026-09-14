# 📝 Lab 32 — Logging with Python's Logging Module

This lab introduces Python's built-in `logging` module and demonstrates how applications can record runtime information using different logging levels and formats.

---

## 🎯 Objective

By completing this lab, you will:

- Understand the importance of logging.
- Use Python's built-in `logging` module.
- Configure logging levels.
- Format log messages.
- Generate messages at different severity levels.
- Implement logging in a Python function.

---

## 📚 Prerequisites

- Basic Python programming knowledge.
- Python installed on your system.
- Familiarity with running Python scripts.

---

## 🧠 Introduction

Logging is an important part of software development and maintenance.

It helps developers understand application behavior, troubleshoot problems, and track important runtime information.

Python provides the built-in `logging` module for creating structured log messages.

---

## 🧪 Lab Tasks

### Task 1 — Import the Logging Module

```python
import logging
```

The `logging` module is part of Python's Standard Library.

---

### Task 2 — Set the Logging Level

Logging levels categorize the importance of messages.

```python
logging.basicConfig(level=logging.DEBUG)
```

The main levels are:

| Level | Purpose |
|---|---|
| `DEBUG` | Detailed diagnostic information |
| `INFO` | Confirmation that things are working normally |
| `WARNING` | Something unexpected happened or may become a problem |
| `ERROR` | A more serious problem prevented some operation |
| `CRITICAL` | A very serious problem that may prevent the program from continuing |

---

### Task 3 — Format Log Messages

A logging format can improve readability and consistency.

```python
logging.basicConfig(
    format='%(asctime)s - %(levelname)s - %(message)s'
)
```

Important format fields include:

- `%(asctime)s` — time of the log record.
- `%(levelname)s` — logging level.
- `%(message)s` — log message.

---

### Task 4 — Generate Messages at Different Levels

```python
logging.debug("This is a debug message.")
logging.info("This is an info message.")
logging.warning("This is a warning message.")
logging.error("This is an error message.")
logging.critical("This is a critical message.")
```

Each logging function corresponds to a severity level.

---

## 🔬 Complete Logging Example

```python
import logging


logging.basicConfig(
    level=logging.DEBUG,
    format='%(asctime)s - %(levelname)s - %(message)s'
)


logging.debug("This is a debug message.")
logging.info("This is an info message.")
logging.warning("This is a warning message.")
logging.error("This is an error message.")
logging.critical("This is a critical message.")
```

---

## 🧪 Task 5 — Practical Application of Logging

Implement logging inside a function.

```python
def divide_numbers(a, b):
    try:
        result = a / b
        logging.info("Division successful.")
        return result
    except ZeroDivisionError:
        logging.error("Division by zero error.")
        return None


result = divide_numbers(10, 0)
```

The function records:

- An `INFO` message when division succeeds.
- An `ERROR` message when division by zero occurs.

---

## 🔬 Complete Practical Example

```python
import logging


logging.basicConfig(
    level=logging.DEBUG,
    format='%(asctime)s - %(levelname)s - %(message)s'
)


def divide_numbers(a, b):
    try:
        result = a / b
        logging.info("Division successful.")
        return result
    except ZeroDivisionError:
        logging.error("Division by zero error.")
        return None


result = divide_numbers(10, 0)
```

---

## 🛡️ Cybersecurity Perspective

Logging is especially important in cybersecurity.

Security systems rely heavily on logs to understand what happened during an event.

Logging can support:

- Security monitoring.
- Troubleshooting.
- Incident investigation.
- Application monitoring.
- Error detection.
- Security-event analysis.

This makes logging a fundamental concept when working with SIEM and security-monitoring systems.

---

## 📸 Evidence / Screenshots

Capture:

- Logging source code.
- Terminal output showing timestamps and levels.
- `DEBUG`, `INFO`, `WARNING`, `ERROR`, and `CRITICAL` messages.
- The division-by-zero example producing an error log.

Suggested structure:

```text
32-logging-with-python-logging-module/
├── README.md
└── screenshots/
    ├── logging-code.png
    └── logging-output.png
```

---

## ⚠️ Best Practices

- Choose appropriate logging levels.
- Avoid logging unnecessary sensitive information.
- Use consistent log formats.
- Use `DEBUG` for detailed diagnostic information.
- Use `INFO` for normal application events.
- Use `WARNING` for unexpected conditions.
- Use `ERROR` for failed operations.
- Use `CRITICAL` for severe failures.

---

## 🧠 Self-Check

1. Why is logging important?
2. What module provides logging functionality?
3. What is the purpose of `DEBUG`?
4. What is the purpose of `INFO`?
5. What is the difference between `WARNING` and `ERROR`?
6. When should `CRITICAL` be used?
7. What does `%(asctime)s` represent?
8. Why is logging important for cybersecurity?

---

## ✅ Completion Checklist

- [ ] Imported `logging`.
- [ ] Configured a logging level.
- [ ] Configured a log format.
- [ ] Generated messages at different levels.
- [ ] Implemented logging inside a function.
- [ ] Tested an error condition.
- [ ] Captured logging output.
- [ ] Reviewed the cybersecurity relevance.

---

## 🏁 Conclusion

In this lab, you learned how to use Python's built-in logging module.

You configured logging levels and formats and implemented logging in an application to track successful and failed operations.

---

## ➡️ Next Lab

**Lab 33 — Basic Web Scraping with `requests` + BeautifulSoup**
