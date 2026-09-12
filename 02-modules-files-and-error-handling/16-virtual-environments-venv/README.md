# 🧪 Lab 16 — Virtual Environments (venv)

## 🎯 Objective

Understand how Python virtual environments isolate project dependencies and provide controlled development environments.

By completing this lab, you will learn how to:

- Create a virtual environment.
- Activate a virtual environment.
- Install packages inside an environment.
- Verify installed packages.
- Deactivate a virtual environment.
- Understand dependency isolation.

---

## 📚 Prerequisites

Before starting this lab, you should have:

- Basic Python knowledge.
- Familiarity with the command line.
- Python 3.3 or later installed.

---

## 🧠 Key Concepts

### Virtual Environment

A virtual environment is an isolated Python environment containing its own Python executable, libraries, and scripts for a project.

---

### Isolation

Virtual environments allow different projects to maintain separate dependencies.

For example:

```text
Project A
└── Environment A
    └── Package Version A

Project B
└── Environment B
    └── Package Version B
```

This reduces dependency conflicts between projects.

---

# 🧪 Practical Lab

## Task 1 — Create a Project Directory

Create a practice directory:

```bash
mkdir my_project
cd my_project
```

---

## Task 2 — Create a Virtual Environment

Create an environment using Python's `venv` module:

```bash
python -m venv myenv
```

This creates:

```text
my_project/
└── myenv/
```

The `myenv` directory contains the files required for the isolated environment.

---

## Task 3 — Activate the Environment

### Linux/macOS

```bash
source myenv/bin/activate
```

### Windows

```powershell
.\myenv\Scripts\activate
```

After activation, the environment name will normally appear in the terminal prompt:

```text
(myenv)
```

---

## Task 4 — Install a Package

With the virtual environment active, install `requests`:

```bash
pip install requests
```

Verify installed packages:

```bash
pip list
```

The installed `requests` package should appear in the package list.

---

## Task 5 — Deactivate the Environment

When finished, deactivate the environment:

```bash
deactivate
```

The environment indicator should disappear from the terminal prompt.

---

## 🔎 Virtual Environment Workflow

```text
Create Project
      │
      ▼
Create venv
      │
      ▼
Activate Environment
      │
      ▼
Install Dependencies
      │
      ▼
Develop / Test
      │
      ▼
Deactivate
```

---

## 🧠 Why Virtual Environments Matter

Consider two projects:

```text
Project A
requests == 2.25.1

Project B
requests == 2.26.0
```

Using isolated environments allows each project to maintain its own dependency requirements without forcing both projects to use the same package version.

---

## 🛡️ Cybersecurity Perspective

Virtual environments are important when developing cybersecurity tools because different projects may require different Python libraries or versions.

Examples include:

- Security automation tools.
- API clients.
- Log-processing applications.
- Cloud security scripts.
- Detection engineering utilities.
- Security research projects.

Isolation helps prevent dependencies from different projects from interfering with one another.

---

## 📸 Evidence

Recommended evidence:

- Virtual environment creation.
- Activated environment shown in the terminal.
- `pip install requests` result.
- `pip list` showing the installed package.
- Successful deactivation.

---

## ⚠️ Best Practices

When working with project environments:

- Keep dependencies isolated per project.
- Avoid unnecessarily installing project-specific packages globally.
- Document project dependencies.
- Do not commit the virtual environment directory to GitHub.

A typical Git repository should generally exclude the environment itself.

---

## 📝 Self-Check

- [ ] Can I create a virtual environment?
- [ ] Can I activate it?
- [ ] Can I install a package inside it?
- [ ] Can I verify installed packages?
- [ ] Can I deactivate it?
- [ ] Can I explain dependency isolation?
- [ ] Do I understand why virtual environments are useful?

---

## ✅ Completion Checklist

- [ ] Project directory created
- [ ] Virtual environment created
- [ ] Environment activated
- [ ] `requests` installed
- [ ] Package installation verified
- [ ] Environment deactivated
- [ ] Dependency isolation understood
- [ ] Evidence added where useful

---

## 🏁 Conclusion

This lab introduced Python virtual environments using `venv`.

Virtual environments provide project-level dependency isolation and are an important part of maintaining reliable Python development environments.

---

## 🚀 Section 02 Complete

You have now completed:

- **Lab 11 — Modules & Packages**
- **Lab 12 — File I/O Basics**
- **Lab 13 — Handling Exceptions**
- **Lab 14 — JSON Handling**
- **Lab 15 — Basic Debugging Techniques**
- **Lab 16 — Virtual Environments (venv)**

Next:

**Section 03 — Object-Oriented & Functional Python**
