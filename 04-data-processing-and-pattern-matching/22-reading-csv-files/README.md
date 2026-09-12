# Lab 22 — Reading CSV Files

> Learn how to read and process tabular data stored in CSV files using Python's built-in `csv` module.

---

## 🎯 Objective

By completing this lab, you will learn how to:

- Understand CSV files
- Import Python's `csv` module
- Open CSV files for reading
- Read CSV rows using `csv.reader()`
- Handle CSV files with headers
- Handle CSV files without headers
- Use `csv.DictReader()`
- Store CSV records as dictionaries
- Process structured tabular data

---

## 📚 Prerequisites

Before starting this lab, you should have:

- Basic Python programming knowledge
- Python installed on your machine
- Familiarity with strings and lists
- Basic file-handling knowledge

Recommended previous labs:

- **Lab 07 — Lists & List Methods**
- **Lab 12 — File I/O Basics**
- **Lab 21 — List & Dictionary Comprehensions**

---

# 1. Introduction to CSV Files

CSV stands for **Comma-Separated Values**.

It is a simple format commonly used to store tabular data.

Example:

```text
name,age,department
Alice,30,Security
Bob,25,Networking
Charlie,28,Development
```

Each line represents a record, while commas separate individual fields.

CSV files are commonly used for:

- Data exchange
- Reports
- Spreadsheets
- Logs
- Data analysis
- Application imports and exports

---

# 2. Task 1 — Understand the CSV Module

Python provides a built-in module called `csv` for working with CSV files.

Import it with:

```python
import csv
```

No external package is required.

---

# 3. Task 2 — Open a CSV File

Create a file named:

```text
sample.csv
```

For example:

```csv
name,age,department
Alice,30,Security
Bob,25,Networking
Charlie,28,Development
```

Now open the file using Python:

```python
import csv

file_path = "sample.csv"

with open(file_path, mode="r") as file:
    pass
```

The `with` statement ensures that the file is properly managed after the operation completes.

---

# 4. Task 3 — Read CSV Content

Use `csv.reader()` to process the file.

```python
import csv

file_path = "sample.csv"

with open(file_path, mode="r") as file:
    csv_reader = csv.reader(file)

    for row in csv_reader:
        print(row)
```

Each row is returned as a list of strings.

### Example output

```text
['name', 'age', 'department']
['Alice', '30', 'Security']
['Bob', '25', 'Networking']
['Charlie', '28', 'Development']
```

---

# 5. Task 4 — Handling CSV Headers

Many CSV files contain a header row.

For example:

```csv
name,age,department
Alice,30,Security
Bob,25,Networking
```

The first row contains the column names.

You can skip the header using `next()`:

```python
import csv

file_path = "sample.csv"

with open(file_path, mode="r") as file:
    csv_reader = csv.reader(file)

    header = next(csv_reader)

    print("Header:", header)

    for row in csv_reader:
        print(row)
```

This allows the remaining loop to process only the actual records.

---

# 6. CSV Files Without Headers

If a CSV file does not contain a header row, you can directly iterate through it:

```python
import csv

file_path = "sample.csv"

with open(file_path, mode="r") as file:
    csv_reader = csv.reader(file)

    for row in csv_reader:
        print(row)
```

The appropriate approach depends on the structure of the CSV file.

---

# 7. Task 5 — Store CSV Data as Dictionaries

For more structured processing, Python provides `csv.DictReader()`.

```python
import csv

file_path = "sample.csv"

data_list = []

with open(file_path, mode="r") as file:
    csv_reader = csv.DictReader(file)

    for row in csv_reader:
        data_list.append(row)

for item in data_list:
    print(item)
```

### Example output

```text
{'name': 'Alice', 'age': '30', 'department': 'Security'}
{'name': 'Bob', 'age': '25', 'department': 'Networking'}
{'name': 'Charlie', 'age': '28', 'department': 'Development'}
```

Each row becomes a dictionary where the CSV headers are used as keys.

---

# 8. Accessing Individual Fields

Once the rows are represented as dictionaries, individual fields can be accessed using their column names.

Example:

```python
for item in data_list:
    print("Name:", item["name"])
    print("Department:", item["department"])
```

This can be easier to work with than numeric list indexes.

---

# 🧠 Key Concepts

### `csv`

Python's built-in module for working with CSV files.

```python
import csv
```

### `csv.reader()`

Reads CSV rows as lists.

```python
csv_reader = csv.reader(file)
```

### `next()`

Can be used to read or skip the first row.

```python
header = next(csv_reader)
```

### `csv.DictReader()`

Reads CSV records as dictionaries.

```python
csv_reader = csv.DictReader(file)
```

---

# 🛡️ Security Perspective

CSV processing is useful in cybersecurity automation and analysis.

Security teams may receive CSV data containing:

- Security events
- Asset inventories
- User records
- Vulnerability reports
- Network information
- Incident data
- Authentication records

Python can process these datasets before further analysis.

For example:

```python
import csv

with open("security_events.csv", mode="r") as file:
    csv_reader = csv.DictReader(file)

    for event in csv_reader:
        if event["severity"] == "HIGH":
            print("High severity event:", event)
```

This demonstrates how structured security data can be filtered programmatically.

> **Security note:** Avoid committing real credentials, personal information, tokens, or sensitive organizational data to a public GitHub repository.

---

# 📸 Evidence / Screenshots

Useful evidence for this lab includes:

- The `sample.csv` file
- Terminal output showing CSV rows
- Header handling
- `DictReader()` output

Suggested structure:

```text
22-reading-csv-files/
├── README.md
├── sample.csv
├── read_csv.py
└── screenshots/
    └── csv-output.png
```

Use sample or synthetic data for a public portfolio.

---

# ⚠️ Best Practices

- Use `with open(...)` when working with files.
- Understand whether the CSV contains headers.
- Use `DictReader()` when named fields make processing clearer.
- Validate input data before relying on it.
- Avoid exposing sensitive information.
- Keep sample datasets safe for public repositories.

---

# 📝 Self-Check

1. What does CSV stand for?
2. What does Python's `csv` module provide?
3. What does `csv.reader()` return for each row?
4. How can you skip a CSV header?
5. What is `csv.DictReader()`?
6. What is the advantage of representing rows as dictionaries?
7. Where might CSV data appear in cybersecurity?
8. Why should sensitive CSV files not be committed to a public repository?

---

# ✅ Lab Completion Checklist

- [ ] I understand the CSV format.
- [ ] I can import the `csv` module.
- [ ] I can open a CSV file.
- [ ] I can read rows with `csv.reader()`.
- [ ] I can handle a header row.
- [ ] I understand CSV files without headers.
- [ ] I can use `csv.DictReader()`.
- [ ] I can store CSV records as dictionaries.
- [ ] I understand CSV processing in cybersecurity.
- [ ] I completed the practical exercises.

---

# 📌 Conclusion

In this lab, you learned how to read and process CSV files using Python's built-in `csv` module.

You practiced:

- Reading CSV files
- Handling headers
- Iterating through rows
- Using `DictReader()`
- Converting tabular data into structured dictionaries

These skills provide a foundation for data processing, automation, and security-data analysis.

---

## 🚀 Next Lab

**Lab 23 — Using Requests for HTTP Calls**
