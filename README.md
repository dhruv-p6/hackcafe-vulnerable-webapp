# HackCafe — Vulnerable Web App

A deliberately vulnerable web application built as a hands-on learning project to study common web security vulnerabilities. Each page demonstrates a specific vulnerability with a guided walkthrough of how it works, how to identify it, and how it would be fixed in a real application.

## Purpose

Built to apply concepts from cybersecurity coursework (Google Cybersecurity Professional Certificate, IBM Cybersecurity Analyst Professional Certificate) in a practical, hands-on setting rather than just theory.

## Vulnerabilities Covered

1. **Reflected XSS** — the search bar renders user input directly as HTML, allowing script injection (e.g. an `<img>` tag with an `onerror` handler) that executes in the victim's browser
2. **SQL Injection** — the login form fails to sanitize input, allowing a crafted username to comment out the password check and bypass authentication entirely
3. **Insecure Direct Object Reference (IDOR)** — the order lookup has no ownership check, so changing the order ID in the request exposes other customers' private order details
4. **Sensitive Data Exposure** — credentials and internal details are left in HTML comments, visible to anyone who views the page source
5. **Weak Passwords** — accounts use common, easily-guessed passwords, demonstrating the risk of weak password policies
6. **Stored XSS** — the review/comment section saves user input as raw HTML, so an injected script executes for every visitor who views the page afterward — a persistent, higher-impact version of #1
7. **Broken Access Control (Open Admin Panel)** — the admin panel has no authentication check at all, exposing usernames, emails, and plaintext passwords to anyone who navigates to it

## How to Use

1. Clone or download this repository
2. Open the HTML files in a browser (or visit the live demo link below, if available)
3. Each page walks through one vulnerability, showing the exploit and the underlying flaw

## Disclaimer

This project is intentionally insecure and built for educational purposes only. Do not deploy it as a real application or use these techniques against systems you don't own or have permission to test.

## Author

Dhruv Patel — [LinkedIn](https://linkedin.com/in/dhruv-patel-85a16626b/)
