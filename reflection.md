\# Lab 5: Static Code Analysis — Reflection



\## 1. What is static code analysis, and why is it important?



\*\*Answer:\*\* Static code analysis examines source code without executing it to identify bugs, security vulnerabilities, and coding style issues. It helps improve code quality, security, and maintainability. In this lab, I used Pylint, Bandit, and Flake8 to analyze my Python program.



\## 2. What issues did you identify, and how did you fix them?



\*\*Answer:\*\* I identified missing docstrings, inconsistent naming, a mutable default argument, weak MD5 hashing, and unsafe shell command execution. I added docstrings, changed names to snake\_case, replaced the mutable default with None, used SHA-256, and removed the unused shell command helper.



\## 3. How did Pylint, Bandit, and Flake8 help improve your code?



\*\*Answer:\*\* Pylint identified code quality issues, Bandit detected potential security vulnerabilities, and Flake8 found formatting violations. After fixing the issues, Pylint scored 10.00/10, Bandit reported no issues, and Flake8 reported no violations.



\## 4. What did you learn from this lab?



\*\*Answer:\*\* I learned to write cleaner and safer Python code, avoid mutable default arguments, follow naming conventions, and use static analysis tools regularly. I will use these tools in future projects to identify and fix problems before submitting or deploying my code.

