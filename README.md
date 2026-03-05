# ⚙️ Automation Hub

> A desktop web automation toolkit built with Python and Tkinter, demonstrating modular architecture, GUI development, and automated testing.

[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/)  
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)  
[![Tests: pytest](https://img.shields.io/badge/tests-pytest-green.svg)](#-running-tests)

---

## ✨ Overview

Automation Hub is a **desktop multi-tool application** designed to centralize common web utilities into a single graphical interface.

The application allows users to perform tasks such as quick web searches, social media access, weather lookup, page downloads, and link validation without opening multiple browser tabs or scripts.

The project focuses on demonstrating:

- GUI development with Tkinter
- Modular Python architecture
- HTTP requests and web scraping
- Configuration management using JSON
- Logging and execution history
- Automated testing with pytest

---

## 🚀 Features

| Feature | Description |
|-------|-------------|
| Quick Search | Instantly search multiple platforms such as Google, YouTube, GitHub, and Maps |
| Social Shortcuts | Open commonly used platforms with one click |
| Weather Tool | Retrieve current weather information for any city |
| Web Downloader | Download full pages, links, or images from websites |
| Link Checker | Detect broken links on a webpage |
| History System | Automatically stores executed actions and results |

---

## 🖼 Screenshots

### Quick Search  
![Quick Search](screenshots/01_quick_search.png)

### Social Shortcuts  
![Social Shortcuts](screenshots/02_social_shortcuts.png)

### Weather  
![Weather](screenshots/03_weather.png)

### Web Downloader  
![Web Downloader](screenshots/04_web_downloader.png)

### Link Checker  
![Link Checker](screenshots/05_link_checker.png)

### History  
![History](screenshots/06_history.png)

---

## 🧰 Tools Included

### Quick Search

Search instantly using configured search engines such as:

- Google  
- YouTube  
- GitHub  
- Google Maps  

Search engines are configurable through `config.json`.

---

### Social Shortcuts

Open frequently used platforms with a single click.

Examples include:

- GitHub  
- LinkedIn  
- Twitter  

Shortcuts can be customized by editing `config.json`.

---

### Weather Tool

Retrieve current weather information for a specific city.

Displays basic data such as:

- Temperature
- Conditions
- Location

---

### Web Downloader

Download resources from a webpage.

Supported actions include:

- Download the full HTML page
- Extract all links from a page
- Download images from a page

---

### Link Checker

Scan a webpage and detect broken links.

The tool checks all hyperlinks and identifies:

- Valid links
- Broken links (404 errors)

Useful for website maintenance and SEO checks.

---

### History System

Automation Hub automatically records executed actions.

Stored information includes:

- Tool used
- Parameters
- Execution results

Users can delete individual entries or clear the entire history.

---

## 📦 Installation

### Requirements

- Python 3.8 or higher
- pip

### Setup

```
git clone https://github.com/Lautarocuello98/automation-hub.git
cd automation-hub
python -m pip install -r requirements.txt
```

---

## ▶️ Running the Application

Start the program with:

```
python app.py
```

The graphical interface will open automatically.

---

## ⚙️ Configuration

User preferences can be customized through `config.json`.

Example configuration:

```
{
  "socials": {
    "GitHub": "https://github.com",
    "LinkedIn": "https://linkedin.com"
  },
  "search_engines": {
    "Google": "https://www.google.com/search?q={query}"
  },
  "download_folder": "downloads"
}
```

You can customize:

- Social media shortcuts  
- Search engines  
- Default download folder  

---

## 📁 Project Structure

```
automation_hub/
│
├── screenshots/
│
├── tools/
│   ├── base.py
│   ├── errors.py
│   ├── types.py
│   ├── quick_search.py
│   ├── social_shortcuts.py
│   ├── weather.py
│   ├── web_downloader.py
│   └── link_checker.py
│
├── tests/
│   ├── test_imports.py
│   └── test_tools_contract.py
│
├── app.py
├── config.json
├── history.json
├── app.log
├── requirements.txt
├── pytest.ini
├── README.md
├── LICENSE
├──.gitignore
└── AutomationHub.spec
```

---

## 🧪 Running Tests

Install pytest if necessary:

```
python -m pip install pytest
```

Run all tests:

```
pytest
```

Verbose output:

```
pytest -v
```

Test files are located in:

```
tests/
├── test_imports.py
└── test_tools_contract.py
```

---

## 🏗 Architecture

The application is structured using a layered design.

```
GUI Layer (app.py)
        ↓
Tool Interface
        ↓
Individual Tools (tools/)
```

Each tool implements a shared interface:

```
run(params) -> Result
```

This allows:

- Easy feature expansion
- Independent tool logic
- Predictable error handling
- Clean debugging

---

## 💡 Use Cases

Automation Hub can be used for:

- Quickly searching multiple platforms
- Checking websites for broken links
- Downloading webpage content
- Accessing social platforms instantly
- Running small web automation tasks from a single interface

---

## 📊 Code Quality

This project demonstrates:

- Modular Python architecture
- GUI development with Tkinter
- Web requests and scraping
- Configuration-driven applications
- Logging and history persistence
- Automated testing with pytest

---

## 🚀 Possible Future Improvements

Potential enhancements include:

- Additional automation tools
- Exportable history reports
- Plugin system for new tools
- Improved GUI components
- Cross-platform packaging

---

## 📄 License

This project is licensed under the MIT License.

See the **LICENSE** file for details.

---

## 👨‍💻 Author

**Lautaro Cuello**

GitHub:  
https://github.com/Lautarocuello98

Python developer focused on automation, scripting, and practical tools.

---

⭐ If you found this project useful, consider giving this repository a star.
