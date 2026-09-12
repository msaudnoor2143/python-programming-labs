# 📁 Lab 12 — File I/O Basics

## 🎯 Objective

Learn the fundamentals of File I/O in Python and understand how programs can read from and write to files.

By completing this lab, you will learn how to:

- Write data to a file.
- Read data from a file.
- Use Python's built-in `open()` function.
- Understand basic file modes.
- Use context managers with files.
- Understand why proper resource management is important.

---

## 📚 Prerequisites

Before starting this lab, you should have:

- Basic Python programming knowledge.
- Understanding of Python syntax.
- Python installed.
- A text editor or IDE.

---

## 🧠 Key Concepts

### File I/O

File Input/Output allows a Python program to interact with files stored on the filesystem.

Common file modes include:

| Mode | Purpose |
|---|---|
| `r` | Read |
| `w` | Write |
| `a` | Append |

---

### Context Manager

Python's `with` statement can be used to manage files.

Example:

```python
with open("example.txt", "r") as f:
    data = f.read()
```

The context manager ensures that the file is properly handled after the block finishes.

---

# 🧪 Practical Lab

## Task 1 — Write to a File

Create:

```text
write_file.py
```

Use a context manager to create `output.txt` and write multiple lines:

```python
with open("output.txt", "w") as f:
    f.write("Hello, World!\n")
    f.write("This is a file I/O example.\n")
    f.write("Python makes File I/O easy!\n")
```

Run the script:

```bash
python write_file.py
```

Verify that:

```text
output.txt
```

was created.

---

## Task 2 — Read from a File

Create:

```text
read_file.py
```

Use the following approach:

```python
with open("output.txt", "r") as f:
    for line in f:
        print(line.strip())
```

Run:

```bash
python read_file.py
```

Expected output:

```text
Hello, World!
This is a file I/O example.
Python makes File I/O easy!
```

---

## Task 3 — Understand Context Managers

Explain how the following structure works:

```python
with open("output.txt", "r") as f:
    ...
```

The `with` statement manages the file resource and ensures that the file is properly closed after the operation.

This helps improve reliability and reduces the chance of leaving resources open unnecessarily.

---

## 🔎 What You Practiced

This lab demonstrated:

- Creating files.
- Writing data.
- Reading data.
- Iterating through file contents.
- Using `open()`.
- Using file modes.
- Using context managers.

---

## 🛡️ Cybersecurity Perspective

File handling is extremely common in cybersecurity.

Security scripts frequently process:

- System logs.
- Authentication records.
- Configuration files.
- Security reports.
- IOC lists.
- Exported monitoring data.

For example, a Python security tool may read a log file and process each line to identify potentially important events.

---

## 📸 Evidence

Useful evidence includes:

- Successful execution of `write_file.py`.
- The generated `output.txt`.
- Successful execution of `read_file.py`.
- Correct file contents.

---

## ⚠️ Best Practice

Be careful when using:

```python
open("file.txt", "w")
```

Write mode can replace existing file contents.

Use the appropriate mode for the operation you intend to perform.

---

## 📝 Self-Check

- [ ] Can I write text to a file?
- [ ] Can I read a file line by line?
- [ ] Do I understand `r`, `w`, and `a`?
- [ ] Can I explain why `with` is useful?
- [ ] Can I identify why resource management matters?

---

## ✅ Completion Checklist

- [ ] `write_file.py` created
- [ ] `output.txt` generated
- [ ] Multiple lines written
- [ ] `read_file.py` created
- [ ] File contents successfully read
- [ ] Context manager understood
- [ ] Output verified
- [ ] Evidence added where useful

---

## 🏁 Conclusion

This lab introduced the fundamentals of File I/O in Python.

The ability to safely read and write files is essential for Python development, automation, system administration, and cybersecurity data processing.

---

## 🚀 Next Lab

**Lab 13 — Handling Exceptions**
