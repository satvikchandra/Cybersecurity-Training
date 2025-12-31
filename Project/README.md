This repository contains my college project demonstrating Dictionary attack simulator for educational password cracking simulations.

# Dictionary Attack Simulator.

# Overview

The Dictionary Attack Simulator is a web-based tool built with Flask (Python) and Bootstrap (HTML/CSS/JS) to demonstrate how dictionary attacks can be used to crack hashed passwords.
It’s designed for educational purposes — helping students and developers understand password security, hashing algorithms, and the importance of strong, unpredictable passwords.

# Features
- Upload wordlist (.txt) files for testing
- Target hash input field to simulate cracking attempts
- Algorithm selection: SHA‑256, MD5, SHA‑1
- Interactive UI with progress bar and results display
- Backend API built with Flask to handle file uploads, hashing, and attack logic

# Tech 
- Backend: Flask (Python)
- Frontend: HTML, Bootstrap, JavaScript
- Hashing: Python’s hashlib
- Environment: Virtualenv for dependency management

# How to run
Clone the repository:
- For backend visit 'backend source code'.
- For frontend visit 'frontend source code'.

## 🔧 Setup Virtual Environment

To create and activate a virtual environment:

```
# Create venv
python -m venv venv

# Activate on Linux/Mac
source venv/bin/activate

# Activate on Windows
venv\Scripts\activate
```

Install dependencies:
```
pip install flask werkzeug
```

Run the server:
```
python app.py
```

Open in browser:
```
http://127.0.0.1:5000/ui
```

# Example
- Wordlist contains: password, 123456, qwerty
- Target hash:
  ```
  5e884898da28047151d0e56f8dc6292773603d0d6aabbdd62a11ef721d1542d8
  ```
- Algorithm: SHA‑256
- Result: ✅ Matched Password → password

# ⚠️ Disclaimer
- This project is for educational and academic purposes only.
- Do not use it for unauthorized password cracking or malicious activities.

# 📌 Future Improvements
- Real-time progress updates
- Support for more hashing algorithms
- Exportable reports of cracked results
- Enhanced UI with dark/light themes
