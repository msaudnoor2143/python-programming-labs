# 🗄️ Lab 30 — Basic SQLite Usage

This lab introduces SQLite database programming using Python's built-in `sqlite3` module.

You will establish a database connection, create a table, insert records, query the database, and display the results.

---

## 🎯 Objective

By completing this lab, you will:

- Understand how to use SQLite with Python.
- Establish a connection to an SQLite database.
- Create a database table.
- Insert data into a table.
- Execute SQL queries.
- Retrieve database records.
- Print and interpret query results.
- Understand basic parameterized SQL operations.

---

## 📚 Prerequisites

- Basic Python programming knowledge.
- Python installed on your computer.
- Access to an IDE, text editor, or terminal.
- Basic understanding of variables and functions.

---

## 🧠 Introduction

SQLite is a lightweight database system that can be used directly from Python through the standard-library `sqlite3` module.

No additional Python package is required for the basic SQLite functionality used in this lab.

---

## 🧪 Lab Tasks

### Task 1 — Import the SQLite3 Module

```python
import sqlite3
```

The `sqlite3` module is included with Python's Standard Library.

---

### Task 2 — Connect to an SQLite Database

For this lab, use an in-memory database.

```python
connection = sqlite3.connect(':memory:')
```

`:memory:` creates a temporary database in RAM.

The database is discarded when the program ends.

### Key Concept — In-Memory Database

In-memory databases can be useful for:

- Testing.
- Temporary data.
- Fast read/write operations.
- Demonstrations and experiments.

---

### Task 3 — Create a Table

Create a cursor and execute a SQL `CREATE TABLE` statement.

```python
cursor = connection.cursor()

cursor.execute("""
CREATE TABLE students (
    id INTEGER PRIMARY KEY,
    name TEXT NOT NULL,
    grade REAL
)
""")
```

The `students` table contains:

| Column | Type | Purpose |
|---|---|---|
| `id` | INTEGER | Unique student identifier |
| `name` | TEXT | Student name |
| `grade` | REAL | Student grade |

### Technical Term — Cursor

A cursor is an object used to execute SQL queries and retrieve results from a database.

---

### Task 4 — Insert Rows into the Table

Create student records.

```python
students_data = [
    (1, 'Alice', 85.5),
    (2, 'Bob', 78.0),
    (3, 'Charlie', 92.0)
]

cursor.executemany(
    "INSERT INTO students VALUES (?, ?, ?)",
    students_data
)

connection.commit()
```

`executemany()` inserts multiple records efficiently.

`commit()` saves the changes to the database.

### 🔐 Security Note

The SQL statement uses placeholders:

```text
?
```

This demonstrates parameterized SQL rather than constructing SQL statements by directly combining user-controlled values into a query.

Parameterized queries are an important technique for reducing SQL injection risk.

---

### Task 5 — Query the Table

Retrieve all records.

```python
cursor.execute("SELECT * FROM students")
results = cursor.fetchall()
```

`SELECT` retrieves records from the database.

`fetchall()` returns all retrieved rows.

---

### Task 6 — Fetch and Display Results

Iterate through the results.

```python
for row in results:
    print(row)
```

The records should represent the students inserted into the table.

Example output:

```text
(1, 'Alice', 85.5)
(2, 'Bob', 78.0)
(3, 'Charlie', 92.0)
```

---

## 🔬 Complete Example

```python
import sqlite3


# Connect to an in-memory SQLite database
connection = sqlite3.connect(':memory:')

# Create a cursor
cursor = connection.cursor()

# Create students table
cursor.execute("""
CREATE TABLE students (
    id INTEGER PRIMARY KEY,
    name TEXT NOT NULL,
    grade REAL
)
""")

# Insert student records
students_data = [
    (1, 'Alice', 85.5),
    (2, 'Bob', 78.0),
    (3, 'Charlie', 92.0)
]

cursor.executemany(
    "INSERT INTO students VALUES (?, ?, ?)",
    students_data
)

# Save changes
connection.commit()

# Query the table
cursor.execute("SELECT * FROM students")
results = cursor.fetchall()

# Display results
for row in results:
    print(row)
```

---

## 🧠 Key Concepts

### Database Connection

The connection represents communication between the Python application and the SQLite database.

### Cursor

The cursor is used to execute SQL statements and retrieve results.

### Table

A table stores structured records using rows and columns.

### SQL Query

SQL (Structured Query Language) is used to interact with relational databases.

### `commit()`

`commit()` saves database changes.

### `fetchall()`

`fetchall()` retrieves all rows returned by a query.

### `executemany()`

`executemany()` allows the same SQL operation to be executed for multiple sets of values.

---

## 🛡️ Cybersecurity Perspective

Databases are commonly used by cybersecurity tools and applications to store structured information.

Examples include:

- Security events.
- Asset information.
- Scan results.
- Alert records.
- User information.
- Investigation data.
- Automation results.

The use of parameterized queries is especially important in security-sensitive applications because SQL injection is a major class of application-security vulnerability.

---

## 📸 Evidence / Screenshots

Useful evidence includes:

- SQLite Python code.
- Database table creation.
- Insert operation.
- Terminal output showing retrieved records.
- Successful SQL query execution.

Suggested structure:

```text
30-basic-sqlite-usage/
├── README.md
└── screenshots/
    ├── sqlite-code.png
    └── sqlite-output.png
```

---

## ⚠️ Best Practices

- Use parameterized queries when inserting external values.
- Avoid constructing SQL queries through unsafe string concatenation.
- Commit database changes when appropriate.
- Close database connections when working with persistent applications.
- Validate data before storing it.
- Keep database credentials and sensitive information out of source code when applicable.

---

## 🧠 Self-Check

1. What is SQLite?
2. What does `sqlite3.connect()` do?
3. What is an in-memory database?
4. What is a cursor?
5. What does `CREATE TABLE` do?
6. What does `executemany()` do?
7. Why is `commit()` used?
8. What does `SELECT` do?
9. What does `fetchall()` return?
10. Why are parameterized queries important for security?

---

## ✅ Completion Checklist

- [ ] Imported `sqlite3`.
- [ ] Created an SQLite connection.
- [ ] Created a cursor.
- [ ] Created the `students` table.
- [ ] Inserted student records.
- [ ] Used `commit()`.
- [ ] Executed a `SELECT` query.
- [ ] Retrieved records with `fetchall()`.
- [ ] Displayed the results.
- [ ] Understand parameterized SQL.
- [ ] Captured useful evidence.

---

## 🏁 Conclusion

In this lab, you learned the fundamentals of using SQLite with Python.

You established a database connection, created a table, inserted records, executed a query, and retrieved the stored data.

This provides a foundation for more advanced database-driven Python applications.

---

## 🎉 Section 06 Complete

You have now completed:

- Lab 28 — Multithreading Basics
- Lab 29 — Multiprocessing Basics
- Lab 30 — Basic SQLite Usage

The next section moves into practical Python tools for command-line applications, logging, web scraping, and file-management automation.

---

## ➡️ Next Section

**Section 07 — CLI, Logging & Automation**
