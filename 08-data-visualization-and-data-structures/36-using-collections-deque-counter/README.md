# 🧰 Lab 36 — Using Collections (`deque`, `Counter`)

This lab introduces specialized container data types from Python's built-in `collections` module.

You will work with `deque` for efficient operations at both ends of a sequence and `Counter` for counting occurrences of hashable objects.

---

## 🎯 Objective

By completing this lab, you will:

- Understand the `collections` module.
- Learn how to use `deque`.
- Perform append and pop operations from both ends of a deque.
- Learn how to use `Counter`.
- Count occurrences of items in a collection.
- Retrieve the most common elements.
- Understand the performance and clarity benefits of specialized data structures.

---

## 📚 Prerequisites

- Basic Python programming knowledge.
- Familiarity with lists.
- Familiarity with dictionaries.
- Understanding of basic Python functions and loops.

---

## 🧠 Introduction

Python's `collections` module provides specialized container datatypes that can be useful alternatives to common built-in structures.

Some examples include:

- `deque`
- `Counter`
- `OrderedDict`

This lab focuses on `deque` and `Counter`.

---

# 🔄 Task 1 — Introduction to the `collections` Module

The `collections` module is a built-in Python library providing alternatives and extensions for common data types such as lists, dictionaries, and tuples.

It includes specialized containers designed for particular types of problems.

---

# ↔️ Task 2 — Using `deque`

Import `deque`:

```python
from collections import deque
```

---

## Create a deque

```python
d = deque()
```

A `deque` can efficiently add and remove elements from either end.

---

## Append to the Right

```python
d.append('task1')
d.append('task2')
```

The deque now contains:

```text
task1
task2
```

---

## Pop from the Right

```python
last_task = d.pop()

print("Popped from the right:", last_task)
```

The last element is removed from the right side.

---

## Append to the Left

```python
d.appendleft('task0')
```

The new element is inserted at the left side.

---

## Pop from the Left

```python
first_task = d.popleft()

print("Popped from the left:", first_task)
```

The first element is removed from the left side.

---

## 🔬 Complete `deque` Example

```python
from collections import deque


# Create a deque
d = deque()

# Append to the right
d.append('task1')
d.append('task2')

# Pop from the right
last_task = d.pop()
print("Popped from the right:", last_task)

# Append to the left
d.appendleft('task0')

# Pop from the left
first_task = d.popleft()
print("Popped from the left:", first_task)
```

---

## ⚡ Advantages of `deque`

A major advantage of `deque` is the efficiency of operations at both ends.

Common operations such as:

```python
append()
appendleft()
pop()
popleft()
```

are designed for efficient use at either end.

This makes `deque` appropriate for tasks such as:

- Queues.
- Browser-history style structures.
- Processing tasks from either end.
- Certain concurrent-processing scenarios.

---

# 🔢 Task 3 — Using `Counter`

Import `Counter`:

```python
from collections import Counter
```

---

## Create a Sample List

```python
words = [
    'apple',
    'orange',
    'banana',
    'apple',
    'orange',
    'apple'
]
```

---

## Create a Counter

```python
word_count = Counter(words)

print("Word Count:", word_count)
```

`Counter` automatically counts how many times each item occurs.

---

## ⭐ Retrieve the Most Common Words

Use `most_common()`:

```python
most_common = word_count.most_common(2)

print("Most Common Words:", most_common)
```

The argument `2` requests the two most common elements.

---

## 🔬 Complete `Counter` Example

```python
from collections import Counter


# Sample list of words
words = [
    'apple',
    'orange',
    'banana',
    'apple',
    'orange',
    'apple'
]

# Create a Counter
word_count = Counter(words)

print("Word Count:", word_count)

# Retrieve the two most common words
most_common = word_count.most_common(2)

print("Most Common Words:", most_common)
```

---

## 🧠 Advantages of `Counter`

`Counter` provides a simple and readable way to count occurrences.

Without `Counter`, similar functionality could require manually maintaining a dictionary and incrementing values.

Useful methods include:

```python
most_common()
```

---

## 🔬 `deque` vs Standard List

A standard list is suitable for many situations, but repeatedly inserting or removing elements from the beginning can be inefficient.

`deque` is designed specifically for efficient operations at both ends.

| Structure | Common Use |
|---|---|
| `list` | General-purpose sequence |
| `deque` | Efficient operations at both ends |
| `Counter` | Counting occurrences |

---

## 🛡️ Cybersecurity Perspective

These data structures can be useful in cybersecurity and security automation.

### `deque`

A `deque` can represent queues of:

- Security tasks.
- Events waiting for processing.
- Data-processing jobs.
- Monitoring events.

### `Counter`

A `Counter` can help summarize repeated values.

For example, security data could be analyzed to count:

- Repeated event types.
- Frequently occurring values.
- Repeated log categories.

This can make large collections of information easier to summarize.

---

## 📸 Evidence / Screenshots

Capture:

- Python source code.
- `deque` operations.
- Terminal output showing values popped from each end.
- `Counter` output.
- `most_common()` results.

Suggested structure:

```text
36-using-collections-deque-counter/
├── README.md
└── screenshots/
    ├── collections-code.png
    └── collections-output.png
```

---

## ⚠️ Best Practices

- Choose data structures based on the operations your program performs most often.
- Use `deque` when efficient operations at both ends are required.
- Use `Counter` when counting occurrences is the primary task.
- Prefer specialized structures when they make the code clearer and more appropriate for the problem.

---

## 🧠 Self-Check

1. What is the `collections` module?
2. What is a `deque`?
3. What does `append()` do?
4. What does `appendleft()` do?
5. What does `pop()` do?
6. What does `popleft()` do?
7. What is `Counter` used for?
8. What does `most_common()` return?
9. Why might `deque` be preferred over a list for operations at both ends?
10. How could `Counter` be useful when analyzing security data?

---

## ✅ Completion Checklist

- [ ] Imported `deque`.
- [ ] Created a deque.
- [ ] Appended elements to the right.
- [ ] Popped an element from the right.
- [ ] Appended an element to the left.
- [ ] Popped an element from the left.
- [ ] Imported `Counter`.
- [ ] Counted elements in a list.
- [ ] Used `most_common()`.
- [ ] Captured useful evidence.
- [ ] Reviewed cybersecurity applications.

---

## 🏁 Conclusion

In this lab, you explored specialized data structures from Python's `collections` module.

You used `deque` for efficient operations at both ends of a sequence and `Counter` to count occurrences of elements.

Understanding when to use specialized data structures can improve both code clarity and application performance.

---

## 🎉 Section 08 Complete

You have now completed:

- Lab 35 — Quick Data Visualization with matplotlib
- Lab 36 — Using Collections (`deque`, `Counter`)

---

## ➡️ Next Section

**Section 09 — Algorithms, Functions & Code Quality**

Labs:

- Lab 37 — BFS/DFS Implementation
- Lab 38 — Parameter Passing & Unpacking
- Lab 39 — Python Style & PEP 8 Checks
