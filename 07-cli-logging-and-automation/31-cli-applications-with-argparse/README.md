# 🖥️ Lab 31 — CLI Applications with `argparse`

This lab introduces the creation of command-line applications in Python using the built-in `argparse` module.

---

## 🎯 Objective

By completing this lab, you will:

- Understand the basics of Python CLI applications.
- Learn how to parse command-line arguments.
- Use the `argparse` module.
- Create a user-friendly command-line application.
- Use automatic help-text generation.

---

## 📚 Prerequisites

- Basic Python programming knowledge.
- Python installed on your machine.
- Basic command-line interface knowledge.
- Familiarity with running Python scripts.

---

## 🧠 Introduction

The `argparse` module makes it easier to build user-friendly command-line interfaces.

A program can define the arguments it expects, and `argparse` handles parsing those arguments from `sys.argv`.

It can also automatically generate usage and help messages.

---

## 🧪 Lab Tasks

### Task 1 — Introduction to `argparse`

The module provides tools for defining and parsing command-line arguments.

```python
import argparse
```

---

### Task 2 — Verify the Python Environment

Check that Python is available.

```bash
python --version
```

---

### Task 3 — Create the Python Script

Create a Python file named:

```text
greet.py
```

This script will accept a name from the command line and produce a greeting.

---

### Task 4 — Import `argparse`

```python
import argparse
```

---

### Task 5 — Define and Parse Arguments

Create an argument parser and define a `--name` argument.

```python
import argparse


# Create the parser
parser = argparse.ArgumentParser(
    description='A simple greeting application.'
)

# Add an argument
parser.add_argument(
    '--name',
    type=str,
    help='The name of the person to greet.'
)

# Parse the argument
args = parser.parse_args()
```

---

### Task 6 — Use the Parsed Argument

Use the supplied name when it is available.

```python
if args.name:
    print(f'Hello, {args.name}!')
else:
    print('Hello, Stranger!')
```

---

## 🔬 Complete Example

```python
import argparse


# Create the parser
parser = argparse.ArgumentParser(
    description='A simple greeting application.'
)

# Add an argument
parser.add_argument(
    '--name',
    type=str,
    help='The name of the person to greet.'
)

# Parse the argument
args = parser.parse_args()

# Use the parsed argument
if args.name:
    print(f'Hello, {args.name}!')
else:
    print('Hello, Stranger!')
```

---

## ▶️ Task 7 — Run the Script

Run the application with a name:

```bash
python greet.py --name Alice
```

Expected output:

```text
Hello, Alice!
```

Run the application without a name:

```bash
python greet.py
```

Expected output:

```text
Hello, Stranger!
```

---

## ❓ Task 8 — Automatic Help Text

`argparse` automatically generates help information.

Run:

```bash
python greet.py --help
```

The output will describe the program and its available arguments.

Example:

```text
usage: greet.py [-h] [--name NAME]

A simple greeting application.

optional arguments:
  -h, --help   show this help message and exit
  --name NAME  The name of the person to greet.
```

The exact formatting can vary between Python versions.

---

## 🛡️ Cybersecurity Perspective

Command-line applications are widely used in cybersecurity.

Examples include:

- Log-analysis tools.
- Security automation scripts.
- System administration utilities.
- Incident-response utilities.
- Data-processing tools.

Using `argparse` allows a Python security tool to accept structured input directly from the command line.

---

## 📸 Evidence / Screenshots

Capture:

- `greet.py` source code.
- Running the script with `--name`.
- Running the script without the argument.
- `--help` output.

Suggested structure:

```text
31-cli-applications-with-argparse/
├── README.md
└── screenshots/
    ├── greet-code.png
    ├── greet-output.png
    └── argparse-help.png
```

---

## 🧠 Self-Check

1. What is `argparse`?
2. What does `ArgumentParser()` create?
3. What does `add_argument()` do?
4. What does `parse_args()` do?
5. What is the purpose of `--name`?
6. How can you display automatic help information?

---

## ✅ Completion Checklist

- [ ] Imported `argparse`.
- [ ] Created an argument parser.
- [ ] Added the `--name` argument.
- [ ] Parsed command-line arguments.
- [ ] Ran the script with an argument.
- [ ] Ran the script without an argument.
- [ ] Tested `--help`.
- [ ] Captured useful evidence.

---

## 🏁 Conclusion

In this lab, you created a basic command-line application using Python's `argparse` module.

You learned how to define arguments, parse user input, generate output, and use automatic help text.

---

## ➡️ Next Lab

**Lab 32 — Logging with Python's Logging Module**
