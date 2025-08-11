# Metasploitable2-DVWA-Project
Damn Vulnerable Web Application (DVWA) Pentesting Report – A detailed security assessment of DVWA covering vulnerability identification, exploitation techniques, and remediation strategies. Includes practical demonstrations of web security flaws such as SQL Injection, XSS, CSRF, Command Injection, and more, along with mitigation recommendations.



# DVWA (Damn Vulnerable Web Application) – Complete Guide

## Table of Contents
1. [Introduction](#introduction)
2. [Installation & Setup](#installation--setup)
3. [Security Levels in DVWA](#security-levels-in-dvwa)
4. [Modules & Vulnerabilities](#modules--vulnerabilities)
    - [SQL Injection](#sql-injection)
    - [XSS (Cross-Site Scripting)](#xss-cross-site-scripting)
    - [CSRF (Cross-Site Request Forgery)](#csrf-cross-site-request-forgery)
    - [Command Injection](#command-injection)
    - [File Inclusion](#file-inclusion)
    - [Brute Force](#brute-force)
5. [Best Practices for Testing](#best-practices-for-testing)
6. [Mitigation Techniques](#mitigation-techniques)
7. [References](#references)

---

## Introduction
Damn Vulnerable Web Application (DVWA) is a PHP/MySQL web application designed for security professionals to test their skills and tools in a legal environment. It contains several security flaws to practice penetration testing techniques.

---

## Installation & Setup
1. Download DVWA from the official GitHub repository.
2. Place it in your web server directory (e.g., `htdocs` for XAMPP).
3. Configure `config.inc.php` with your database credentials.
4. Import the `dvwa.sql` database.
5. Start Apache and MySQL.
6. Access DVWA via `http://localhost/dvwa`.

---

## Security Levels in DVWA
DVWA has three security levels:
- **Low** – Minimal protection, easy to exploit.
- **Medium** – Basic security features enabled.
- **High** – Advanced protection and sanitization.

---

## Modules & Vulnerabilities

### SQL Injection
- **Goal:** Test ability to exploit and extract database information.
- **Example Payload:** `' OR '1'='1 --`
- **Mitigation:** Use prepared statements and parameterized queries.

### XSS (Cross-Site Scripting)
- **Goal:** Inject malicious JavaScript into a web page.
- **Example Payload:** `<script>alert('XSS')</script>`
- **Mitigation:** Input validation and output encoding.

### CSRF (Cross-Site Request Forgery)
- **Goal:** Trick authenticated users into performing unwanted actions.
- **Mitigation:** Use CSRF tokens in forms.

### Command Injection
- **Goal:** Execute OS commands via unsanitized user input.
- **Example Payload:** `; ls`
- **Mitigation:** Validate and sanitize user inputs.

### File Inclusion
- **Goal:** Include unauthorized files on the server.
- **Types:** Local File Inclusion (LFI), Remote File Inclusion (RFI)
- **Mitigation:** Use whitelists for file paths.

### Brute Force
- **Goal:** Guess valid login credentials by repeated attempts.
- **Mitigation:** Rate limiting, account lockouts, strong password policies.

---

## Best Practices for Testing
- Always test in a controlled, isolated environment.
- Document each vulnerability found.
- Use tools like Burp Suite, OWASP ZAP, and SQLMap for automation.

---

## Mitigation Techniques
- Validate and sanitize all inputs.
- Apply the principle of least privilege.
- Keep software up to date.
- Implement secure coding practices.

---

## References
- [DVWA GitHub Repository](https://github.com/digininja/DVWA)
- [OWASP Top Ten](https://owasp.org/www-project-top-ten/)
