# 🧮 Lab 04 — Arithmetic & Expressions

## 🎯 Objective

Understand and apply basic arithmetic operations in Python and explore the difference between integer division and standard floating-point division.

By completing this lab, you will practice:

- Addition
- Subtraction
- Multiplication
- Division
- Integer division
- Floating-point division
- User input
- Arithmetic expressions

---

## 📚 Prerequisites

- Basic Python programming knowledge
- Understanding of fundamental arithmetic operations
- Python 3 installed

---

## 📁 Lab Structure

```text
04-arithmetic-and-expressions/
├── README.md
├── arithmetic_operations.py
└── screenshots/
```

---

# 🧪 Lab Tasks

## Task 1 — Basic Arithmetic Operations

Create a file named:

```text
arithmetic_operations.py
```

Use `input()` to receive two numbers.

```python
number1 = int(input("Enter the first number: "))
number2 = int(input("Enter the second number: "))
```

Perform addition:

```python
addition_result = number1 + number2
print(f"Addition: {number1} + {number2} = {addition_result}")
```

Perform subtraction:

```python
subtraction_result = number1 - number2
print(f"Subtraction: {number1} - {number2} = {subtraction_result}")
```

Perform multiplication:

```python
multiplication_result = number1 * number2
print(f"Multiplication: {number1} * {number2} = {multiplication_result}")
```

Perform division:

```python
division_result = number1 / number2
print(f"Division: {number1} / {number2} = {division_result}")
```

---

## Task 2 — Integer Division vs Float Division

### Integer Division

Python uses `//` for floor division.

```python
integer_division_result = number1 // number2

print(
    f"Integer Division: {number1} // {number2} = {integer_division_result}"
)
```

### Floating-Point Division

Python uses `/` for standard division.

```python
float_division_result = number1 / number2

print(
    f"Float Division: {number1} / {number2} = {float_division_result}"
)
```

### Example

For:

```text
10 / 3
```

standard division produces a decimal result, while:

```text
10 // 3
```

returns the floor value.

---

# 🔎 Command Reference

| Operator | Operation |
|---|---|
| `+` | Addition |
| `-` | Subtraction |
| `*` | Multiplication |
| `/` | Float division |
| `//` | Integer/floor division |

---

# 🧠 Key Concepts

### Addition

Combines two values.

```python
10 + 5
```

### Subtraction

Subtracts one value from another.

```python
10 - 5
```

### Multiplication

Calculates the product.

```python
10 * 5
```

### Division

Performs standard division.

```python
10 / 5
```

### Integer Division

Returns the floor result.

```python
10 // 3
```

---

# 🧪 Further Exploration

Experiment with:

- Larger numbers
- Negative numbers
- Decimal numbers
- Different division values

Try applying arithmetic operations to practical problems such as:

- Area calculations
- Budget calculations
- Unit conversions
- Basic numerical analysis

---

# 🛡️ Security Perspective

Arithmetic operations are frequently used in security and systems programming.

Examples include:

- Calculating resource usage
- Processing numerical thresholds
- Analyzing security metrics
- Calculating rates and percentages
- Processing counters and statistics

Correct handling of numerical operations is important because unexpected values can lead to incorrect program behavior.

---

# 📝 Self-Check Questions

1. What operator performs addition?
2. What operator performs multiplication?
3. What is the difference between `/` and `//`?
4. What does integer division return?
5. Why is `input()` converted using `int()` in this lab?
6. What happens if the second number is zero during division?

---

# ✅ Lab Completion Checklist

- [ ] I can accept numerical input.
- [ ] I can perform addition.
- [ ] I can perform subtraction.
- [ ] I can perform multiplication.
- [ ] I can perform division.
- [ ] I understand `/`.
- [ ] I understand `//`.
- [ ] I experimented with different values.

---

## 📸 Evidence

Recommended screenshots:

- Python script
- Program execution
- Arithmetic results
- `/` versus `//` output

Store evidence in:

```text
screenshots/
```

---

## 📌 Summary

In this lab, you implemented fundamental arithmetic operations and explored the difference between standard division and integer/floor division.

## 🚀 Next Lab

**Lab 05 — Understanding Conditionals (if, elif, else)**
