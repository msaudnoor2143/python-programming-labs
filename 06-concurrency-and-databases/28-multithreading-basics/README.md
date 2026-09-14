# 🧵 Lab 28 — Multithreading Basics

This lab introduces Python multithreading, including thread creation, thread management, shared memory, and potential concurrency issues.

---

## 🎯 Objective

By completing this lab, you will:

- Understand the fundamentals of multithreading in Python.
- Learn how to create and manage threads.
- Understand the shared-memory model used by threads.
- Recognize potential concurrency issues.
- Understand why synchronization can be important when multiple threads access shared resources.

---

## 📚 Prerequisites

- Basic knowledge of Python programming.
- Python installed on your machine.
- A code editor or IDE such as Visual Studio Code or PyCharm.
- Familiarity with running Python scripts.

---

## 🧠 Introduction

Multithreading allows a Python program to create multiple threads that can execute tasks concurrently.

Threads operate within the same process and share the process's memory space.

This makes communication between threads convenient, but shared resources can also introduce concurrency problems such as race conditions.

---

## 🧪 Lab Tasks

### Task 1 — Import the Threading Module

Python provides the `threading` module for working with threads.

```python
import threading
```

---

### Task 2 — Define a Function to Be Executed by Threads

Create a function that prints a range of numbers.

```python
def print_numbers(thread_name, start, end):
    """Prints numbers from start to end."""
    for number in range(start, end):
        print(f"{thread_name}: {number}")
```

The function accepts:

- `thread_name` — identifies the thread.
- `start` — starting value.
- `end` — ending boundary.

---

### Task 3 — Create Threads

Use `threading.Thread` to create two threads.

```python
# Create threads
thread1 = threading.Thread(
    target=print_numbers,
    args=("Thread-1", 0, 5)
)

thread2 = threading.Thread(
    target=print_numbers,
    args=("Thread-2", 5, 10)
)
```

Each thread is associated with the `print_numbers()` function and receives its own arguments.

### Key Concept

Threads are lightweight execution units that allow tasks to run concurrently.

---

### Task 4 — Start and Join Threads

Start both threads and then wait for them to finish.

```python
# Start threads
thread1.start()
thread2.start()

# Join threads
thread1.join()
thread2.join()
```

### Key Concepts

`start()` begins thread execution.

`join()` causes the main program to wait until the specified thread finishes.

---

## 🔬 Complete Example

```python
import threading


def print_numbers(thread_name, start, end):
    """Prints numbers from start to end."""
    for number in range(start, end):
        print(f"{thread_name}: {number}")


# Create threads
thread1 = threading.Thread(
    target=print_numbers,
    args=("Thread-1", 0, 5)
)

thread2 = threading.Thread(
    target=print_numbers,
    args=("Thread-2", 5, 10)
)

# Start threads
thread1.start()
thread2.start()

# Wait for threads to finish
thread1.join()
thread2.join()
```

The exact order of printed lines may vary because the threads execute concurrently.

---

## 🧠 Task 5 — Understand Shared Memory and Concurrency Issues

Threads operate within the same memory space.

This means threads can access shared variables and data structures.

### Shared Memory

Multiple threads can access the same resources.

This can make communication easier, but it can also cause inconsistent results when several threads modify the same resource.

### Concurrency Issues

Without proper synchronization, threads may interfere with each other.

One important example is a **race condition**, where the result depends on the timing or order of concurrent operations.

---

## 🏦 Example Case Study — Shared Account Balance

Consider a banking application where two threads simultaneously attempt to update the balance of an account.

If both threads read and modify the same balance without proper synchronization, the final result may not correctly represent both operations.

This demonstrates why shared resources must be carefully managed in concurrent applications.

---

## 🛡️ Cybersecurity Perspective

Multithreading is useful in security automation and defensive tooling.

Possible applications include:

- Processing multiple security events concurrently.
- Handling multiple log-processing tasks.
- Performing independent network-related operations.
- Building responsive security utilities.
- Processing security monitoring data.

However, shared resources must be handled carefully because concurrency bugs can affect the correctness and reliability of security tools.

---

## 📸 Evidence / Screenshots

Capture meaningful evidence such as:

- Python script in the editor.
- Terminal showing both threads executing.
- Output showing `Thread-1` and `Thread-2`.
- Any experiment demonstrating concurrent execution.

Suggested structure:

```text
28-multithreading-basics/
├── README.md
└── screenshots/
    ├── thread-code.png
    └── thread-output.png
```

---

## ⚠️ Best Practices

- Understand which resources are shared between threads.
- Use synchronization when shared resources require protection.
- Keep threaded tasks clearly separated.
- Use `join()` when the main program must wait for worker threads.
- Test concurrent code carefully because timing-related bugs can be difficult to reproduce.

---

## 🧠 Self-Check

1. What is a thread?
2. How do you create a thread in Python?
3. What does `start()` do?
4. What does `join()` do?
5. Why do threads have access to shared memory?
6. What is a race condition?
7. Why can concurrency issues be difficult to reproduce?

---

## ✅ Completion Checklist

- [ ] Imported the `threading` module.
- [ ] Created a function for thread execution.
- [ ] Created multiple threads.
- [ ] Started the threads.
- [ ] Used `join()`.
- [ ] Observed thread output.
- [ ] Understand shared memory.
- [ ] Understand race conditions.
- [ ] Captured useful evidence.

---

## 🏁 Conclusion

In this lab, you explored the fundamentals of Python multithreading.

You created and managed multiple threads, learned how `start()` and `join()` work, and examined shared memory and concurrency issues.

The next lab introduces multiprocessing and explains how processes differ from threads.

---

## ➡️ Next Lab

**Lab 29 — Multiprocessing Basics**
