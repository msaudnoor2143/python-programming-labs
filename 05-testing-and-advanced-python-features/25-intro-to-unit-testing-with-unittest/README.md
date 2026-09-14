# Lab 25 — Intro to Unit Testing with `unittest`

> Learn the fundamentals of unit testing in Python and use the built-in `unittest` framework to verify that individual functions behave as expected.

---

## 🎯 Objective

By completing this lab, you will learn how to:

- Understand the purpose of unit testing
- Use Python's built-in `unittest` module
- Create basic test cases
- Use `unittest.TestCase`
- Use assertions such as `assertEqual`
- Run tests using test discovery
- Interpret test results
- Understand how testing improves software reliability

---

## 📚 Prerequisites

Before starting this lab, you should have:

- Basic understanding of Python programming
- Familiarity with functions
- Ability to write and execute Python scripts

Recommended previous labs:

- **Lab 10 — Basic Functions**
- **Lab 15 — Basic Debugging Techniques**

---

# 1. Introduction to Unit Testing

Unit testing is a software-development practice used to verify that individual components of a program work correctly.

A **unit** is usually a small, isolated part of a program, such as a function.

For example:

```python
def add(a, b):
    return a + b
```

A unit test can verify that this function produces the expected result.

Testing helps developers detect problems early and provides confidence when modifying code.

---

# 2. Task 1 — Set Up the Testing Environment

Python must be installed on your system.

Verify Python:

```bash
python3 --version
```

Create a new Python file:

```text
test_example.py
```

This file will contain the function and its test case.

---

# 3. Task 2 — Write a Simple Function to Test

Create a simple addition function:

```python
def add(a, b):
    return a + b
```

The function accepts two values and returns their sum.

For example:

```python
result = add(2, 3)

print(result)
```

Expected output:

```text
5
```

Instead of manually checking the result every time, we can create an automated test.

---

# 4. Task 3 — Import `unittest`

Import Python's built-in testing framework:

```python
import unittest
```

No external package is required.

---

# 5. Task 4 — Create a Test Case

Create a class that inherits from `unittest.TestCase`:

```python
class TestMath(unittest.TestCase):

    def test_add(self):
        self.assertEqual(add(2, 3), 5)
```

The complete script becomes:

```python
import unittest


def add(a, b):
    return a + b


class TestMath(unittest.TestCase):

    def test_add(self):
        self.assertEqual(add(2, 3), 5)
```

---

# 6. Understanding `unittest.TestCase`

`unittest.TestCase` is the base class used to create test cases.

Our class:

```python
class TestMath(unittest.TestCase):
```

inherits testing functionality from `unittest.TestCase`.

The method:

```python
def test_add(self):
```

contains the actual test.

Python's test discovery recognizes methods beginning with:

```text
test
```

---

# 7. Understanding `assertEqual`

The test uses:

```python
self.assertEqual(add(2, 3), 5)
```

This checks whether:

```python
add(2, 3)
```

is equal to:

```python
5
```

If they are equal, the test passes.

If they are different, the test fails.

This provides an automated way to verify program behavior.

---

# 8. Task 5 — Run the Test

Use Python's unittest discovery mechanism:

```bash
python3 -m unittest discover
```

If your environment uses `python` instead of `python3`, you can use:

```bash
python -m unittest discover
```

The test discovery mechanism looks for test files and runs the tests it finds.

---

# 9. Understanding Test Output

A successful test produces output similar to:

```text
.
----------------------------------------------------------------------
Ran 1 test in 0.001s

OK
```

The important parts are:

### `.`

A dot represents a successful test.

### `Ran 1 test`

One test was executed.

### `OK`

All executed tests passed.

---

# 10. Experiment — Make the Test Fail

To understand test results, temporarily change:

```python
self.assertEqual(add(2, 3), 5)
```

to:

```python
self.assertEqual(add(2, 3), 10)
```

The test should now fail because:

```text
2 + 3 = 5
```

not:

```text
10
```

Restore the correct assertion afterward:

```python
self.assertEqual(add(2, 3), 5)
```

This demonstrates why automated testing is useful.

---

# 11. Complete Lab Example

```python
import unittest


def add(a, b):
    return a + b


class TestMath(unittest.TestCase):

    def test_add(self):
        self.assertEqual(add(2, 3), 5)


if __name__ == "__main__":
    unittest.main()
```

You can run it directly with:

```bash
python3 test_example.py
```

You can also use test discovery:

```bash
python3 -m unittest discover
```

---

# 🧠 Key Concepts

### Unit test

A test designed to verify an individual component of a program.

### `unittest`

Python's built-in unit-testing framework.

```python
import unittest
```

### `TestCase`

Base class for creating test cases.

```python
class TestMath(unittest.TestCase):
```

### `assertEqual`

Checks whether two values are equal.

```python
self.assertEqual(actual, expected)
```

### Test discovery

Automatically finds and executes tests.

```bash
python3 -m unittest discover
```

---

# 🛡️ Security Perspective

Testing is important for cybersecurity software because security tools must behave predictably.

Unit tests can be used to verify functions involved in:

- Log processing
- Input validation
- Detection rules
- Data parsing
- Security automation
- Configuration processing
- Alert generation
- Access-control logic

For example, a security tool might contain a function that classifies an event:

```python
def classify_event(severity):
    if severity == "HIGH":
        return "ALERT"
    return "NORMAL"
```

A test can verify that the classification behaves correctly.

Reliable testing reduces the chance that a software change unintentionally breaks security-related functionality.

---

# 📸 Evidence / Screenshots

Useful evidence for your GitHub portfolio includes:

- Test script
- Successful test execution
- `OK` result
- Failed-test demonstration followed by the corrected test

Suggested structure:

```text
25-intro-to-unit-testing-with-unittest/
├── README.md
├── test_example.py
└── screenshots/
    ├── test-success.png
    └── test-failure-example.png
```

The failure screenshot is optional; the successful test result is the most important evidence.

---

# ⚠️ Best Practices

- Write small, focused tests.
- Use meaningful test names.
- Test expected behavior rather than implementation details.
- Run tests after modifying important code.
- Keep tests repeatable.
- Do not ignore failed tests.
- Keep test data safe and non-sensitive.

---

# 📝 Self-Check

1. What is unit testing?
2. Why is unit testing useful?
3. What is Python's `unittest` module?
4. What is `unittest.TestCase`?
5. What does `assertEqual()` do?
6. How does Python identify test methods?
7. What does `python3 -m unittest discover` do?
8. What does `OK` mean in unittest output?
9. Why is testing important for security-related software?

---

# ✅ Lab Completion Checklist

- [ ] I understand the purpose of unit testing.
- [ ] I imported `unittest`.
- [ ] I created a function to test.
- [ ] I created a `TestCase` class.
- [ ] I used `assertEqual`.
- [ ] I ran the test successfully.
- [ ] I understand test discovery.
- [ ] I understand successful and failed test results.
- [ ] I completed the practical exercise.
- [ ] I captured useful testing evidence.

---

# 📌 Conclusion

In this lab, you learned the fundamentals of unit testing in Python using the built-in `unittest` framework.

You created a function, wrote an automated test, executed the test, and interpreted the result.

Unit testing provides an important foundation for developing reliable, maintainable, and trustworthy Python applications.

---

## 🚀 Next Lab

**Lab 26 — Decorators: Basic Usage**
