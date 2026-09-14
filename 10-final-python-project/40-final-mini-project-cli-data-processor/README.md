# 🚀 Lab 40 — Final Mini-Project: Building a CLI Data Processor

This final lab combines several Python concepts into a practical command-line application.

The project fetches JSON data from an API, validates the response, saves the data to a file, accepts command-line arguments, logs progress, and handles possible errors.

---

## 🎯 Objective

By completing this lab, you will:

- Fetch data from an API using Python.
- Process JSON responses.
- Save JSON data to a file.
- Implement command-line arguments.
- Use Python logging.
- Handle exceptions.
- Validate JSON data.
- Combine multiple Python modules into one practical application.

---

## 📚 Prerequisites

You should have:

- Basic Python programming knowledge.
- Familiarity with command-line interfaces.
- Python 3.x installed.
- Internet access for API requests.
- Understanding of functions, JSON, exceptions, and modules.

---

# 🏗️ Project Overview

The application follows this workflow:

```text
Command-Line Arguments
          │
          ▼
      API URL
          │
          ▼
     Fetch API Data
          │
          ▼
   Validate HTTP Response
          │
          ▼
      Parse JSON
          │
          ▼
      Save JSON File
          │
          ▼
        Logging
```

---

# 🧪 Task 1 — Setting Up the Environment

## Install `requests`

The project uses the `requests` library to communicate with APIs.

```bash
pip install requests
```

---

## Create the Python File

Create:

```text
data_processor.py
```

Recommended structure:

```text
40-final-mini-project-cli-data-processor/
├── README.md
├── data_processor.py
└── screenshots/
```

---

# 🌐 Task 2 — Fetching Data from an API

Import the required modules:

```python
import requests
import json
import argparse
import logging
```

Create a function for fetching API data:

```python
def fetch_data(api_url):
    try:
        response = requests.get(api_url)
        response.raise_for_status()
        data = response.json()
        return data
    except requests.exceptions.HTTPError as http_err:
        logging.error(f"HTTP error occurred: {http_err}")
    except Exception as err:
        logging.error(f"Other error occurred: {err}")
```

### How It Works

The function:

1. Receives an API URL.
2. Sends an HTTP GET request.
3. Checks whether the request was successful.
4. Converts the response into JSON.
5. Returns the resulting data.
6. Logs errors when something goes wrong.

---

# 💾 Task 3 — Saving JSON to a File

Create a function for saving the retrieved data:

```python
def save_data_to_file(data, file_path):
    try:
        with open(file_path, 'w') as json_file:
            json.dump(data, json_file, indent=4)
        logging.info(f"Data successfully saved to {file_path}")
    except Exception as e:
        logging.error(f"Error saving data: {e}")
```

### Key Concept

```python
json.dump()
```

writes Python data to a JSON file.

The following option:

```python
indent=4
```

formats the JSON so that it is easier to read.

---

# 🖥️ Task 4 — Implementing CLI Arguments

Create a function to process command-line arguments:

```python
def parse_arguments():
    parser = argparse.ArgumentParser(description='CLI Data Processor')

    parser.add_argument(
        '--api_url',
        type=str,
        required=True,
        help='API URL to fetch data from'
    )

    parser.add_argument(
        '--file_path',
        type=str,
        required=True,
        help='Path to save JSON data'
    )

    return parser.parse_args()
```

The application now accepts two required arguments:

```text
--api_url
--file_path
```

This allows the same program to process different APIs and output files without changing the Python source code.

---

# 📝 Task 5 — Logging Progress

Configure logging:

```python
logging.basicConfig(
    level=logging.INFO,
    format='%(asctime)s - %(levelname)s - %(message)s'
)
```

Logging provides information about the application's execution.

Example message types include:

```text
INFO
ERROR
WARNING
DEBUG
CRITICAL
```

For this project, the logging configuration uses:

```text
INFO
```

as the minimum logging level.

---

# 🧩 Task 6 — Main Function Implementation

Combine the different components:

```python
if __name__ == '__main__':
    args = parse_arguments()

    logging.info("Started fetching data...")

    data = fetch_data(args.api_url)

    if data:
        save_data_to_file(data, args.file_path)
```

The main workflow is now:

```text
Parse arguments
      ↓
Log process start
      ↓
Fetch API data
      ↓
Check returned data
      ↓
Save JSON data
```

---

# ✅ Task 7 — Validating JSON Data

JSON validation is handled during the API response processing:

```python
data = response.json()
```

If the response cannot be processed as JSON, the exception handling mechanism can capture the resulting error.

This prevents the application from assuming that every response contains valid JSON.

---

# 🧪 Complete Project

The complete implementation based on the lab tasks is:

```python
import requests
import json
import argparse
import logging


def fetch_data(api_url):
    try:
        response = requests.get(api_url)
        response.raise_for_status()
        data = response.json()
        return data

    except requests.exceptions.HTTPError as http_err:
        logging.error(f"HTTP error occurred: {http_err}")

    except Exception as err:
        logging.error(f"Other error occurred: {err}")


def save_data_to_file(data, file_path):
    try:
        with open(file_path, 'w') as json_file:
            json.dump(data, json_file, indent=4)

        logging.info(f"Data successfully saved to {file_path}")

    except Exception as e:
        logging.error(f"Error saving data: {e}")


def parse_arguments():
    parser = argparse.ArgumentParser(
        description='CLI Data Processor'
    )

    parser.add_argument(
        '--api_url',
        type=str,
        required=True,
        help='API URL to fetch data from'
    )

    parser.add_argument(
        '--file_path',
        type=str,
        required=True,
        help='Path to save JSON data'
    )

    return parser.parse_args()


logging.basicConfig(
    level=logging.INFO,
    format='%(asctime)s - %(levelname)s - %(message)s'
)


if __name__ == '__main__':
    args = parse_arguments()

    logging.info("Started fetching data...")

    data = fetch_data(args.api_url)

    if data:
        save_data_to_file(data, args.file_path)
```

---

# 🖥️ Running the Application

The application requires both arguments:

```bash
python data_processor.py --api_url "API_URL" --file_path "output.json"
```

The exact API URL used can depend on the API available during testing.

---

# 🔎 Understanding the Components

| Component | Purpose |
|---|---|
| `requests` | Fetches data over HTTP |
| `json` | Processes and saves JSON |
| `argparse` | Handles CLI arguments |
| `logging` | Records application activity |
| `try/except` | Handles errors |
| `response.raise_for_status()` | Checks HTTP request success |
| `response.json()` | Converts response data to JSON |
| `json.dump()` | Writes JSON to a file |

---

# 🛡️ Cybersecurity Perspective

This project demonstrates several concepts that are useful in cybersecurity and cloud environments.

### API Security

Security applications frequently communicate with APIs to retrieve information such as:

- Security events
- Monitoring data
- Alerts
- Asset information
- Service status

### Logging

Logging provides useful information for:

- Troubleshooting
- Monitoring
- Auditing
- Incident investigation

### Exception Handling

Error handling helps applications deal with unexpected conditions in a controlled manner.

### Automation

A CLI data processor can serve as a foundation for automation scripts used in system administration, cloud environments, and security operations.

---

# ⚠️ Best Practices

When adapting this project for real-world use:

- Validate external input.
- Handle network failures.
- Avoid exposing sensitive information in logs.
- Use secure API endpoints.
- Protect API credentials.
- Avoid hard-coding secrets.
- Validate data received from external sources.
- Use appropriate timeouts for production HTTP requests.

---

# 📸 Evidence & Screenshots

Recommended screenshots:

### 1. Successful Execution

Show the CLI command and logging output.

```text
Started fetching data...
Data successfully saved to output.json
```

### 2. Generated JSON

Show the resulting JSON file and its contents.

### 3. Error Handling

Show an appropriate error being logged when the API request fails.

Store evidence inside:

```text
screenshots/
```

Example:

```text
screenshots/
├── successful-run.png
├── saved-json.png
└── error-handling.png
```

Screenshots should demonstrate actual project functionality.

---

# 🧠 Self-Check

Before completing the lab, make sure you understand:

- [ ] What does `requests.get()` do?
- [ ] Why is `response.raise_for_status()` used?
- [ ] What does `response.json()` do?
- [ ] How does `json.dump()` save data?
- [ ] Why are `argparse` arguments useful?
- [ ] What information does logging provide?
- [ ] Why is exception handling important?
- [ ] How does the program determine where to save the JSON file?
- [ ] Why should externally received data be treated carefully?

---

# ✅ Completion Checklist

- [ ] `requests` installed
- [ ] `data_processor.py` created
- [ ] API fetching implemented
- [ ] HTTP errors handled
- [ ] JSON processing implemented
- [ ] JSON saving implemented
- [ ] CLI arguments implemented
- [ ] Logging configured
- [ ] Exception handling implemented
- [ ] Application tested
- [ ] JSON output verified
- [ ] Evidence screenshots added
- [ ] README completed

---

# 🏁 Conclusion

You have completed the final Python lab by building a command-line data processor capable of:

- Fetching data from an API
- Handling possible errors
- Processing JSON data
- Logging application progress
- Accepting command-line arguments
- Saving data to a file

This project combines concepts learned throughout the Python Programming Labs into a practical application.

---

# 🎓 Final Repository Milestone

**Lab 40 marks the completion of the 40-lab Python Programming Labs curriculum.**

You have progressed from Python environment setup and basic syntax to APIs, testing, concurrency, databases, automation, algorithms, code quality, and finally a practical CLI application.

**Python Programming Labs — 40/40 Complete. 🚀**
