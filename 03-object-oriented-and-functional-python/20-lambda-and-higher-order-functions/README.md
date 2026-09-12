# ⚡ Lab 20 — Using Lambda & Higher-Order Functions

## 🎯 Objective

Learn how Python supports functional programming concepts through lambda expressions and higher-order functions.

By completing this lab, you will learn how to:

- Create lambda functions.
- Pass functions as arguments.
- Use functions that return other functions.
- Apply functions to collections.
- Understand basic functional programming techniques.

---

## 📚 Prerequisites

Before starting this lab, you should understand:

- Python functions.
- Function parameters.
- Return values.
- Lists and other basic collections.

---

## 🧠 Key Concepts

### Lambda Function

A lambda is a small anonymous function written as an expression.

Basic syntax:

```python
lambda arguments: expression
```

Example:

```python
square = lambda x: x * x
```

Calling it:

```python
print(square(5))
```

Expected output:

```text
25
```

---

### Higher-Order Function

A higher-order function is a function that accepts another function as an argument or returns a function.

Python treats functions as objects, which makes this possible.

---

# 🧪 Practical Lab

## Task 1 — Create a Lambda Function

Create:

```text
lambda_example.py
```

Define:

```python
square = lambda x: x * x
```

Test it:

```python
print("Square:", square(6))
```

Expected output:

```text
Square: 36
```

---

## Task 2 — Lambda With Multiple Arguments

Create a lambda function for addition:

```python
add = lambda a, b: a + b

print("Sum:", add(10, 5))
```

Expected output:

```text
Sum: 15
```

---

## Task 3 — Use a Function as an Argument

Create a higher-order function:

```python
def apply_function(function, value):
    return function(value)
```

Create a lambda:

```python
double = lambda x: x * 2
```

Pass the lambda to the function:

```python
result = apply_function(double, 10)

print("Result:", result)
```

Expected output:

```text
Result: 20
```

---

## Task 4 — Use Lambda With `map()`

Create a list:

```python
numbers = [1, 2, 3, 4, 5]
```

Use `map()`:

```python
squared_numbers = list(map(lambda x: x * x, numbers))

print("Squared numbers:", squared_numbers)
```

Expected output:

```text
Squared numbers: [1, 4, 9, 16, 25]
```

---

## Task 5 — Use Lambda With `filter()`

Filter even numbers:

```python
numbers = [1, 2, 3, 4, 5, 6]

even_numbers = list(filter(lambda x: x % 2 == 0, numbers))

print("Even numbers:", even_numbers)
```

Expected output:

```text
Even numbers: [2, 4, 6]
```

---

## 🔎 What You Practiced

This lab demonstrated:

- Lambda functions.
- Anonymous functions.
- Functions as objects.
- Higher-order functions.
- `map()`.
- `filter()`.
- Passing functions as arguments.

---

## 🧠 Functional Programming Concept

The basic relationship can be represented as:

```text
Function
   │
   ▼
Passed to another function
   │
   ▼
Processed
   │
   ▼
Result
```

This allows functions to be treated as reusable pieces of behavior.

---

## 🛡️ Cybersecurity Perspective

Functional programming techniques can be useful in cybersecurity data processing.

For example, a security application might process a collection of events and:

- Transform values.
- Filter events.
- Extract relevant information.
- Apply validation functions.
- Process large collections of records.

This can make certain data-processing operations concise and reusable.

---

## 📸 Evidence

Recommended evidence:

- Lambda execution.
- Higher-order function output.
- `map()` results.
- `filter()` results.
- Processed collection output.

---

## ⚠️ Best Practice

Lambda expressions are useful for small, simple operations.

For more complicated logic, a normal named function is often easier to read and maintain.

Prefer readability over unnecessarily compact code.

---

## 📝 Self-Check

- [ ] Can I write a lambda function?
- [ ] Can I pass a function as an argument?
- [ ] Can I explain what a higher-order function is?
- [ ] Can I use `map()`?
- [ ] Can I use `filter()`?
- [ ] Can I explain when a normal function is preferable to a lambda?

---

## ✅ Completion Checklist

- [ ] Lambda function created
- [ ] Multiple-argument lambda tested
- [ ] Higher-order function implemented
- [ ] Function passed as an argument
- [ ] `map()` tested
- [ ] `filter()` tested
- [ ] Output verified
- [ ] Evidence added where useful

---

## 🏁 Conclusion

This lab introduced lambda expressions and higher-order functions in Python.

These techniques provide a foundation for functional programming and can be useful when processing collections and building reusable data-processing logic.

---

## 🎉 Section 03 Complete

You have now completed:

- **Lab 17 — OOP: Defining Classes**
- **Lab 18 — OOP: Inheritance Basics**
- **Lab 19 — Basic Recursion Example**
- **Lab 20 — Using Lambda & Higher-Order Functions**

Next:

**Section 04 — Data Processing & Pattern Matching**
