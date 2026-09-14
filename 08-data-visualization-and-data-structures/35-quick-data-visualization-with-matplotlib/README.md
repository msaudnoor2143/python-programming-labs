# 📈 Lab 35 — Quick Data Visualization with matplotlib

This lab introduces the basics of data visualization using Python's `matplotlib` library.

You will install matplotlib, define sample data, create a simple line graph, and customize the visualization with a title and axis labels.

---

## 🎯 Objective

By completing this lab, you will:

- Understand the basics of data visualization using matplotlib.
- Learn how to install and set up matplotlib.
- Create simple plots using matplotlib.
- Add titles and axis labels.
- Understand the benefits of quick data visualization.

---

## 📚 Prerequisites

- Basic knowledge of Python programming.
- Python installed on your computer.
- `pip` installed.
- A basic text editor or IDE such as Visual Studio Code.

---

## 🧠 Introduction

Data visualization provides a graphical way to represent information.

Instead of examining values individually, a visualization can make trends and patterns easier to identify.

Python's `matplotlib` library provides tools for creating many different types of graphs and charts.

---

## 🧰 Task 1 — Install matplotlib

Install matplotlib using pip:

```bash
pip install matplotlib
```

Make sure your system has an internet connection when installing the package.

---

## 🐍 Task 2 — Import matplotlib

Create a Python script such as:

```text
quick_plot.py
```

Import the `pyplot` module:

```python
import matplotlib.pyplot as plt
```

`pyplot` provides a MATLAB-like interface for creating plots and graphs.

---

## 📊 Task 3 — Define Data

Create two lists containing sample data:

```python
# Sample data
x = [0, 1, 2, 3, 4, 5]
y = [0, 1, 4, 9, 16, 25]
```

Here:

- `x` represents the independent variable.
- `y` represents the dependent variable.

---

## 📈 Task 4 — Create a Basic Plot

Create a line graph:

```python
plt.plot(x, y)
```

---

## 🏷️ Task 5 — Customize the Plot

Add a title and labels:

```python
plt.title('Simple Line Plot')
plt.xlabel('X Axis Label')
plt.ylabel('Y Axis Label')
```

These labels make the visualization easier to understand.

---

## 🖥️ Task 6 — Display the Plot

Display the current figure:

```python
plt.show()
```

`plt.show()` opens the generated visualization.

---

## 🔬 Complete Example

```python
import matplotlib.pyplot as plt


# Sample data
x = [0, 1, 2, 3, 4, 5]
y = [0, 1, 4, 9, 16, 25]


# Create the plot
plt.plot(x, y)

# Customize the plot
plt.title('Simple Line Plot')
plt.xlabel('X Axis Label')
plt.ylabel('Y Axis Label')

# Display the plot
plt.show()
```

---

## 📌 Expected Result

The program should display a line graph representing the supplied `x` and `y` values.

The graph will show the increasing values:

```text
x: 0  1  2  3  4  5
y: 0  1  4  9 16 25
```

---

## 🧠 Why Quick Visualization Matters

Quick plots can help you:

- Visualize trends.
- Identify patterns.
- Compare datasets.
- Communicate results.
- Support data-driven decisions.

The clarity of a visualization can significantly affect how easily information is understood.

---

## 🛡️ Cybersecurity Perspective

Data visualization is highly useful in cybersecurity.

Security teams often work with large quantities of data, including:

- Authentication events.
- Network activity.
- System logs.
- Security alerts.
- Incident statistics.

Visualizing this information can make trends and unusual patterns easier to identify.

For example, a security analyst could visualize the number of security events recorded over time.

---

## 📸 Evidence / Screenshots

Capture meaningful evidence such as:

1. matplotlib installation.
2. Python source code.
3. Generated line graph.

Suggested structure:

```text
35-quick-data-visualization-with-matplotlib/
├── README.md
├── quick_plot.py
└── screenshots/
    ├── matplotlib-installation.png
    ├── visualization-code.png
    └── line-plot.png
```

The generated graph is particularly valuable evidence because it demonstrates the actual result of the lab.

---

## ⚠️ Best Practices

- Use meaningful titles.
- Label axes clearly.
- Keep visualizations easy to understand.
- Avoid unnecessary visual elements.
- Choose appropriate visualization types for the data.
- Verify that the displayed graph accurately represents the underlying data.

---

## 🧠 Self-Check

1. What is data visualization?
2. What is matplotlib?
3. What does `pyplot` provide?
4. What does `plt.plot()` do?
5. What does `plt.title()` do?
6. What do `plt.xlabel()` and `plt.ylabel()` do?
7. What does `plt.show()` do?
8. Why is visualization useful when analyzing data?

---

## ✅ Completion Checklist

- [ ] Installed matplotlib.
- [ ] Imported `matplotlib.pyplot`.
- [ ] Created sample `x` data.
- [ ] Created sample `y` data.
- [ ] Created a line plot.
- [ ] Added a title.
- [ ] Added axis labels.
- [ ] Displayed the visualization.
- [ ] Captured the generated graph.
- [ ] Reviewed cybersecurity applications.

---

## 🏁 Conclusion

In this lab, you learned how to quickly visualize data using matplotlib.

You progressed from installing the library to creating and customizing a simple line graph.

The lab demonstrates how visualizations can make trends and patterns easier to understand.

---

## ➡️ Next Lab

**Lab 36 — Using Collections (`deque`, `Counter`)**
