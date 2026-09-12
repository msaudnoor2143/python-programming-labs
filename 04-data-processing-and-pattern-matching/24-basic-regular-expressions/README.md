# Lab 24 — Basic Regular Expressions

> Learn how to use Python's `re` module to search, match, replace, and extract structured patterns from text.

---

## 🎯 Objective

By completing this lab, you will learn how to:

- Understand basic regular expressions
- Use Python's `re` module
- Compile regex patterns
- Find matching text
- Replace matching patterns
- Use special regex characters
- Create regex groups
- Use named groups
- Extract structured information from strings

---

## 📚 Prerequisites

Before starting this lab, you should have:

- Basic Python programming knowledge
- Familiarity with strings
- Understanding of basic string operations
- Python installed
- Access to a code editor or IDE

Recommended previous labs:

- **Lab 03 — Data Types & Variables**
- **Lab 10 — Basic Functions**
- **Lab 21 — List & Dictionary Comprehensions**

---

# 1. Introduction to Regular Expressions

Regular expressions, commonly called **regex**, are patterns used to search and process text.

They are useful for tasks such as:

- Searching text
- Finding patterns
- Extracting information
- Replacing text
- Validating structured input
- Parsing text

Python provides regular-expression functionality through the built-in:

```python
re
```

module.

---

# 2. Task 1 — Import the `re` Module

Start by importing the module:

```python
import re
```

No external package is required.

---

# 3. Task 2 — Compile a Regular Expression Pattern

Use `re.compile()` to create a reusable regex pattern.

To match digits, use:

```python
r"\d+"
```

Here:

- `\d` matches a digit
- `+` means one or more occurrences

Create the pattern:

```python
import re

pattern = re.compile(r"\d+")
```

---

# 4. Task 3 — Find All Matches

Create a test string:

```python
test_string = "The rainfall 2021 was greater than 2019 and 2020 combined."
```

Use `findall()` to locate all matching numbers:

```python
import re

pattern = re.compile(r"\d+")

test_string = "The rainfall 2021 was greater than 2019 and 2020 combined."

matches = pattern.findall(test_string)

print("Matches found:", matches)
```

### Expected output

```text
Matches found: ['2021', '2019', '2020']
```

The numbers are returned as strings.

---

# 5. Task 4 — Replace Matches

The `sub()` method can replace text matching a pattern.

Example:

```python
import re

pattern = re.compile(r"\d+")

test_string = "The rainfall 2021 was greater than 2019 and 2020 combined."

replaced_string = pattern.sub("XXXX", test_string)

print("Replaced String:", replaced_string)
```

### Expected output

```text
Replaced String: The rainfall XXXX was greater than XXXX and XXXX combined.
```

This demonstrates how regex can be used for text transformation.

---

# 6. Task 5 — Use Groups and Special Characters

Regular expressions can use parentheses to create groups.

For example, a date can be represented as:

```text
YYYY-MM-DD
```

Create a pattern:

```python
date_pattern = re.compile(r"(\d{4})-(\d{2})-(\d{2})")
```

The pattern contains three groups:

```text
(\d{4})  → year
(\d{2})  → month
(\d{2})  → day
```

---

# 7. Match Dates

Create a test string:

```python
date_string = "Date of birth: 1990-08-15 and starting date 2020-01-01."
```

Find the dates:

```python
import re

date_pattern = re.compile(r"(\d{4})-(\d{2})-(\d{2})")

date_string = "Date of birth: 1990-08-15 and starting date 2020-01-01."

date_matches = date_pattern.findall(date_string)

print("Date Matches:", date_matches)
```

The groups allow the date components to be captured separately.

---

# 8. Named Groups

Named groups make regex patterns easier to understand.

The syntax is:

```text
(?P<name>pattern)
```

Create a named date pattern:

```python
import re

named_date_pattern = re.compile(
    r"(?P<year>\d{4})-(?P<month>\d{2})-(?P<day>\d{2})"
)
```

Now use `finditer()`:

```python
date_string = "Date of birth: 1990-08-15 and starting date 2020-01-01."

named_date_matches = named_date_pattern.finditer(date_string)

for match in named_date_matches:
    print(
        "Year:", match.group("year"),
        "Month:", match.group("month"),
        "Day:", match.group("day")
    )
```

This makes each captured component explicitly identifiable.

---

# 9. Complete Example

The following combines the main exercises from the lab:

```python
import re

# Find numbers
pattern = re.compile(r"\d+")

test_string = "The rainfall 2021 was greater than 2019 and 2020 combined."

matches = pattern.findall(test_string)

print("Matches found:", matches)

# Replace numbers
replaced_string = pattern.sub("XXXX", test_string)

print("Replaced String:", replaced_string)

# Match dates
date_pattern = re.compile(r"(\d{4})-(\d{2})-(\d{2})")

date_string = "Date of birth: 1990-08-15 and starting date 2020-01-01."

date_matches = date_pattern.findall(date_string)

print("Date Matches:", date_matches)

# Named groups
named_date_pattern = re.compile(
    r"(?P<year>\d{4})-(?P<month>\d{2})-(?P<day>\d{2})"
)

named_date_matches = named_date_pattern.finditer(date_string)

for match in named_date_matches:
    print(
        "Year:", match.group("year"),
        "Month:", match.group("month"),
        "Day:", match.group("day")
    )
```

---

# 🧠 Key Concepts

### `re.compile()`

Compiles a regular-expression pattern.

```python
pattern = re.compile(r"\d+")
```

### `findall()`

Returns all matches.

```python
matches = pattern.findall(text)
```

### `sub()`

Replaces matching text.

```python
pattern.sub("XXXX", text)
```

### Groups

Parentheses create capture groups.

```python
(\d{4})
```

### Named groups

Give a capture group a meaningful name.

```python
(?P<year>\d{4})
```

### `finditer()`

Returns match objects that can be inspected individually.

```python
for match in pattern.finditer(text):
    print(match.group())
```

---

# 🛡️ Security Perspective

Regular expressions are highly useful in cybersecurity and defensive automation.

They can help process text such as:

- Log files
- Alert messages
- Configuration data
- Security reports
- Structured identifiers
- Network-related text
- Application output

For example, a security analyst may need to locate date-like patterns in a large text dataset.

Regex can also assist with extracting structured information before further analysis.

> **Important:** Regex is a pattern-processing tool, not a complete security-validation mechanism. Complex input validation should be designed carefully and tested against unexpected input.

---

# 📸 Evidence / Screenshots

Useful evidence for this lab includes:

- Regex pattern execution
- Numbers extracted using `findall()`
- Text transformed using `sub()`
- Date groups extracted
- Named-group output

Suggested structure:

```text
24-basic-regular-expressions/
├── README.md
├── regex_basics.py
└── screenshots/
    └── regex-output.png
```

---

# ⚠️ Best Practices

- Use raw strings such as `r"\d+"` for regex patterns.
- Keep patterns understandable.
- Test patterns against multiple inputs.
- Be careful with complex regex expressions.
- Do not assume a regex automatically provides complete security validation.
- Document complicated patterns.
- Avoid unnecessarily complicated expressions when simpler string operations are sufficient.

---

# 📝 Self-Check

1. What is a regular expression?
2. What does Python's `re` module provide?
3. What does `\d` represent?
4. What does `+` mean in `\d+`?
5. What does `findall()` do?
6. What does `sub()` do?
7. What are regex groups?
8. What are named groups?
9. What does `finditer()` provide?
10. How can regex be useful when processing security logs?

---

# ✅ Lab Completion Checklist

- [ ] I understand the purpose of regular expressions.
- [ ] I imported the `re` module.
- [ ] I compiled a regex pattern.
- [ ] I used `findall()`.
- [ ] I used `sub()`.
- [ ] I created regex groups.
- [ ] I matched structured dates.
- [ ] I used named groups.
- [ ] I used `finditer()`.
- [ ] I understand regex applications in cybersecurity.
- [ ] I completed the practical exercises.
- [ ] I captured meaningful execution evidence.

---

# 📌 Conclusion

In this lab, you learned the fundamentals of regular expressions using Python's `re` module.

You practiced:

- Compiling patterns
- Finding matches
- Replacing text
- Creating groups
- Using named groups
- Extracting structured information

These skills are particularly useful for text processing, automation, data analysis, and defensive cybersecurity tasks involving structured or semi-structured text.

---

## 🎉 Section 04 Complete

You have now completed the documentation for:

- **Lab 21 — List & Dictionary Comprehensions**
- **Lab 22 — Reading CSV Files**
- **Lab 23 — Using Requests for HTTP Calls**
- **Lab 24 — Basic Regular Expressions**

### 🚀 Next Section

**Section 05 — Testing & Advanced Python Features**

- Lab 25 — Intro to Unit Testing with `unittest`
- Lab 26 — Decorators: Basic Usage
- Lab 27 — Context Managers (`with` statement)
