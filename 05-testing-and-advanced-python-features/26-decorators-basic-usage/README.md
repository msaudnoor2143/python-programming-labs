# Lab 26 — Decorators: Basic Usage

> Learn how Python decorators can wrap existing functions and add reusable functionality without modifying the function's core logic.

---

## 🎯 Objective

By completing this lab, you will learn how to:

- Understand the concept of decorators
- Understand decorator syntax
- Create a basic decorator
- Wrap an existing function
- Use the `@` decorator syntax
- Work with `*args` and `**kwargs`
- Understand practical uses such as logging and caching
- Recognize decorators as a form of reusable functionality

---

## 📚 Prerequisites

Before starting this lab, you should have:

- Basic understanding of Python
- Familiarity with functions
- Understanding of function calls
- Understanding of parameters and return values

Recommended previous labs:

- **Lab 10 — Basic Functions**
- **Lab 20 — Using Lambda & Higher-Order Functions**
- **Lab 25 — Intro to Unit Testing with unittest**

---

# 1. Introduction to Python Decorators

A decorator is a Python design pattern used to modify or extend the behavior of an existing function or method.

Instead of changing the original function directly, a decorator can **wrap** it and add additional behavior.

Conceptually:

```text
Original Function
       ↓
    Decorator
       ↓
Wrapped Function
```

This makes decorators useful for functionality that needs to be applied to multiple functions.

---

# 2. Task 1 — Create a Basic Decorator

Create a decorator named:

```python
log_decorator
```

The decorator will display a message before and after the wrapped function executes.

```python
def log_decorator(func):

    def wrapper(*args, **kwargs):
        print("Start")

        result = func(*args, **kwargs)

        print("End")

        return result

    return wrapper
```

---

# 3. Understanding the Decorator

The decorator receives a function:

```python
def log_decorator(func):
```

Inside it, we create another function:

```python
def wrapper(*args, **kwargs):
```

The wrapper:

1. Prints `"Start"`
2. Executes the original function
3. Prints `"End"`
4. Returns the original result

The original function is:

```python
func
```

and is executed with:

```python
result = func(*args, **kwargs)
```

---

# 4. Understanding `*args` and `**kwargs`

The wrapper uses:

```python
*args
```

to accept positional arguments and:

```python
**kwargs
```

to accept keyword arguments.

This allows the decorator to work with functions that accept different arguments.

For example:

```python
def example(name, age):
    print(name, age)
```

The wrapper can still pass those arguments through to the original function.

---

# 5. Task 2 — Apply the Decorator

Use the `@` symbol to apply the decorator.

```python
@log_decorator
def say_hello(name):
    print(f"Hello, {name}!")
```

Now call the function:

```python
say_hello("Alice")
```

The complete example is:

```python
def log_decorator(func):

    def wrapper(*args, **kwargs):
        print("Start")

        result = func(*args, **kwargs)

        print("End")

        return result

    return wrapper


@log_decorator
def say_hello(name):
    print(f"Hello, {name}!")


say_hello("Alice")
```

Expected output:

```text
Start
Hello, Alice!
End
```

---

# 6. Understanding the `@` Syntax

This:

```python
@log_decorator
def say_hello(name):
    print(f"Hello, {name}!")
```

is a concise way of applying the decorator to the function.

Conceptually, Python transforms the function so that the decorator wraps it.

The result is that calling:

```python
say_hello("Alice")
```

causes the additional behavior to execute around the original function.

---

# 7. Decorators and Cross-Cutting Concerns

One major benefit of decorators is handling functionality that applies to many parts of an application.

Examples include:

### Logging

Record when a function executes.

```text
Function started
Function completed
```

### Caching

Store results so repeated operations can be performed more efficiently.

### Monitoring

Track function execution or application behavior.

### Access control

In appropriate applications, decorators can enforce whether a function should be available under certain conditions.

---

# 8. Reusing the Decorator

A decorator can be applied to multiple functions.

Example:

```python
def log_decorator(func):

    def wrapper(*args, **kwargs):
        print("Start")
        result = func(*args, **kwargs)
        print("End")
        return result

    return wrapper


@log_decorator
def say_hello(name):
    print(f"Hello, {name}!")


@log_decorator
def say_goodbye(name):
    print(f"Goodbye, {name}!")


say_hello("Alice")
say_goodbye("Alice")
```

The same logging behavior can now be reused without duplicating it inside every function.

---

# 🧠 Key Concepts

### Decorator

A mechanism for extending or modifying the behavior of a function.

### Wrapper

The inner function that surrounds the original function.

```python
def wrapper(*args, **kwargs):
```

### `@` syntax

Provides a concise way to apply a decorator.

```python
@log_decorator
```

### `*args`

Accepts positional arguments.

### `**kwargs`

Accepts keyword arguments.

### Cross-cutting concerns

Functionality that applies across multiple parts of an application, such as logging or caching.

---

# 🛡️ Security Perspective

Decorators can be useful in cybersecurity and security automation.

Potential applications include:

- Logging function execution
- Monitoring sensitive operations
- Applying access-control checks
- Auditing actions
- Measuring execution behavior
- Adding reusable validation logic

For example, a security-oriented application might use a decorator to consistently record when certain operations are performed.

The advantage is that the logging or checking logic can be maintained separately from the main business logic.

---

# 📸 Evidence / Screenshots

Useful evidence includes:

- The decorator implementation
- Successful execution of the decorated function
- `Start → function → End` output
- Applying the same decorator to multiple functions

Suggested structure:

```text
26-decorators-basic-usage/
├── README.md
├── decorators.py
└── screenshots/
    └── decorator-output.png
```

---

# ⚠️ Best Practices

- Keep decorators focused on one responsibility.
- Use meaningful decorator names.
- Avoid hiding important behavior inside complicated decorators.
- Preserve the original function's behavior and return value.
- Document decorators that modify important application behavior.
- Be especially careful when decorators affect security checks or authorization logic.

---

# 📝 Self-Check

1. What is a Python decorator?
2. Why are decorators useful?
3. What is a wrapper function?
4. What does the `@` syntax do?
5. Why are `*args` and `**kwargs` useful in decorators?
6. What are cross-cutting concerns?
7. How can decorators support logging?
8. How could decorators be useful in cybersecurity?
9. Why should decorators remain focused and understandable?

---

# ✅ Lab Completion Checklist

- [ ] I understand what a decorator is.
- [ ] I created a basic decorator.
- [ ] I created a wrapper function.
- [ ] I used `*args` and `**kwargs`.
- [ ] I applied a decorator using `@`.
- [ ] I executed a decorated function.
- [ ] I understand reusable decorator behavior.
- [ ] I understand logging and caching use cases.
- [ ] I understand the cybersecurity relevance.
- [ ] I captured useful execution evidence.

---

# 📌 Conclusion

In this lab, you learned how Python decorators can extend the behavior of existing functions.

You created a decorator that logs messages before and after function execution and applied it using the `@` syntax.

Decorators provide a clean way to reuse functionality such as logging, caching, and other cross-cutting concerns without duplicating code.

---

## 🚀 Next Lab

**Lab 27 — Context Managers (`with` Statement)**
