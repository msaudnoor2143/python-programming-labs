# Lab 27 — Context Managers (`with` Statement)

> Learn how Python context managers handle resource acquisition and cleanup automatically using the `with` statement.

---

## 🎯 Objective

By completing this lab, you will learn how to:

- Understand context managers
- Understand the purpose of the `with` statement
- Understand resource acquisition and release
- Create a custom context manager
- Implement `__enter__()`
- Implement `__exit__()`
- Automatically clean up resources
- Understand why context managers improve resource-management safety

---

## 📚 Prerequisites

Before starting this lab, you should have:

- Basic Python programming knowledge
- Familiarity with file operations
- Understanding of exception handling
- Basic understanding of object-oriented programming

Recommended previous labs:

- **Lab 12 — File I/O Basics**
- **Lab 13 — Handling Exceptions**
- **Lab 17 — OOP: Defining Classes**

---

# 1. Introduction to Context Managers

Context managers are Python mechanisms designed to manage resources correctly.

They are commonly used for resources such as:

- Files
- Network connections
- Database connections
- Locks
- Other resources requiring cleanup

The `with` statement simplifies resource management by automatically handling setup and cleanup.

Conceptually:

```text
Acquire Resource
       ↓
Run Code
       ↓
Release Resource
```

The cleanup occurs when the context is exited.

---

# 2. Why Context Managers Matter

Consider opening a file manually:

```python
file = open("sample.txt", "w")

file.write("Hello, World!")

file.close()
```

The file must be explicitly closed.

Using a context manager:

```python
with open("sample.txt", "w") as file:
    file.write("Hello, World!")
```

Python automatically handles the resource cleanup after the `with` block finishes.

This makes the code easier to manage and reduces the chance of forgetting cleanup operations.

---

# 3. Task 1 — Understand the Context Manager Lifecycle

A context manager handles two important stages:

### Enter

The resource is acquired or prepared.

### Exit

The resource is released or cleaned up.

Custom context managers implement these operations using:

```python
__enter__()
```

and:

```python
__exit__()
```

---

# 4. Task 2 — Create a Custom Context Manager

Create a class named:

```python
MyContext
```

```python
class MyContext:

    def __enter__(self):
        print("Entering the context and allocating resources.")
        return self

    def __exit__(self, exc_type, exc_value, traceback):
        print("Exiting the context and cleaning up resources.")
```

The `__enter__()` method runs when entering the `with` block.

The `__exit__()` method runs when leaving the block.

---

# 5. Task 3 — Use the Context Manager

Use the class with a `with` statement:

```python
with MyContext() as context:
    print("Running within the context block.")
```

Expected output:

```text
Entering the context and allocating resources.
Running within the context block.
Exiting the context and cleaning up resources.
```

The order demonstrates the context-manager lifecycle.

---

# 6. Understanding `__enter__()`

The `__enter__()` method executes when the `with` statement begins.

Example:

```python
def __enter__(self):
    print("Entering the context and allocating resources.")
    return self
```

It can return a resource or object that becomes available through the variable after `as`.

For example:

```python
with MyContext() as context:
```

The value returned from `__enter__()` is assigned to:

```python
context
```

---

# 7. Understanding `__exit__()`

The `__exit__()` method runs when the context is exited.

Its parameters are:

```python
def __exit__(self, exc_type, exc_value, traceback):
```

These parameters provide information about an exception if one occurred inside the context.

The important concept is that cleanup logic can be placed inside `__exit__()`.

---

# 8. Task 4 — Build a File Manager

The original lab demonstrates how a custom context manager can manage a file.

Create:

```python
class FileManager:

    def __init__(self, filename, mode):
        self.filename = filename
        self.mode = mode

    def __enter__(self):
        self.file = open(self.filename, self.mode)
        return self.file

    def __exit__(self, exc_type, exc_value, traceback):
        self.file.close()
```

Now use it:

```python
with FileManager("sample.txt", "w") as f:
    f.write("Hello, World!")
```

The file is opened when entering the context and closed automatically when leaving it.

---

# 9. Complete Example

```python
class FileManager:

    def __init__(self, filename, mode):
        self.filename = filename
        self.mode = mode

    def __enter__(self):
        self.file = open(self.filename, self.mode)
        return self.file

    def __exit__(self, exc_type, exc_value, traceback):
        self.file.close()


with FileManager("sample.txt", "w") as f:
    f.write("Hello, World!")

print("File operation completed.")
```

The important workflow is:

```text
FileManager created
        ↓
__enter__()
        ↓
File opened
        ↓
File operation
        ↓
__exit__()
        ↓
File closed
```

---

# 10. Resource Auto-Management

One of the major advantages of context managers is automatic resource cleanup.

Resources such as files or locks may need explicit release.

If cleanup is forgotten, resources can remain open or unavailable longer than necessary.

Context managers provide a structured mechanism for handling:

```text
Setup
  ↓
Operation
  ↓
Cleanup
```

This becomes particularly important when exceptions occur.

---

# 11. Context Managers and Exceptions

A context manager's `__exit__()` method is called when the context is exited, including when an exception causes the block to terminate.

For example:

```python
with MyContext() as context:
    print("Running inside context")
    # An exception could occur here
```

The context manager still receives control through:

```python
__exit__()
```

This allows cleanup operations to be performed.

---

# 🧠 Key Concepts

### Context manager

A mechanism for managing resources and their lifecycle.

### `with`

Used to execute a block within a managed context.

```python
with MyContext():
    pass
```

### `__enter__()`

Handles entry/setup.

```python
def __enter__(self):
    ...
```

### `__exit__()`

Handles exit/cleanup.

```python
def __exit__(self, exc_type, exc_value, traceback):
    ...
```

### Resource management

Ensures resources are properly acquired and released.

---

# 🛡️ Security Perspective

Proper resource management is important for reliable and secure software.

Context managers can help manage:

- Files
- Database connections
- Network connections
- Locks
- Temporary resources

For cybersecurity automation, poorly managed resources can lead to reliability problems and unexpected system behavior.

For example, security tools may read large log files, interact with databases, or communicate with network services.

Using structured resource management helps ensure that resources are released correctly.

---

# 📸 Evidence / Screenshots

Useful evidence includes:

- Custom context manager implementation
- `__enter__()` output
- Code running inside the context
- `__exit__()` cleanup output
- File creation and successful write operation

Suggested structure:

```text
27-context-managers-with-statement/
├── README.md
├── context_manager.py
├── sample.txt
└── screenshots/
    └── context-manager-output.png
```

---

# ⚠️ Best Practices

- Prefer `with` when working with resources that require cleanup.
- Keep cleanup logic reliable.
- Make the lifecycle of resources clear.
- Avoid leaving files, connections, or locks open unnecessarily.
- Handle exceptions carefully.
- Test cleanup behavior when errors occur.

---

# 📝 Self-Check

1. What is a context manager?
2. What does the `with` statement provide?
3. What is the purpose of `__enter__()`?
4. What is the purpose of `__exit__()`?
5. Why is automatic cleanup useful?
6. What resources can context managers manage?
7. What happens to `__exit__()` when an exception occurs inside the context?
8. How can context managers improve software reliability?
9. Why is proper resource management relevant to cybersecurity?

---

# ✅ Lab Completion Checklist

- [ ] I understand context managers.
- [ ] I understand the `with` statement.
- [ ] I created a custom context manager.
- [ ] I implemented `__enter__()`.
- [ ] I implemented `__exit__()`.
- [ ] I used a context manager with `with`.
- [ ] I created a custom file manager.
- [ ] I understand automatic resource cleanup.
- [ ] I understand the role of cleanup during exceptions.
- [ ] I completed the practical exercises.
- [ ] I captured useful execution evidence.

---

# 📌 Conclusion

In this lab, you learned how Python context managers simplify resource management.

You created a custom context manager using:

```python
__enter__()
```

and:

```python
__exit__()
```

You then used the `with` statement to manage resources automatically.

Context managers provide a clean and reliable approach to resource acquisition and cleanup, making them especially useful for files, connections, locks, and other resources that require proper lifecycle management.

---

## 🎉 Section 05 Complete

You have now completed:

- **Lab 25 — Intro to Unit Testing with `unittest`**
- **Lab 26 — Decorators: Basic Usage**
- **Lab 27 — Context Managers (`with` statement)**

### 🚀 Next Section

**Section 06 — Concurrency & Databases**

- Lab 28 — Multithreading Basics
- Lab 29 — Multiprocessing Basics
- Lab 30 — Basic SQLite Usage
