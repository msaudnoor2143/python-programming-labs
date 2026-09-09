# 🐍 Lab 01 — Installing Python & Environment Setup

This lab focuses on verifying the Python 3 environment and preparing the tools required for Python development.

## 🎯 Objective

By completing this lab, you will:

- Verify that Python 3 is installed
- Identify the installed Python executable
- Verify the development environment
- Confirm that Git is available for project version control
- Create and execute a basic Python verification program

## 📚 Prerequisites

- Linux system
- Terminal access
- Python 3
- Git
- A code editor such as Visual Studio Code

## 🔍 Environment Verification

Check the installed Python version:

```bash
python3 --version
```

Identify the Python executable:

```bash
which python3
```

Check the installed Git version:

```bash
git --version
```

If Visual Studio Code is installed, verify it with:

```bash
code --version
```

## 🧪 Practical Lab

A small Python program was created to verify the Python runtime and executable path.

The program displays:

- Python version
- Python executable path
- Environment readiness

### Program

```python
import sys

print("Python Environment Verification")
print("===============================")
print(f"Python version : {sys.version.split()[0]}")
print(f"Python path    : {sys.executable}")
print("Environment    : Ready")
```

### Execute the Program

```bash
python3 python_info.py
```

## 📸 Evidence

The `screenshots/` directory is reserved for meaningful evidence from the lab.

Recommended evidence includes:

- Python version verification
- Successful execution of the verification program

## 🔎 Command Reference

| Command | Purpose |
|---|---|
| `python3 --version` | Displays the installed Python version |
| `which python3` | Shows the Python executable path |
| `git --version` | Displays the installed Git version |
| `code --version` | Displays the installed VS Code version |
| `python3 python_info.py` | Executes the Python verification program |

## 🧠 Key Concepts

### Python Interpreter

The Python interpreter executes Python source code and converts it into actions performed by the system.

### Python Version

Knowing the installed Python version is important because different Python versions can have different features and compatibility requirements.

### Executable Path

The `which` command identifies the executable that will be used when the corresponding command is entered in the shell.

### Development Environment

A reliable development environment consists of the required interpreter, editor, version-control tools, and supporting configuration.

## 🛡️ Security Perspective

Python is widely used for automation, system administration, data processing, and cybersecurity tooling.

A correctly configured development environment provides a reliable foundation for building and testing Python applications.

## ⚠️ Best Practices

- Verify the Python version before starting a project.
- Keep project dependencies isolated when required.
- Use version control for project files.
- Avoid running unfamiliar Python programs without understanding their purpose.
- Keep development tools maintained.

## 📝 Questions

1. What does `python3 --version` display?
2. What is the purpose of `which python3`?
3. What is the role of the Python interpreter?
4. Why is version information important when developing Python applications?
5. Why is Git useful for Python projects?

## ✅ Lab Completion Checklist

- [x] Python 3 verified
- [x] Python executable path verified
- [x] Git verified
- [x] VS Code verified
- [x] Python verification program created
- [x] Verification program executed successfully
- [ ] Evidence screenshots added

## 📌 Summary

Lab 01 established and verified the Python development environment required for the remaining Python labs.

## 🚀 Next Lab

**Lab 02 — Hello World & Basic Syntax**
