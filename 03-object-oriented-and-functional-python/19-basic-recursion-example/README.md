# 🔁 Lab 19 — Basic Recursion Example

## 🎯 Objective

Understand the fundamentals of recursion and learn how a function can call itself to solve a problem.

By completing this lab, you will learn how to:

- Understand recursive functions.
- Identify a base case.
- Identify a recursive case.
- Trace recursive execution.
- Implement a simple recursive function.
- Understand why a stopping condition is necessary.

---

## 📚 Prerequisites

Before starting this lab, you should understand:

- Python functions.
- Function parameters.
- Return values.
- Conditional statements.

---

## 🧠 Key Concepts

### Recursion

Recursion occurs when a function calls itself as part of solving a problem.

A recursive function normally contains two important components:

```text
Base Case
    +
Recursive Case
```

---

### Base Case

The base case provides the condition that stops further recursive calls.

Without an appropriate base case, recursion may continue indefinitely until Python reaches its recursion limit.

---

### Recursive Case

The recursive case calls the same function with a modified input.

---

# 🧪 Practical Lab

## Task 1 — Create a Recursive Countdown

Create:

```text
recursion_example.py
```

Implement:

```python
def countdown(n):
    if n <= 0:
        print("Done!")
        return

    print(n)
    countdown(n - 1)
```

Call the function:

```python
countdown(5)
```

Expected output:

```text
5
4
3
2
1
Done!
```

---

## Task 2 — Understand the Base Case

The following condition is the base case:

```python
if n <= 0:
    print("Done!")
    return
```

Once `n` reaches `0`, the function stops making recursive calls.

---

## Task 3 — Understand the Recursive Case

This line creates the recursive call:

```python
countdown(n - 1)
```

Each call decreases `n` by one.

The execution can be visualized as:

```text
countdown(5)
    ↓
countdown(4)
    ↓
countdown(3)
    ↓
countdown(2)
    ↓
countdown(1)
    ↓
countdown(0)
    ↓
Done!
```

---

## Task 4 — Recursive Factorial

Create a recursive factorial function:

```python
def factorial(n):
    if n <= 1:
        return 1

    return n * factorial(n - 1)
```

Test it:

```python
print("Factorial:", factorial(5))
```

Expected output:

```text
Factorial: 120
```

---

## 🔎 What You Practiced

This lab demonstrated:

- Recursive functions.
- Base cases.
- Recursive cases.
- Recursive execution.
- Function calls.
- Return values.
- Factorial calculation.

---

## 🧠 Recursion vs Iteration

Many recursive problems can also be solved using loops.

For example:

```text
Recursion
    Function calls itself

Iteration
    Loop repeats instructions
```

The best approach depends on the problem and the desired implementation.

---

## 🛡️ Cybersecurity Perspective

Recursion is useful when working with hierarchical or graph-like structures.

Potential applications include:

- Traversing directories.
- Processing nested data.
- Exploring tree structures.
- Traversing relationships.
- Processing nested configuration data.

Understanding recursion also provides a foundation for more advanced algorithms.

---

## 📸 Evidence

Recommended evidence:

- Countdown execution.
- Recursive call output.
- Factorial result.
- Debugging or tracing recursion when useful.

---

## ⚠️ Important Consideration

Recursive functions require a reliable stopping condition.

Always ensure that the recursive input moves toward the base case.

---

## 📝 Self-Check

- [ ] Can I explain recursion?
- [ ] Can I identify a base case?
- [ ] Can I identify a recursive case?
- [ ] Can I trace recursive execution?
- [ ] Can I implement a simple recursive function?
- [ ] Can I explain why a base case is necessary?

---

## ✅ Completion Checklist

- [ ] Recursive countdown created
- [ ] Base case implemented
- [ ] Recursive case implemented
- [ ] Countdown tested
- [ ] Factorial function implemented
- [ ] Factorial tested
- [ ] Recursive flow understood
- [ ] Evidence added where useful

---

## 🏁 Conclusion

This lab introduced recursion and demonstrated how a function can repeatedly call itself while moving toward a defined base case.

Recursion is an important programming concept and provides a foundation for understanding more advanced algorithms and data structures.

---

## 🚀 Next Lab

**Lab 20 — Using Lambda & Higher-Order Functions**
