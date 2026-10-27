# Lab 5: Static Code Analysis — Issue Report

## Issues Identified and Fixes Applied

| Issue | Type | Location | Description | Fix Approach |
|---|---|---|---|---|
| Missing docstrings | Code quality | Multiple lines | Module and functions lacked documentation | Added descriptive docstrings |
| Non-standard naming | Code quality | Multiple lines | Names used camelCase | Renamed identifiers using snake_case |
| Mutable default argument | Bug risk | `grade_student()` | Shared dictionary could retain data between calls | Changed default to `None` and initialized inside the function |
| Inefficient iteration | Code quality | Grading loop | Used `range(len(...))` | Replaced with `enumerate()` |
| Unnecessary `elif` | Code quality | Grade function | Used `elif` after `return` | Simplified conditional logic |
| Weak MD5 hash | Security | Answer hashing | MD5 is unsuitable for security-sensitive hashing | Replaced MD5 with SHA-256 |
| Hardcoded password | Security | Module constant | Password was stored directly in source code | Removed unused password constant |
| Shell command execution | Security | Screen-lock helper | Used `os.system()` to invoke a shell command | Removed unused helper |
| Random selection warning | Security review | Bonus question | Standard pseudorandom selection was flagged by Bandit | Used `secrets.choice()` |
| Formatting violations | Style | Multiple lines | Spacing, blank-line, comment, and newline violations | Corrected formatting |

## Verification Results

- **Pylint:** 10.00/10
- **Bandit:** No issues identified
- **Flake8:** No violations reported

The updated program ran successfully and preserved the demonstrated student scores, class average, and topper.

## Conclusion

Static analysis helped identify code-quality, security, and formatting issues. Fixing these issues improved readability, maintainability, and security practices. Rerunning all three tools confirmed that the updated script passed the checks performed by the installed tools.
