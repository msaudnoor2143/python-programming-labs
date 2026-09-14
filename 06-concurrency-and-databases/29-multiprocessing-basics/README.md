# ⚙️ Lab 29 — Multiprocessing Basics

This lab introduces Python multiprocessing and demonstrates how separate processes can execute CPU-bound tasks concurrently.

---

## 🎯 Objective

By completing this lab, you will:

- Understand the basics of multiprocessing in Python.
- Learn how to create and manage multiple processes.
- Understand how processes differ from threads.
- Understand the separate-memory model used by processes.
- Explore multiprocessing for CPU-bound workloads.

---

## 📚 Prerequisites

- Basic Python programming knowledge.
- Familiarity with the concept of threading.
- Python installed on your system.
- Ability to run Python scripts.

---

## 🧠 Introduction

Multiprocessing allows Python programs to create multiple processes that can execute tasks independently.

Unlike threads, processes have separate memory spaces.

This isolation can help prevent direct data interference between processes and makes multiprocessing useful for CPU-bound workloads.

---

## 🧪 Lab Tasks

### Task 1 — Import the Multiprocessing Module

```python
import multiprocessing
```

The `multiprocessing` module provides an interface for creating and managing processes.

---

### Task 2 — Define a CPU-Bound Function

Create a function that performs an operation on a large list.

```python
def sum_large_list(num_list):
    total = sum(num_list)
    print(f"Sum of the list is: {total}")
```

This function calculates the sum of the supplied list.

---

### Task 3 — Create the Input Data

Create a large list of numbers.

```python
numbers = list(range(1000000))
```

The large dataset provides a simple CPU-bound workload for the demonstration.

---

### Task 4 — Create and Start Multiple Processes

Create two processes using `multiprocessing.Process`.

```python
if __name__ == '__main__':
    process1 = multiprocessing.Process(
        target=sum_large_list,
        args=(numbers,)
    )

    process2 = multiprocessing.Process(
        target=sum_large_list,
        args=(numbers,)
    )

    process1.start()
    process2.start()

    process1.join()
    process2.join()
```

### Key Concepts

`Process()` creates a process.

`start()` begins process execution.

`join()` waits for the process to finish.

---

## 🔬 Complete Example

```python
import multiprocessing


def sum_large_list(num_list):
    total = sum(num_list)
    print(f"Sum of the list is: {total}")


numbers = list(range(1000000))


if __name__ == '__main__':
    process1 = multiprocessing.Process(
        target=sum_large_list,
        args=(numbers,)
    )

    process2 = multiprocessing.Process(
        target=sum_large_list,
        args=(numbers,)
    )

    process1.start()
    process2.start()

    process1.join()
    process2.join()
```

---

## 🔎 Task 5 — Observe Parallel Execution

Run the program and observe the terminal output.

Each process executes the `sum_large_list()` function.

The two processes can run independently, allowing the system to schedule their execution concurrently.

---

## 🧵 Task 6 — Compare Multiprocessing with Threading

### Threading

Threads share the same memory space.

Advantages include easier sharing of data between threads.

However, shared memory can create concurrency problems if resources are not synchronized correctly.

### Multiprocessing

Processes have separate memory spaces.

This provides greater isolation between processes, but sharing data between processes can be more complicated.

| Feature | Threading | Multiprocessing |
|---|---|---|
| Execution unit | Thread | Process |
| Memory | Shared | Separate |
| Data sharing | Easier | More complex |
| Isolation | Lower | Higher |
| Useful for | Concurrent tasks | CPU-bound workloads |

---

## 🖼️ Practical Example — Image Processing

Consider a security or automation system that needs to process multiple images using a CPU-intensive operation such as applying a filter.

Multiple processes could handle different image-processing tasks concurrently.

This can potentially reduce overall processing time when the workload is suitable for parallel execution.

---

## 🛡️ Cybersecurity Perspective

Multiprocessing can be useful in defensive cybersecurity applications such as:

- Processing large security datasets.
- Performing independent analysis tasks.
- Processing batches of security events.
- Running CPU-intensive analysis.
- Building security automation pipelines.

Process isolation can also help separate independent workloads.

---

## 📸 Evidence / Screenshots

Useful evidence includes:

- Multiprocessing source code.
- Terminal output from both processes.
- Demonstration of process execution.
- Comparison notes between threads and processes.

Suggested structure:

```text
29-multiprocessing-basics/
├── README.md
└── screenshots/
    ├── multiprocessing-code.png
    └── multiprocessing-output.png
```

---

## ⚠️ Best Practices

- Use `if __name__ == '__main__':` when creating processes.
- Use `join()` when the parent program needs to wait for child processes.
- Understand the memory model before sharing data.
- Use multiprocessing when the workload benefits from multiple processes.
- Avoid creating unnecessary processes for very small tasks.

---

## 🧠 Self-Check

1. What is multiprocessing?
2. What module provides multiprocessing in Python?
3. What does `Process()` do?
4. What does `start()` do?
5. What does `join()` do?
6. How does process memory differ from thread memory?
7. Why can multiprocessing be useful for CPU-bound workloads?

---

## ✅ Completion Checklist

- [ ] Imported `multiprocessing`.
- [ ] Created a CPU-bound function.
- [ ] Created a large dataset.
- [ ] Created multiple processes.
- [ ] Started the processes.
- [ ] Used `join()`.
- [ ] Observed process output.
- [ ] Compared processes and threads.
- [ ] Captured useful evidence.

---

## 🏁 Conclusion

In this lab, you learned how Python multiprocessing can execute tasks using multiple independent processes.

You also compared multiprocessing with threading, particularly in terms of memory sharing and process independence.

The next lab introduces SQLite database programming in Python.

---

## ➡️ Next Lab

**Lab 30 — Basic SQLite Usage**
