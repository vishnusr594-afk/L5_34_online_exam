# Lab 5: Static Code Analysis — Reflection

## Question 1: What is static code analysis, and why is it important?

**Answer:**

Static code analysis is the process of examining source code without executing it to identify potential bugs, security vulnerabilities, and coding style issues.

It is important because it helps developers detect problems early, improve code quality, enhance security, and make programs easier to maintain.

In this lab, I used **Pylint, Bandit, and Flake8** to analyze my Python program.

---

## Question 2: What issues did you identify, and how did you fix them?

**Answer:**

I identified several issues in `online_exam.py`, including:

- Missing module and function docstrings.
- Inconsistent naming conventions.
- A mutable default argument.
- Weak MD5 hashing.
- A hardcoded password.
- Unsafe shell command execution.
- Formatting violations.

I fixed these issues by adding docstrings, using `snake_case` naming, replacing the mutable default argument with `None`, changing MD5 to SHA-256, removing the unused hardcoded password and shell command helper, and correcting the formatting violations.

---

## Question 3: How did Pylint, Bandit, and Flake8 help improve your code?

**Answer:**

Each tool helped identify a different category of problems:

- **Pylint:** Identified code quality issues, including missing documentation, naming problems, and inefficient iteration.
- **Bandit:** Detected potential security issues, including weak hashing, a hardcoded password, and shell command execution.
- **Flake8:** Identified formatting violations, such as incorrect whitespace, blank lines, and a missing final newline.

After fixing the reported issues, the final results were:

| Tool | Final result |
|---|---|
| Pylint | 10.00/10 |
| Bandit | No issues identified |
| Flake8 | No violations reported |

These tools helped improve the readability, maintainability, and security of my program.

---

## Question 4: What did you learn from this lab, and how will you apply it in future projects?

**Answer:**

I learned that a program can run successfully and still contain code quality issues, potential security vulnerabilities, and style violations.

I also learned the importance of avoiding mutable default arguments, following Python naming conventions, using appropriate security practices, and maintaining consistent formatting.

In future projects, I will use static analysis tools regularly, review their reports, fix important findings, and rerun the tools to verify my changes before submitting or deploying code.

---

## Conclusion

This lab helped me understand the importance of static code analysis in software development. By using Pylint, Bandit, and Flake8, I improved my Python program and verified the fixes with the final analysis reports.
