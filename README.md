# 🤖 Python Automation with Selenium

A comprehensive collection of web automation scripts using Python and Selenium WebDriver. This repository demonstrates practical browser automation techniques, from basic navigation to advanced element interactions and waiting strategies.

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Selenium](https://img.shields.io/badge/Selenium-43B02A?style=for-the-badge&logo=selenium&logoColor=white)
![Firefox](https://img.shields.io/badge/Firefox-FF7139?style=for-the-badge&logo=Firefox-Browser&logoColor=white)

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Project Structure](#project-structure)
- [Technologies](#technologies)
- [Installation](#installation)
- [Usage](#usage)
- [Learning Modules](#learning-modules)
- [Key Concepts Covered](#key-concepts-covered)
- [Contributing](#contributing)
- [License](#license)

## 🎯 Overview

This project showcases my proficiency in **web automation** and **testing** using Selenium WebDriver with Python. Each module demonstrates different aspects of browser automation, making it an excellent resource for learning Selenium or serving as a reference for automation projects.

## ✨ Features

- 🌐 **Browser Automation**: Automated interaction with web pages using Selenium WebDriver
- 🔍 **Element Location**: Multiple strategies for finding web elements (ID, Name, XPath, Class Name)
- 🎯 **User Interactions**: Simulating user actions like typing, clicking, and form submissions
- ⏱️ **Smart Waiting**: Explicit and implicit waits for handling dynamic content
- 📝 **Form Handling**: Automated form filling and submission
- 🎨 **Dropdown Menus**: Selection and interaction with dropdown elements
- 🔑 **Keyboard Events**: Simulating keyboard inputs and special keys

## 📁 Project Structure

```
python-automation-with-selenium/
│
├── CH01/                      # Getting Started with Selenium
│   ├── 01_02/                 # Basic browser initialization
│   ├── 01_03/                 # Page navigation and search
│   └── 01_04/                 # Element interaction basics
│
├── CH02/                      # Locating Elements
│   ├── 02_02/                 # Finding elements by ID
│   ├── 02_03/                 # Finding elements by Name
│   ├── 02_04/                 # Finding elements by Class/XPath
│   ├── 02_05/                 # Advanced element location
│   ├── 02_07/                 # Challenge: Multiple locator strategies
│   └── html_code_02.html      # Practice HTML page
│
├── CH03/                      # Interacting with Elements
│   ├── 03_01/                 # Sending keys and text input
│   ├── 03_02/                 # Working with dropdowns
│   ├── 03_03/                 # Form submission
│   ├── 03_05/                 # Challenge: Complex interactions
│   └── html_code_03_02.html   # Practice HTML page
│
└── CH04/                      # Advanced Techniques
    ├── 04_02/                 # Explicit waits
    └── 04_03/                 # WebDriverWait and Expected Conditions
```

## 🛠️ Technologies

- **Python 3.x** - Primary programming language
- **Selenium WebDriver** - Browser automation framework
- **Firefox/GeckoDriver** - WebDriver for Firefox browser
- **HTML/CSS** - For practice web pages

## 📦 Installation

### Prerequisites

```bash
# Python 3.x installed
python --version

# pip (Python package manager)
pip --version
```

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/python-automation-with-selenium.git
   cd python-automation-with-selenium
   ```

2. **Install dependencies**
   ```bash
   pip install selenium
   ```

3. **Install WebDriver**
   
   **Option A: Using webdriver-manager (Recommended)**
   ```bash
   pip install webdriver-manager
   ```
   
   **Option B: Manual installation**
   - Download [GeckoDriver](https://github.com/mozilla/geckodriver/releases) for Firefox
   - Add to system PATH

4. **Verify installation**
   ```python
   from selenium import webdriver
   driver = webdriver.Firefox()
   driver.get('https://www.python.org')
   driver.quit()
   ```

## 🚀 Usage

### Running Individual Scripts

Navigate to any chapter directory and run the Python scripts:

```bash
# Example: Run basic navigation script
cd CH01/01_03
python code_01_03.py
```

### Sample Code

**Basic Web Navigation:**
```python
from selenium import webdriver
from selenium.webdriver.common.keys import Keys

driver = webdriver.Firefox()
driver.get("http://www.python.org")

# Find search box and perform search
search_box = driver.find_element_by_name("q")
search_box.send_keys("pycon")
search_box.send_keys(Keys.RETURN)

driver.close()
```

**Using Explicit Waits:**
```python
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC
from selenium.webdriver.common.by import By

driver = webdriver.Firefox()
driver.get('http://www.python.org')

try:
    element = WebDriverWait(driver, 10).until(
        EC.presence_of_element_located((By.ID, "start-shell"))
    )
finally:
    driver.quit()
```

## 📚 Learning Modules

### Chapter 1: Getting Started
- Setting up Selenium WebDriver
- Basic browser operations (open, navigate, close)
- First automated test

### Chapter 2: Locating Elements
- Finding elements by ID
- Finding elements by Name
- Finding elements by Class Name
- Using XPath selectors
- **Challenge**: Implement multiple locator strategies

### Chapter 3: Interacting with Elements
- Sending keyboard input
- Clicking elements
- Working with dropdown menus
- Form submission
- **Challenge**: Complex form automation

### Chapter 4: Advanced Techniques
- Implicit vs Explicit waits
- WebDriverWait implementation
- Expected Conditions
- Handling dynamic content

## 🎓 Key Concepts Covered

| Concept | Description | Example Location |
|---------|-------------|------------------|
| **Element Locators** | Find elements using various strategies | `CH02/*` |
| **User Interactions** | Simulate clicks, typing, submissions | `CH03/*` |
| **Waits** | Handle page load timing issues | `CH04/*` |
| **Form Automation** | Fill and submit forms programmatically | `CH02/02_05` |
| **Dropdown Handling** | Select options from dropdown menus | `CH03/03_02` |
| **Keyboard Events** | Send special keys (Enter, Tab, etc.) | `CH01/01_03` |

## 🎯 Skills Demonstrated

- ✅ **Python Programming**: Object-oriented approach, error handling, modules
- ✅ **Web Automation**: Comprehensive Selenium WebDriver usage
- ✅ **Testing Concepts**: Element verification, wait strategies
- ✅ **Problem Solving**: Challenges in chapters 2 and 3
- ✅ **Clean Code**: Well-organized, commented, and documented
- ✅ **Version Control**: Structured Git repository

## 🔧 Common Use Cases

This automation framework can be adapted for:

- 🧪 **Automated Testing**: End-to-end web application testing
- 📊 **Web Scraping**: Extract data from dynamic websites
- 🔄 **Repetitive Tasks**: Automate form filling, data entry
- 🔍 **Web Monitoring**: Check website changes and availability
- 📱 **Social Media Automation**: Schedule posts, interactions
- 📧 **Email Automation**: Automated email operations

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request


## 👤 Author

- GitHub: [@Yahyalt](https://github.com/Yahyalt)

