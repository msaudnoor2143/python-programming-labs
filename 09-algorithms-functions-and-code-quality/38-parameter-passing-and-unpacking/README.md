# 🧩 Lab 38 — Parameter Passing & Unpacking

This lab explores flexible function arguments in Python using `*args` and `**kwargs`, along with argument unpacking using the `*` and `**` operators.

---

## 🎯 Objective

By completing this lab, you will:

- Understand parameter passing in Python.
- Use `*args` for variable positional arguments.
- Use `**kwargs` for variable keyword arguments.
- Unpack sequences using `*`.
- Unpack dictionaries using `**`.
- Apply these techniques through practical functions.

---

## 📚 Prerequisites

- Basic understanding of Python functions.
- Familiarity with Python data types.
- Familiarity with lists.
- Familiarity with dictionaries.

---

## 🧠 Introduction

Python functions can be designed to accept flexible numbers of arguments.

Two useful mechanisms are:

```python
*args
```

and:

```python
**kwargs
```

They allow functions to accept variable numbers of positional and keyword arguments.

Python also provides `*` and `**` operators for unpacking sequences and dictionaries when calling functions.

---

# 🔢 Task 1 — Using `*args`

`*args` allows a function to accept a variable number of positional arguments.

Inside the function, the arguments are stored in a tuple.

---

## Example

```python
def sum_numbers(*args):
    return sum(args)
```

The function can accept different numbers of arguments:

```python
sum_numbers(1, 2)
sum_numbers(1, 2, 3, 4)
```

---

## Exercise — Create `add_numbers()`

Create a function that calculates the sum of all supplied arguments.

```python
def add_numbers(*args):
    total = 0

    for num in args:
        total += num

    return total
```

Test it:

```python
result = add_numbers(1, 2, 3, 4, 5)

print(result)
```

Expected result:

```text
15
```

---

# 🏷️ Task 2 — Using `**kwargs`

`**kwargs` allows a function to accept a variable number of keyword arguments.

Inside the function, the arguments are stored in a dictionary.

---

## Example

```python
def print_kwargs(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")
```

---

## Exercise — Create `show_info()`

```python
def show_info(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")
```

Test it:

```python
show_info(
    name="Alice",
    age=30,
    city="New York"
)
```

The function receives the named values through the `kwargs` dictionary.

---

# 📦 Task 3 — Unpacking with `*`

The `*` operator can unpack a sequence into positional arguments.

Create a list:

```python
numbers = [1, 2, 3, 4]
```

Pass the list to `sum_numbers()` using unpacking:

```python
print(sum_numbers(*numbers))
```

The list values are supplied as separate positional arguments.

Conceptually:

```text
numbers = [1, 2, 3, 4]

sum_numbers(*numbers)

↓

sum_numbers(1, 2, 3, 4)
```

---

# 🗂️ Task 4 — Unpacking with `**`

The `**` operator can unpack a dictionary into keyword arguments.

Create a dictionary:

```python
data = {
    'name': 'John',
    'age': 25
}
```

Pass it to `print_kwargs()`:

```python
print_kwargs(**data)
```

The dictionary keys become keyword argument names.

---

# 🧪 Task 5 — Dictionary Unpacking Exercise

Create an `info` dictionary:

```python
info = {
    'occupation': 'Engineer',
    'country': 'USA'
}
```

Pass it to `show_info()` using `**`:

```python
show_info(**info)
```

---

## 🔬 Complete Example

```python
def sum_numbers(*args):
    return sum(args)


def add_numbers(*args):
    total = 0

    for num in args:
        total += num

    return total


def print_kwargs(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")


def show_info(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")


# *args
print("Sum:", sum_numbers(1, 2, 3, 4))

print("Add:", add_numbers(1, 2, 3, 4, 5))


# **kwargs
show_info(
    name="Alice",
    age=30,
    city="New York"
)


# List unpacking
numbers = [1, 2, 3, 4]

print("Unpacked sum:", sum_numbers(*numbers))


# Dictionary unpacking
data = {
    'name': 'John',
    'age': 25
}

print_kwargs(**data)


info = {
    'occupation': 'Engineer',
    'country': 'USA'
}

show_info(**info)
```

---

## 🧠 Key Concepts

### `*args`

Used for a variable number of positional arguments.

Arguments are received as a tuple.

### `**kwargs`

Used for a variable number of keyword arguments.

Arguments are received as a dictionary.

### `*` Unpacking

Unpacks a sequence into positional arguments.

### `**` Unpacking

Unpacks a dictionary into keyword arguments.

---

## 🛡️ Cybersecurity Perspective

Flexible argument handling is useful when building reusable Python automation and security utilities.

For example, a function may need to accept different optional parameters depending on the task being performed.

Understanding `*args`, `**kwargs`, and unpacking helps developers design reusable functions and interfaces.

---

## 📸 Evidence / Screenshots

Capture:

- `*args` implementation.
- `**kwargs` implementation.
- List unpacking.
- Dictionary unpacking.
- Terminal output.

Suggested structure:

```text
38-parameter-passing-and-unpacking/
├── README.md
└── screenshots/
    ├── args-kwargs-code.png
    └── args-kwargs-output.png
```

---

## 🧠 Self-Check

1. What does `*args` do?
2. What data structure stores `args` inside a function?
3. What does `**kwargs` do?
4. What data structure stores `kwargs`?
5. What does `*` do during a function call?
6. What does `**` do during a function call?
7. How can list values be passed using `*`?
8. How can dictionary values be passed using `**`?

---

## ✅ Completion Checklist

- [ ] Created a function using `*args`.
- [ ] Tested multiple positional arguments.
- [ ] Created a function using `**kwargs`.
- [ ] Tested multiple keyword arguments.
- [ ] Unpacked a list using `*`.
- [ ] Unpacked a dictionary using `**`.
- [ ] Captured useful evidence.
- [ ] Reviewed practical applications.

---

## 🏁 Conclusion

In this lab, you explored flexible parameter passing with `*args` and `**kwargs`.

You also practiced unpacking lists and dictionaries using `*` and `**`.

These features are important for writing flexible and reusable Python functions.

---

## ➡️ Next Lab

**Lab 39 — Python Style & PEP 8 Checks**
