# Secure Coding Review Report
**Project:** Flask-Based Login App  
**Reviewer:** MD SOJIB
**Internship:** CodeAlpha Cybersecurity Internship  
**Date:** June 2025

## Overview
This project involves a code review of a simple Python Flask web application. The objective is to identify and document security vulnerabilities, suggest remediation strategies, and apply secure coding best practices.

## 🔍 Tools Used
- Bandit (static code analysis)
- Manual review
- OWASP Top 10 reference

## Vulnerabilities Found & Fixes

### 1. SQL Injection
- **Issue:** User input directly concatenated in SQL query.
- **Fix:** Replaced with parameterized queries.

### 2. Plaintext Password Storage
- **Issue:** Passwords stored and compared as plaintext.
- **Fix:** Integrated `bcrypt` for hashing and secure comparison.

### 3. Insecure Cookies
- **Issue:** Cookies set without secure/httponly flags.
- **Fix:** Added flags during cookie setting.

### 4. Debug Mode Enabled
- **Issue:** Application runs in debug mode.
- **Fix:** Disabled debug mode for production.

### 5. No CSRF Protection
- **Issue:** No CSRF token on login form.
- **Fix:** Suggested Flask-WTF implementation.

## Best Practices Applied
- Input validation
- Secure session handling
- Password hashing with salt
- Secure error handling

## Screenshots
All tool outputs and findings are included in `/screenshots/`.

## References
- [OWASP Top 10](https://owasp.org/www-project-top-ten/)
- [Bandit Tool](https://bandit.readthedocs.io/en/latest/)
- [Flask Security Guide](https://flask.palletsprojects.com/en/2.3.x/security/)

## Conclusion
The vulnerable Flask app was thoroughly reviewed and enhanced using secure coding practices. These improvements significantly reduce the attack surface and align with industry standards.
