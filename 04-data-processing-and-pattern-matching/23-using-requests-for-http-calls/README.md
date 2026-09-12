# Lab 23 — Using Requests for HTTP Calls

> Learn how to make HTTP requests with Python, inspect response status codes, and parse JSON data returned by web APIs.

---

## 🎯 Objective

By completing this lab, you will learn how to:

- Use the Python `requests` library
- Make HTTP GET requests
- Understand HTTP response objects
- Inspect HTTP status codes
- Parse JSON responses
- Understand basic API interaction
- Work with data returned by a web service

---

## 📚 Prerequisites

Before starting this lab, you should have:

- Basic Python programming knowledge
- Python 3.x installed
- Basic understanding of variables and functions
- Internet connectivity
- Basic understanding of JSON

Recommended previous labs:

- **Lab 14 — JSON Handling**
- **Lab 16 — Virtual Environments (venv)**

---

# 1. Introduction to HTTP Requests

Applications frequently communicate with remote services over HTTP.

Python can interact with web services by sending HTTP requests.

Common HTTP methods include:

- `GET` — retrieve data
- `POST` — submit data
- `PUT` — update data
- `DELETE` — remove data

This lab focuses on the **GET** method.

---

# 2. Task 1 — Set Up the Requests Library

The original lab uses the `requests` library.

Install it with:

```bash
pip install requests
```

> **Recommendation:** Since this repository includes a virtual-environment lab, use the virtual environment from **Lab 16** when installing third-party Python packages.

Import the library:

```python
import requests
```

---

# 3. Task 2 — Make a Basic HTTP GET Request

The original exercise uses the GitHub API endpoint:

```text
https://api.github.com
```

Create a Python file such as:

```text
http_request.py
```

Add:

```python
import requests

response = requests.get("https://api.github.com")

print(response.status_code)
```

The `requests.get()` function sends an HTTP GET request.

The resulting `response` object contains information returned by the server.

---

# 4. Understanding the Response

The response object provides information about the HTTP request.

One important property is:

```python
response.status_code
```

It represents the HTTP status code returned by the server.

Common examples include:

| Status Code | Meaning |
|---|---|
| `200` | OK |
| `404` | Not Found |
| `500` | Internal Server Error |

For this lab, a successful request should normally return a `200` response.

---

# 5. Task 3 — Parse JSON Response Data

Many APIs return information in JSON format.

The `requests` response object provides:

```python
response.json()
```

to parse JSON into Python data structures.

Example:

```python
import requests

response = requests.get("https://api.github.com")

response_data = response.json()

print(response_data)
```

The resulting object can be processed as a Python dictionary.

---

# 6. Inspect the Returned Data

You can inspect the type of the returned data:

```python
import requests

response = requests.get("https://api.github.com")

response_data = response.json()

print("Status code:", response.status_code)
print("Data type:", type(response_data))
print("Response data:", response_data)
```

This helps demonstrate the relationship between:

```text
HTTP API
   ↓
HTTP Response
   ↓
JSON
   ↓
Python Dictionary
```

---

# 7. A More Structured Example

A simple version combining the main tasks:

```python
import requests

response = requests.get("https://api.github.com")

print("Status code:", response.status_code)

response_data = response.json()

print("Response data:")
print(response_data)
```

This demonstrates the core workflow from the original lab.

---

# 8. API Data Analysis

The original exercise introduces the idea of identifying useful information from JSON returned by an API.

Once JSON has been converted into a Python dictionary, you can inspect its keys:

```python
import requests

response = requests.get("https://api.github.com")

response_data = response.json()

print("Available keys:")

for key in response_data:
    print(key)
```

This is useful when learning an unfamiliar API response structure.

---

# 🧠 Key Concepts

### `requests.get()`

Sends an HTTP GET request.

```python
response = requests.get("https://api.github.com")
```

### Response object

Contains information returned by the server.

```python
response
```

### HTTP status code

Indicates the result of the request.

```python
response.status_code
```

### JSON parsing

Converts JSON response data into Python objects.

```python
response.json()
```

---

# 🛡️ Security Perspective

HTTP and APIs are fundamental to modern cybersecurity.

Security professionals frequently work with:

- REST APIs
- Security platforms
- SIEM APIs
- Cloud APIs
- Threat-intelligence APIs
- Monitoring systems
- Authentication services
- Automated security workflows

Python can be used to retrieve data from authorized APIs and process it automatically.

For example, a security automation workflow might conceptually look like:

```text
Security API
     ↓
HTTP Request
     ↓
JSON Response
     ↓
Python Processing
     ↓
Security Analysis / Automation
```

Understanding HTTP status codes is also important when troubleshooting API integrations.

> **Security rule:** Only interact with systems and APIs that you are authorized to use. This lab uses a public API endpoint for learning.

---

# 📸 Evidence / Screenshots

Useful screenshots include:

- Successful installation of `requests`
- Python script execution
- HTTP status code
- JSON response
- API response keys

Suggested structure:

```text
23-using-requests-for-http-calls/
├── README.md
├── http_request.py
└── screenshots/
    ├── status-code.png
    └── api-response.png
```

Do not capture or publish API keys, authentication tokens, cookies, or other sensitive information.

---

# ⚠️ Best Practices

- Use a virtual environment for third-party packages.
- Check HTTP status codes.
- Do not blindly trust remote data.
- Handle network failures in production applications.
- Avoid exposing credentials or API tokens.
- Only access APIs you are authorized to use.
- Avoid sending unnecessary requests to remote services.

---

# 📝 Self-Check

1. What is an HTTP GET request?
2. What does the `requests` library provide?
3. What does `response.status_code` represent?
4. What does HTTP status code `200` mean?
5. What does `404` indicate?
6. What does `response.json()` do?
7. Why are APIs important in cybersecurity?
8. Why should API credentials never be committed to GitHub?
9. Why should API access be limited to authorized systems?

---

# ✅ Lab Completion Checklist

- [ ] I installed the `requests` library.
- [ ] I imported `requests`.
- [ ] I made an HTTP GET request.
- [ ] I inspected the response status code.
- [ ] I parsed JSON response data.
- [ ] I inspected the returned dictionary.
- [ ] I understand basic API interaction.
- [ ] I understand the cybersecurity relevance of APIs.
- [ ] I completed the practical exercise.
- [ ] I captured useful execution evidence.

---

# 📌 Conclusion

In this lab, you learned how to use Python's `requests` library to communicate with a web API.

You practiced:

- Installing and importing a library
- Making HTTP GET requests
- Reading HTTP status codes
- Parsing JSON responses
- Inspecting API data

These concepts provide a foundation for building Python automation and security tools that interact with authorized web APIs.

---

## 🚀 Next Lab

**Lab 24 — Basic Regular Expressions**
