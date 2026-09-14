# 🧹 Lab 39 — Python Style & PEP 8 Checks

This lab introduces Python code-quality practices based on **PEP 8** and demonstrates automated tools for checking and formatting Python code.

You will use **flake8**, **black**, and **autopep8** to identify and improve style issues.

---

## 🎯 Objective

By completing this lab, you will:

- Understand the importance of Python style guides.
- Learn the fundamentals of PEP 8.
- Use flake8 to check Python code.
- Identify style violations and coding issues.
- Use black to automatically format Python code.
- Use autopep8 to improve PEP 8 compliance.
- Understand how automated tools improve code consistency.

---

## 📚 Prerequisites

- Basic knowledge of Python programming.
- Python installed on your system.
- `pip` installed.
- Basic command-line knowledge.

---

## 🧠 Introduction

PEP 8 is the Python style guide that defines conventions for writing clear and maintainable Python code.

Following consistent coding conventions improves:

- Readability.
- Maintainability.
- Collaboration.
- Code review.
- Project consistency.

Automated tools can help developers identify and correct common style issues.

This lab focuses on:

- `flake8`
- `black`
- `autopep8`

---

# 🔎 Task 1 — Install flake8

Install flake8 using pip:

```bash
pip install flake8
```

`flake8` is commonly used to check Python code for style violations and certain coding errors.

---

# 🧪 Task 2 — Create a Sample Script

Create:

```text
example.py
```

Use the following intentionally poorly formatted code:

```python
def exampleFunction():
    x = { 'key' : 42 , 'another_key': 23 }

    if(x['key'] >0): print("Positive number")

    else:print("Zero or Negative")
```

The code contains several style issues that can be detected by a linting tool.

---

# 🔍 Task 3 — Run flake8

Run:

```bash
flake8 example.py
```

Review the warnings and errors reported by flake8.

Common issues may include:

- Naming conventions.
- Improper spacing.
- Formatting problems.
- Missing newline at the end of the file.
- Other PEP 8 violations.

Document the specific issues reported by your installation.

---

# ⚫ Task 4 — Format Code Using black

Install black:

```bash
pip install black
```

Format the script:

```bash
black example.py
```

Black will automatically reformat the file according to its formatting rules.

Review the changes made to `example.py`.

---

# 🧹 Task 5 — Format Code Using autopep8

Install autopep8:

```bash
pip install autopep8
```

Format the file:

```bash
autopep8 --in-place --aggressive --aggressive example.py
```

The `--in-place` option applies the changes directly to the file.

The aggressive options allow autopep8 to make additional formatting improvements.

---

# 🔬 Task 6 — Compare the Tools

Both black and autopep8 aim to improve Python code formatting, but they can produce different formatting results.

This can depend on:

- Tool configuration.
- Formatting rules.
- The structure of the source code.

The important goal is to maintain consistent and readable code throughout a project.

---

## 📊 Tool Comparison

| Tool | Primary Purpose |
|---|---|
| `flake8` | Check code for style issues and certain errors |
| `black` | Automatically format Python code |
| `autopep8` | Automatically improve PEP 8 compliance |

---

## 🔬 Example Workflow

A practical workflow can look like:

```text
Write Code
    ↓
Run flake8
    ↓
Review Issues
    ↓
Run black / autopep8
    ↓
Review Changes
    ↓
Run flake8 Again
```

This demonstrates how automated tools can become part of a regular development workflow.

---

## 🛡️ Cybersecurity Perspective

Code quality is especially important when developing cybersecurity tools.

Security-related scripts may process:

- Logs.
- Network information.
- System data.
- Security alerts.
- Configuration files.

Readable and maintainable code makes it easier to:

- Review security logic.
- Identify mistakes.
- Collaborate with other developers.
- Maintain automation tools.
- Perform code reviews.

Consistent formatting does not guarantee secure code, but it supports a better development and review process.

---

## 📸 Evidence / Screenshots

Capture meaningful evidence such as:

1. Intentionally poorly formatted code.
2. flake8 output.
3. black formatting result.
4. autopep8 formatting result.
5. Final cleaned-up source code.

Suggested structure:

```text
39-python-style-and-pep8-checks/
├── README.md
├── example.py
└── screenshots/
    ├── initial-code.png
    ├── flake8-output.png
    ├── black-formatting.png
    └── final-code.png
```

---

## ⚠️ Best Practices

- Follow PEP 8 consistently.
- Use automated tools as part of development workflows.
- Review automatic formatting rather than blindly accepting changes.
- Run quality checks before committing code.
- Keep formatting consistent across the repository.
- Remember that style checks are not a replacement for security testing.

---

## 🧠 Self-Check

1. What is PEP 8?
2. Why is code style important?
3. What does flake8 do?
4. What does black do?
5. What does autopep8 do?
6. Why might black and autopep8 produce different formatting?
7. Why should code-quality tools be used before committing code?
8. Does following PEP 8 guarantee secure code?

---

## ✅ Completion Checklist

- [ ] Installed flake8.
- [ ] Created `example.py`.
- [ ] Added intentional style issues.
- [ ] Ran flake8.
- [ ] Reviewed reported issues.
- [ ] Installed black.
- [ ] Formatted the file with black.
- [ ] Installed autopep8.
- [ ] Formatted the file with autopep8.
- [ ] Compared formatting results.
- [ ] Captured useful evidence.
- [ ] Reviewed the cybersecurity relevance.

---

## 🏁 Conclusion

In this lab, you learned the importance of Python style and PEP 8.

You used flake8 to identify code-quality issues and explored black and autopep8 as automated formatting tools.

These practices help maintain readable, consistent, and maintainable Python projects.

---

## 🎉 Section 09 Complete

You have now completed:

- Lab 37 — BFS/DFS Implementation
- Lab 38 — Parameter Passing & Unpacking
- Lab 39 — Python Style & PEP 8 Checks

Only one section remains in the Python repository.

---

## ➡️ Next Section

# 🚀 Section 10 — Final Python Project

**Lab 40 — Final Mini-Project: Building a CLI Data Processor**
