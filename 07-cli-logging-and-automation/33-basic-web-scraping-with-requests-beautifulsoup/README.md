# 🌐 Lab 33 — Basic Web Scraping with `requests` + BeautifulSoup

This lab introduces basic web scraping using Python's `requests` and BeautifulSoup libraries.

You will retrieve a webpage, parse its HTML, and extract information such as the page title and hyperlinks.

---

## 🎯 Objective

By completing this lab, you will:

- Understand basic web scraping.
- Retrieve webpages using `requests`.
- Parse HTML using BeautifulSoup.
- Extract specific information from HTML.
- Navigate basic HTML structures.

---

## 📚 Prerequisites

- Basic Python programming knowledge.
- Python installed on your system.
- Familiarity with running Python scripts.
- Basic knowledge of HTML is beneficial.

---

## 🧰 Required Packages

Install the required packages:

```bash
pip install beautifulsoup4 requests
```

Ensure your Python environment is active and has internet access.

---

## 🧪 Task 1 — Verify the Installation

Check the installed packages:

```bash
pip show beautifulsoup4 requests
```

Review the displayed package information and version numbers.

---

## 🌐 Task 2 — Fetch a Webpage

Import `requests` and send a GET request.

```python
import requests


# Send a GET request to the webpage
response = requests.get("https://example.com")

# Print the status code
print(response.status_code)
```

A successful request should return:

```text
200
```

A status code of `200` indicates a successful HTTP response.

---

## 🧪 Task 3 — Parse the HTML

Import BeautifulSoup and parse the webpage content.

```python
from bs4 import BeautifulSoup


# Parse the HTML content
soup = BeautifulSoup(response.text, 'html.parser')

# Display the structured content
print(soup.prettify())
```

BeautifulSoup parses the HTML and provides methods for navigating its structure.

`html.parser` is a built-in parser option suitable for basic HTML parsing.

---

## 🔎 Task 4 — Extract the Page Title

Extract the title from the parsed HTML.

```python
title = soup.title.string
print("Page Title:", title)
```

The page title provides a brief description of the webpage.

---

## 🔗 Task 5 — Extract Hyperlinks

Find all anchor tags.

```python
links = soup.find_all('a')

for link in links:
    print(link.get('href'))
```

The `href` attribute contains the destination associated with an anchor tag.

---

## 🔬 Complete Example

```python
import requests
from bs4 import BeautifulSoup


# Fetch the webpage
response = requests.get("https://example.com")

# Display HTTP status
print("Status Code:", response.status_code)

# Parse HTML
soup = BeautifulSoup(response.text, 'html.parser')

# Display structured HTML
print(soup.prettify())

# Extract page title
title = soup.title.string
print("Page Title:", title)

# Extract hyperlinks
links = soup.find_all('a')

for link in links:
    print(link.get('href'))
```

---

## 🧠 Key Concepts

### HTTP Request

`requests` can retrieve content from a web server.

### HTML Parsing

BeautifulSoup parses HTML documents.

### DOM Navigation

BeautifulSoup provides methods for navigating HTML elements.

### Information Extraction

Specific HTML elements and attributes can be extracted from the parsed document.

---

## 🛡️ Cybersecurity Perspective

Understanding HTTP requests and HTML parsing provides useful foundations for cybersecurity and security automation.

Possible applications include:

- Gathering information from permitted public webpages.
- Security-data collection.
- Automation.
- Web-content analysis.
- Processing publicly available information.

However, web scraping should always be performed responsibly.

---

## ⚠️ Responsible Scraping

Always:

- Respect a website's Terms of Service.
- Check and respect `robots.txt` where applicable.
- Avoid unnecessary request volume.
- Do not attempt to bypass authentication or access controls.
- Only collect information you are permitted to access.

---

## 📸 Evidence / Screenshots

Capture:

- Package installation/verification.
- HTTP status code.
- Parsed HTML.
- Extracted page title.
- Extracted hyperlinks.

Suggested structure:

```text
33-basic-web-scraping-with-requests-beautifulsoup/
├── README.md
└── screenshots/
    ├── package-verification.png
    ├── request-output.png
    └── scraping-output.png
```

---

## 🧠 Self-Check

1. What is web scraping?
2. What is the purpose of `requests`?
3. What does `BeautifulSoup` do?
4. What does an HTTP status code of `200` indicate?
5. What does `soup.title` represent?
6. What does `find_all('a')` return?
7. What is the purpose of the `href` attribute?
8. Why should web scraping be performed responsibly?

---

## ✅ Completion Checklist

- [ ] Installed `beautifulsoup4`.
- [ ] Installed/verified `requests`.
- [ ] Retrieved a webpage.
- [ ] Checked the HTTP status code.
- [ ] Parsed the HTML.
- [ ] Extracted the page title.
- [ ] Extracted hyperlinks.
- [ ] Captured useful evidence.
- [ ] Reviewed responsible scraping practices.

---

## 🏁 Conclusion

In this lab, you learned the basics of web scraping using `requests` and BeautifulSoup.

You retrieved a webpage, parsed its HTML, extracted the page title, and collected hyperlinks.

These techniques provide a foundation for more advanced web-data processing and automation.

---

## ➡️ Next Lab

**Lab 34 — Simple Scripting for File Management**
