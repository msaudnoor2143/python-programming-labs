# 📁 Lab 34 — Simple Scripting for File Management

This lab introduces Python-based file-management automation using the `os` and `shutil` modules.

You will learn how to list files, create destination directories, copy files, and optionally rename files during the copying process.

---

## 🎯 Objective

By completing this lab, you will:

- Understand basic file management using Python scripts.
- List files in a directory.
- Copy files using Python.
- Create directories programmatically.
- Rename files while copying.
- Understand the benefits of automated file management.

---

## 📚 Prerequisites

- Basic Python programming knowledge.
- Python installed on your system.
- Familiarity with files and directories.
- Basic experience running Python scripts.

---

## 🧠 Introduction

Python can automate repetitive file-management operations.

Instead of manually performing the same operation on many files, a script can perform the operation repeatedly and consistently.

This can improve:

- Automation.
- Scalability.
- Accuracy.
- Customization.

---

## 🧰 Required Modules

This lab uses:

```python
import os
import shutil
```

`os` provides operating-system and filesystem functionality.

`shutil` provides high-level file operations such as copying files.

---

## 🧪 Task 1 — Import Required Modules

```python
import os
import shutil
```

---

## 📂 Task 2 — List Files in a Folder

Use `os.listdir()` to retrieve the contents of a directory.

```python
directory = 'path/to/source/folder'

files = os.listdir(directory)

print("Files in Directory:", files)
```

Replace the example directory path with the folder you want to process.

---

## 📁 Task 3 — Create a Destination Directory

Define the destination directory.

```python
destination = 'path/to/destination/folder'

if not os.path.exists(destination):
    os.makedirs(destination)
```

The script checks whether the destination exists.

If it does not exist, `os.makedirs()` creates it.

---

## 📋 Task 4 — Copy Files

Use `shutil.copy()` to copy the files.

```python
for file in files:
    shutil.copy(
        os.path.join(directory, file),
        destination
    )
```

`os.path.join()` creates the appropriate path to the source file.

`shutil.copy()` copies the file to the destination.

---

## ✏️ Task 5 — Optional File Renaming

The script can also rename files while copying them.

For demonstration, append `_backup` to each filename.

```python
for file in files:
    base, extension = os.path.splitext(file)

    new_name = f"{base}_backup{extension}"

    shutil.copy(
        os.path.join(directory, file),
        os.path.join(destination, new_name)
    )
```

For example:

```text
report.txt
```

can become:

```text
report_backup.txt
```

---

## 🔬 Complete Example

```python
import os
import shutil


directory = 'path/to/source/folder'
destination = 'path/to/destination/folder'


# Create destination directory if necessary
if not os.path.exists(destination):
    os.makedirs(destination)


# List files
files = os.listdir(directory)

print("Files in Directory:", files)


# Copy files
for file in files:
    shutil.copy(
        os.path.join(directory, file),
        destination
    )


# Optional: copy files with "_backup" added to the filename
for file in files:
    base, extension = os.path.splitext(file)

    new_name = f"{base}_backup{extension}"

    shutil.copy(
        os.path.join(directory, file),
        os.path.join(destination, new_name)
    )
```

---

## 🧠 Advantages of Script-Based File Management

### Automation

Write the process once and run it repeatedly.

This reduces repetitive manual work.

### Scalability

Scripts can be adapted to process large numbers of files.

### Accuracy

Automated operations can reduce human error during repetitive tasks.

### Customization

Python allows additional logic such as:

- Conditional processing.
- Logging.
- File filtering.
- Custom naming.
- Additional automation.

---

## 🛡️ Cybersecurity Perspective

File-management automation is useful in cybersecurity workflows.

Examples include:

- Organizing security logs.
- Processing collected evidence.
- Creating backups of security data.
- Moving files into structured directories.
- Automating repetitive administrative tasks.

However, scripts that modify files should be tested carefully to avoid accidentally copying, renaming, or modifying the wrong data.

---

## 📸 Evidence / Screenshots

Capture meaningful evidence such as:

- Source directory contents.
- Python script.
- Destination directory.
- Copied files.
- Renamed backup files.

Suggested structure:

```text
34-simple-scripting-for-file-management/
├── README.md
└── screenshots/
    ├── source-files.png
    ├── file-management-code.png
    └── destination-files.png
```

---

## ⚠️ Best Practices

- Test scripts on non-critical files first.
- Verify source and destination paths.
- Avoid running destructive file operations without checking the target.
- Use clear directory paths.
- Add logging when automating important file operations.
- Validate which files are being processed.

---

## 🧠 Self-Check

1. What is the purpose of the `os` module?
2. What is the purpose of `shutil`?
3. What does `os.listdir()` return?
4. What does `os.makedirs()` do?
5. What does `shutil.copy()` do?
6. Why is `os.path.join()` useful?
7. What does `os.path.splitext()` return?
8. What are the benefits of automating file management?

---

## ✅ Completion Checklist

- [ ] Imported `os`.
- [ ] Imported `shutil`.
- [ ] Listed files in a directory.
- [ ] Created a destination directory.
- [ ] Copied files.
- [ ] Tested file renaming.
- [ ] Verified the destination files.
- [ ] Captured useful evidence.
- [ ] Reviewed file-management safety practices.

---

## 🏁 Conclusion

In this lab, you explored how Python's `os` and `shutil` modules can automate common file-management operations.

You learned how to list files, create directories, copy files, and optionally rename files while copying them.

These techniques provide a foundation for more advanced automation tasks.

---

## 🎉 Section 07 Complete

You have now completed:

- Lab 31 — CLI Applications with `argparse`
- Lab 32 — Logging with Python's Logging Module
- Lab 33 — Basic Web Scraping with `requests` + BeautifulSoup
- Lab 34 — Simple Scripting for File Management

---

## ➡️ Next Section

**Section 08 — Data Visualization & Data Structures**

Labs:

- Lab 35 — Quick Data Visualization with matplotlib
- Lab 36 — Using Collections (`deque`, `Counter`)
