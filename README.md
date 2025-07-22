# Password Strength Checker
---
## Objective
  A simple yet effective Python tool to help users verify the strength of their passwords and check if they have appeared in known data breaches using the Have I Been Pwned API.
--- 
## Overview
- This script performs two essential tasks:
  - Evaluates Password Strength
    It verifies if a password meets widely accepted security standards, such as length, character variety, and the use of special symbols.
  - Checks for Data Breach Exposure
    It securely checks whether the password has been compromised in any known data breaches, leveraging the Pwned Passwords service provided by Have I Been Pwned.
## Attachment
   This project documentation comes with the accompanying script in python language.
---
## Prerequisites
- Python 3.x
- Internet connection for accessing the Have I Been Pwned API
---
## Features
- Strength Analysis
  - Minimum length requirement
  - Presence of uppercase letters
  - Presence of lowercase letters
  - Inclusion of numerical digits
  - Inclusion of special characters
- Breach Verification
  - Securely checks password leaks using the HIBP API
  - Implements the recommended k-anonymity approach, ensuring user privacy
  - Provides clear feedback on breach status
## Installation
1. Clone the repository
   ```bash
   git clone <repo_url>
   cd <repo_folder>
2. Install Dependencies
   The script uses re and hashlib (both standard Python libraries) and requests (an external package).
   Install requests using pip if not already installed: 
   ```bash
   pip install requests
   ```
---
## Usage
   Run the script via the terminal:
   ```bash
   python pswd_checker.py
   ```
---
## Working
This script uses the Have I Been Pwned API's k-anonymity method to ensure security and privacy:

- The password is hashed locally using SHA-1.
- Only the first five characters of the hash are sent to the API.
- The API returns all hashes with that prefix.
- The script compares the suffix locally to determine if there is a match.

At no point is your actual password or full hash transmitted over the internet.
---
## Notice
- Always use unique passwords for different services.
- Even if your password is not currently listed in a breach, there is no guarantee it is entirely secure.
- This tool is intended for personal and educational use only. Follow your organization’s password management policies for production systems.
---
## Author & License
This project was created by **_SATVIK BHAGAT_** to promote stronger password practices and raise awareness about the importance of checking for leaked credentials.
This script is free for personal and educational use. For commercial usage, please refer to the Have I Been Pwned API Terms of Use.



