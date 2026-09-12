# 🧬 Lab 18 — OOP: Inheritance Basics

## 🎯 Objective

Learn how inheritance allows one Python class to reuse and extend the functionality of another class.

By completing this lab, you will learn how to:

- Create a parent class.
- Create a child class.
- Inherit attributes and methods.
- Extend a parent class.
- Add new behavior to a child class.
- Understand basic code reuse through inheritance.

---

## 📚 Prerequisites

Before starting this lab, you should understand:

- Classes and objects.
- Constructors.
- Attributes.
- Methods.
- Basic Python syntax.

It is recommended to complete **Lab 17 — OOP: Defining Classes** first.

---

## 🧠 Key Concepts

### Inheritance

Inheritance allows a child class to acquire attributes and methods from a parent class.

Basic structure:

```text
Parent Class
     │
     ▼
Child Class
```

---

### Parent Class

The parent class contains functionality that can be reused by other classes.

---

### Child Class

The child class inherits functionality from the parent and can add or modify behavior.

---

# 🧪 Practical Lab

## Task 1 — Create a Parent Class

Create:

```text
inheritance_example.py
```

Define a parent class:

```python
class Animal:
    def __init__(self, name):
        self.name = name

    def speak(self):
        print(f"{self.name} makes a sound.")
```

---

## Task 2 — Create a Child Class

Create a child class that inherits from `Animal`:

```python
class Dog(Animal):
    def speak(self):
        print(f"{self.name} says Woof!")
```

The `Dog` class inherits from `Animal` while providing its own implementation of `speak()`.

---

## Task 3 — Create an Object

Create a `Dog` object:

```python
dog = Dog("Buddy")
```

Call the inherited/overridden method:

```python
dog.speak()
```

Expected output:

```text
Buddy says Woof!
```

---

## Task 4 — Add Another Child Class

Create another class:

```python
class Cat(Animal):
    def speak(self):
        print(f"{self.name} says Meow!")
```

Create an object:

```python
cat = Cat("Milo")
cat.speak()
```

Expected output:

```text
Milo says Meow!
```

---

## 🔎 What You Practiced

This lab demonstrated:

- Parent classes.
- Child classes.
- Inheritance.
- Method overriding.
- Code reuse.
- Specialized child-class behavior.

---

## 🧠 Inheritance Structure

The example can be represented as:

```text
             Animal
              │
       ┌──────┴──────┐
       │             │
      Dog           Cat
       │             │
     speak()       speak()
```

Both `Dog` and `Cat` inherit from `Animal`.

---

## 🛡️ Cybersecurity Perspective

Inheritance can help organize cybersecurity applications containing related objects.

For example:

```text
SecurityEvent
     │
 ┌───┴──────────┐
 │              │
LoginEvent   NetworkEvent
```

A shared parent class can contain common attributes or behavior, while specialized classes can implement event-specific functionality.

This can improve code reuse and organization in larger security projects.

---

## 📸 Evidence

Recommended evidence:

- Parent class definition.
- Child class definition.
- Successful object creation.
- Overridden method output.
- Multiple child classes executing.

---

## ⚠️ Best Practice

Inheritance should be used when there is a clear relationship between classes.

Do not create inheritance relationships simply to make code more complicated. Prefer a structure that makes the application's behavior easier to understand.

---

## 📝 Self-Check

- [ ] Can I define a parent class?
- [ ] Can I create a child class?
- [ ] Do I understand inheritance?
- [ ] Can I override a method?
- [ ] Can I explain why inheritance supports code reuse?

---

## ✅ Completion Checklist

- [ ] Parent class created
- [ ] Child class created
- [ ] Inheritance implemented
- [ ] Method overridden
- [ ] Multiple child classes tested
- [ ] Output verified
- [ ] Evidence added where useful

---

## 🏁 Conclusion

This lab introduced inheritance in Python and demonstrated how child classes can reuse and extend functionality from parent classes.

Inheritance is an important OOP concept for organizing related objects and reducing unnecessary duplication.

---

## 🚀 Next Lab

**Lab 19 — Basic Recursion Example**
