# OverTheWire: Natas

Natas is a web application security wargame from OverTheWire.

Unlike Bandit, Leviathan, and Krypton, Natas focuses entirely on web security. Each level is a live web application that must be analyzed through HTTP requests, responses, cookies, sessions, source code review, and application behavior.

The challenges cover a wide range of web application vulnerabilities including information disclosure, access control flaws, session management weaknesses, command injection, SQL injection, file upload vulnerabilities, cryptographic weaknesses, PHP type juggling, deserialization attacks, and remote code execution.

**Host:** natas.labs.overthewire.org

---

## Completed Levels

| Level   | Concept                        | Technique                         | Writeup                   |
| ------- | ------------------------------ | --------------------------------- | ------------------------- |
| 0 → 1   | Information Disclosure         | HTML Source Inspection            | [writeup](level-00-01.md) |
| 1 → 2   | Client-Side Restriction Bypass | Developer Tools Inspection        | [writeup](level-01-02.md) |
| 2 → 3   | Directory Enumeration          | Exposed File Discovery            | [writeup](level-02-03.md) |
| 3 → 4   | robots.txt Enumeration         | Hidden Directory Discovery        | [writeup](level-03-04.md) |
| 4 → 5   | Broken Access Control          | HTTP Referer Manipulation         | [writeup](level-04-05.md) |
| 5 → 6   | Session Management Weakness    | Cookie Manipulation               | [writeup](level-05-06.md) |
| 6 → 7   | Source Code Disclosure         | Hardcoded Secret Recovery         | [writeup](level-06-07.md) |
| 7 → 8   | Directory Traversal            | URL Parameter Manipulation        | [writeup](level-07-08.md) |
| 8 → 9   | Encoding Reversal              | Base64 + Hex Decoding             | [writeup](level-08-09.md) |
| 9 → 10  | Command Injection              | Unfiltered passthru()             | [writeup](level-09-10.md) |
| 10 → 11 | Command Injection              | Filter Bypass                     | [writeup](level-10-11.md) |
| 11 → 12 | Cryptographic Failure          | XOR Cookie Forgery                | [writeup](level-11-12.md) |
| 12 → 13 | Unrestricted File Upload       | PHP Webshell Upload               | [writeup](level-12-13.md) |
| 13 → 14 | File Upload Bypass             | Magic Bytes Manipulation          | [writeup](level-13-14.md) |
| 14 → 15 | SQL Injection                  | Authentication Bypass             | [writeup](level-14-15.md) |
| 15 → 16 | Blind SQL Injection            | Boolean Enumeration               | [writeup](level-15-16.md) |
| 16 → 17 | Blind Command Injection        | Command Substitution Bypass       | [writeup](level-16-17.md) |
| 17 → 18 | Blind SQL Injection            | Time-Based Enumeration            | [writeup](level-17-18.md) |
| 18 → 19 | Session Hijacking              | Session ID Brute Force            | [writeup](level-18-19.md) |
| 19 → 20 | Session Prediction             | Encoded Session Enumeration       | [writeup](level-19-20.md) |
| 20 → 21 | Session Manipulation           | Object Injection via Newline      | [writeup](level-20-21.md) |
| 21 → 22 | Broken Access Control          | Cross-Application Session Sharing | [writeup](level-21-22.md) |
| 22 → 23 | Redirect Bypass                | Header Manipulation               | [writeup](level-22-23.md) |
| 23 → 24 | PHP Loose Comparison           | strncmp() Bypass                  | [writeup](level-23-24.md) |
| 24 → 25 | PHP Type Juggling              | Array Injection                   | [writeup](level-24-25.md) |
| 25 → 26 | Local File Inclusion           | Log Poisoning to RCE              | [writeup](level-25-26.md) |
| 26 → 27 | PHP Object Injection           | Cookie Deserialization            | [writeup](level-26-27.md) |
| 27 → 28 | SQL Truncation Attack          | Account Manipulation              | [writeup](level-27-28.md) |
| 28 → 29 | Cryptographic Weakness         | ECB Cut-and-Paste Attack          | [writeup](level-28-29.md) |
| 29 → 30 | Perl Injection                 | Command Injection via open()      | [writeup](level-29-30.md) |
| 30 → 31 | Perl SQL Injection             | Array-Based Type Confusion        | [writeup](level-30-31.md) |
| 31 → 32 | Argument Injection             | Multipart Parameter Pollution     | [writeup](level-31-32.md) |
| 32 → 33 | MD5 Collision Abuse            | File Upload Type Confusion        | [writeup](level-32-33.md) |
| 33 → 34 | PHP Phar Deserialization       | File Upload RCE                   | [writeup](level-33-34.md) |

---

## Concepts Covered

### Information Disclosure

* HTML source inspection
* Source code disclosure
* Hidden file discovery
* robots.txt enumeration

### Access Control & Session Security

* Referer manipulation
* Cookie tampering
* Session hijacking
* Session prediction
* Session poisoning
* Cross-application session sharing
* Authentication bypass

### Injection Vulnerabilities

* Command injection
* Blind command injection
* SQL injection
* Blind SQL injection
* Time-based SQL injection
* Argument injection
* Perl injection

### File Handling Vulnerabilities

* Unrestricted file upload
* Magic bytes bypass
* Local File Inclusion (LFI)
* Log poisoning
* File upload RCE

### PHP Security Weaknesses

* Loose comparison vulnerabilities
* Type juggling
* Object injection
* Deserialization attacks
* Phar deserialization

### Cryptography & Encoding

* Base64 decoding
* Hex decoding
* XOR cookie forgery
* ECB block cipher manipulation

---

## Tools Used

Throughout the Natas wargame, the following tools and techniques were used:

```text
Firefox Developer Tools
Browser Storage Inspector
Browser Network Inspector
Burp Suite Repeater
Burp Suite Intruder
Python
requests
curl
PHP
Perl
Linux CLI
Base64
Hex Encoding
Multipart Request Manipulation
HTTP Request Analysis
```

---

## Why Natas?

Natas teaches web application penetration testing methodology.

The core skill developed throughout Natas is learning how modern web applications trust user-controlled data and how those trust assumptions can fail.

Each level reinforces a different aspect of web security:

* Understanding HTTP requests and responses
* Reviewing source code for security flaws
* Testing authentication and authorization logic
* Manipulating cookies and session state
* Exploiting command injection and SQL injection
* Abusing file upload functionality
* Identifying cryptographic design flaws
* Exploiting PHP-specific security weaknesses
* Chaining vulnerabilities into remote code execution

These skills map directly to real-world web application assessments, bug bounty programs, VAPT engagements, red team operations, and application security engineering.

---

## Repository Structure

```text
natas/
├── README.md
├── level-00-01.md
├── level-01-02.md
├── ...
├── level-33-34.md
│
└── assets/
```

---

## Completion Status

* Status: Completed
* Levels Completed: 34/34
* Final Level Reached: Natas34

### Completion Proof

![Natas completion](assets/level-34-completion.png)

---

## Key Takeaways

Natas demonstrates that web application security is rarely about a single vulnerability.

Across the 34 levels, the primary lessons were:

* Never trust client-controlled input
* Review source code whenever it is available
* Validate both input content and input types
* Session identifiers must be unpredictable
* Encryption does not guarantee integrity
* File uploads should never be trusted
* Blacklists are weaker than allowlists
* Deserialization can lead directly to code execution
* Small implementation mistakes often create critical vulnerabilities
* Real-world exploitation frequently requires chaining multiple weaknesses

These concepts appear regularly in web application penetration tests, bug bounty programs, red team engagements, secure code reviews, and application security engineering roles.
