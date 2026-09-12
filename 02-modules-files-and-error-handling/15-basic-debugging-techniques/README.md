# 🐞 Lab 15 — Basic Debugging Techniques

## 🎯 Objective

Learn practical techniques for identifying and understanding problems in Python programs.

By completing this lab, you will learn how to:

- Use print statements for debugging.
- Inspect intermediate values.
- Understand the Python Debugger (`pdb`).
- Set a breakpoint.
- Step through program execution.
- Inspect variables.
- Continue or stop execution.

---

## 📚 Prerequisites

Before starting this lab, you should understand:

- Basic Python programming.
- Functions.
- Loops.
- Conditionals.
- Python execution.

---

## 🧠 Key Concepts

### Debugging

Debugging is the process of identifying and understanding problems in a program and determining how the program behaves during execution.

---

### Print Debugging

A simple technique is to print variables and intermediate results.

Example:

```python
print("Debug:", variable)
```

This can help reveal unexpected values or execution states.

---

### Python Debugger — `pdb`

Python includes a built-in debugger called `pdb`.

A breakpoint can be inserted with:

```python
import pdb
pdb.set_trace()
```

When execution reaches the breakpoint, the debugger allows you to inspect and control execution.

---

# 🧪 Practical Lab

## Task 1 — Debug Using Print Statements

Create a function:

```python
def calculate_sum(numbers):
    total = 0

    for num in numbers:
        total += num
        print("Debug: Adding", num, "Total so far:", total)

    return total
```

Test it:

```python
numbers = [5, 10, 15]

print("Final Sum:", calculate_sum(numbers))
```

Expected final result:

```text
Final Sum: 30
```

The debug output allows you to observe how `total` changes during execution.

---

## Task 2 — Introduce `pdb`

Create a simple function:

```python
def divide_numbers(a, b):
    import pdb
    pdb.set_trace()

    result = a / b
    print("Result:", result)

    return result
```

Call the function:

```python
divide_numbers(10, 0)
```

The intentional error allows you to inspect the program while it is paused at the debugger breakpoint.

---

## Task 3 — Step Through Execution

When the debugger pauses, practice these commands:

| Command | Purpose |
|---|---|
| `n` | Execute the next line |
| `s` | Step into a function |
| `c` | Continue execution |
| `q` | Quit the debugger |
| `print(a, b)` | Inspect variable values |

For example:

```text
(Pdb) print(a, b)
```

This allows you to inspect the current values.

---

## 🔎 Debugging Workflow

A practical debugging process can be summarized as:

```text
Observe Problem
      │
      ▼
Reproduce Problem
      │
      ▼
Inspect Program State
      │
      ▼
Identify Cause
      │
      ▼
Apply Fix
      │
      ▼
Test Again
```

---

## 🧠 What You Practiced

This lab demonstrated:

- Print-based debugging.
- Intermediate value inspection.
- `pdb`.
- Breakpoints.
- Stepping through execution.
- Variable inspection.
- Continuing execution.
- Quitting the debugger.

---

## 🛡️ Cybersecurity Perspective

Debugging is especially important when developing cybersecurity automation.

Security scripts may process:

- Logs.
- Network data.
- API responses.
- Configuration files.
- Security events.
- Large datasets.

When a security tool produces unexpected results, debugging helps determine whether the problem is caused by the input, program logic, or execution flow.

---

## 📸 Evidence

Recommended evidence:

- Print-debugging output.
- `pdb` breakpoint.
- Variable inspection inside `pdb`.
- Stepping through execution.

Debugger screenshots are particularly useful because they demonstrate actual troubleshooting skills.

---

## ⚠️ Best Practice

Print statements are useful for simple debugging, but more structured debugging techniques become increasingly valuable as programs become larger.

Avoid leaving unnecessary debugging output in production code.

---

## 📝 Self-Check

- [ ] Can I use print statements to inspect variables?
- [ ] Can I set a `pdb` breakpoint?
- [ ] Can I inspect variables inside `pdb`?
- [ ] Do I understand `n`?
- [ ] Do I understand `s`?
- [ ] Do I understand `c`?
- [ ] Do I understand `q`?

---

## ✅ Completion Checklist

- [ ] Print-debugging example created
- [ ] Intermediate values inspected
- [ ] `pdb` imported
- [ ] Breakpoint created
- [ ] Debugger commands practiced
- [ ] Variables inspected
- [ ] Program behavior understood
- [ ] Evidence added where useful

---

## 🏁 Conclusion

This lab introduced practical Python debugging techniques using print statements and the built-in `pdb` debugger.

Developing strong debugging skills improves problem-solving efficiency and helps build more reliable Python applications and automation tools.

---

## 🚀 Next Lab

**Lab 16 — Virtual Environments (venv)**
