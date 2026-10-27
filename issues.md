\# Lab 5: Static Code Analysis — Issue Report



\## Issues Identified and Fixes Applied



| Issue | Type | Original location | Description | Fix approach |

|---|---|---|---|---|

| Missing module and function docstrings | Code quality | Multiple lines | Functions and module lacked documentation | Added descriptive docstrings |

| Non-standard naming | Code quality | Multiple lines | Function and parameter names used camelCase | Renamed identifiers using snake\_case |

| Mutable default argument | Bug risk | `gradeStudent()` | A shared dictionary default could retain state between calls | Changed the default to `None` and initialized it inside the function |

| Inefficient iteration | Code quality | Grading loop | Used `range(len(...))` to access questions | Replaced with `enumerate()` |

| Unnecessary `elif` | Code quality | Grade function | Used `elif` after a return statement | Simplified conditional logic |

| Weak MD5 hash | Security | Answer hashing | MD5 is not suitable for security-sensitive hashing | Replaced MD5 with SHA-256 |

| Hardcoded proctor password | Security | Module constant | Password was stored directly in source code | Removed the unused hardcoded password |

| Shell command execution | Security | Screen-lock helper | Used `os.system()` to invoke a shell command | Removed the unused helper from the demo |

| Random selection warning | Security review | Bonus question | Standard pseudorandom selection was flagged by Bandit | Used `secrets.choice()` |

| Formatting violations | Style | Multiple lines | Incorrect spacing, blank lines, inline comments, and missing final newline | Corrected formatting |



\## Verification Results



\- Pylint: 10.00/10.

\- Bandit: No issues identified.

\- Flake8: No violations reported.



The updated program ran successfully and preserved the demonstrated student scores, class average, and topper.



\## Conclusion



Static analysis helped identify code-quality, security, and formatting issues before submission. Fixing these issues improved readability, maintainability, and security practices. Rerunning all three tools confirmed that the updated script satisfied the checks performed by the installed tools.

