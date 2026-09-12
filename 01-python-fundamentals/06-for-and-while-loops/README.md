# 🔁 Lab 06 — For & While Loops

## 🎯 Objective

Understand and implement `for` and `while` loops in Python and identify appropriate situations for each type of loop.

---

## 📚 Prerequisites

- Basic Python syntax
- Understanding of variables
- Python 3 installed

---

## 📁 Lab Structure

```text
06-for-and-while-loops/
├── README.md
├── for_loop_example.py
├── while_loop_example.py
└── screenshots/
```

---

# 🧠 Introduction to Loops

Loops allow a program to execute a block of code repeatedly.

Two fundamental Python loops are:

- `for`
- `while`

### Iteration

Iteration means repeatedly executing a set of statements.

### Loop Condition

A loop condition determines whether the loop continues executing.

---

# 🧪 Task 1 — Use a `for` Loop

Create:

```text
for_loop_example.py
```

Use a `for` loop to print numbers from 1 to 5.

```python
for i in range(1, 6):
    print(i)
```

### Explanation

```python
range(1, 6)
```

generates values from `1` through `5`.

The loop processes each value sequentially.

Run the script and observe the output.

---

# 🧪 Task 2 — Use a `while` Loop

Create:

```text
while_loop_example.py
```

Use a `while` loop to calculate a running total until it exceeds 20.

```python
total = 0
i = 1

while total <= 20:
    total += i
    i += 1

print("Final total:", total)
```

### Explanation

`total` stores the cumulative sum.

`i` is increased during every iteration.

The loop continues while:

```python
total <= 20
```

is true.

---

# 🔀 Task 3 — Compare `for` and `while`

## `for` Loop

A `for` loop is useful when:

- The number of iterations is known
- Processing a sequence
- Iterating over a collection
- Working with a fixed range

Example:

```python
for item in items:
    print(item)
```

## `while` Loop

A `while` loop is useful when:

- Execution depends on a condition
- The number of iterations is not predetermined
- Processing continues until a condition changes

Example:

```python
while condition:
    # code
```

---

# 🔎 Loop Reference

| Loop | Common Use |
|---|---|
| `for` | Iterating over sequences |
| `while` | Condition-controlled repetition |
| `range()` | Generating a sequence of numbers |

---

# 🛡️ Security Perspective

Loops are widely used in cybersecurity and automation.

Examples include:

- Processing security logs
- Checking multiple systems
- Processing lists of events
- Monitoring conditions
- Repeating administrative tasks
- Automating analysis

However, loops must have appropriate termination conditions. An incorrectly designed `while` loop can continue indefinitely.

---

# 🧪 Practical Exercise

Modify the `for` loop to print numbers from:

```text
1 to 10
```

Then modify the `while` loop so that it uses a different stopping condition.

Observe how changing the condition affects program execution.

---

# 📝 Self-Check Questions

1. What is a loop?
2. What is iteration?
3. When is a `for` loop appropriate?
4. When is a `while` loop appropriate?
5. What does `range(1, 6)` produce?
6. What controls the execution of a `while` loop?
7. Why should a `while` loop have a suitable termination condition?

---

# ✅ Lab Completion Checklist

- [ ] I understand iteration.
- [ ] I can write a `for` loop.
- [ ] I can write a `while` loop.
- [ ] I understand `range()`.
- [ ] I can control loop execution.
- [ ] I understand the difference between `for` and `while`.
- [ ] I completed both practical examples.

---

## 📸 Evidence

Recommended screenshots:

- `for_loop_example.py` execution
- `while_loop_example.py` execution
- Terminal output showing the results

Store evidence in:

```text
screenshots/
```

---

## 📌 Summary

This lab introduced repetitive execution using `for` and `while` loops. Understanding when to use each loop is essential for writing efficient Python programs and automation scripts.

## 🚀 Next Lab

**Lab 07 — Lists & List Methods**
