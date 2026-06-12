# OverTheWire Writeups

This repository contains writeups for challenges from the OverTheWire wargames platform.

OverTheWire provides hands-on exercises focused on Linux fundamentals, networking, cryptography, web application security, file systems, permissions, authentication, privilege escalation, binary analysis, and security concepts. These challenges are designed to build practical problem-solving skills that transfer directly into real-world cybersecurity work.

## Wargames

| Wargame   | Status            |
| --------- | ----------------- |
| Bandit    | Completed (33/33) |
| Leviathan | Completed (8/8)   |
| Krypton   | Completed (7/7)   |
| Natas     | Completed (34/34) |

---

## Why OverTheWire?

OverTheWire provides structured, progressive challenges that introduce both foundational and advanced security concepts through practical exercises rather than theory alone.

The platform encourages methodical problem-solving, enumeration, experimentation, analysis, and exploitation—skills that are essential across multiple cybersecurity domains.

---

## Why Bandit?

Bandit serves as a foundation for many cybersecurity disciplines by introducing:

* Linux command-line proficiency
* File discovery and manipulation
* Permissions and ownership
* Networking fundamentals
* Service enumeration
* Data encoding and decoding
* SSH authentication
* SSL/TLS communication
* Shell scripting
* Cron job analysis
* Git repository analysis
* Restricted shell bypass techniques
* Privilege escalation concepts

These skills frequently appear in SOC investigations, penetration testing engagements, cloud environments, system administration, and security engineering workflows.

---

## Why Leviathan?

Leviathan focuses on attacker methodology and Linux privilege escalation.

Unlike Bandit, Leviathan provides little guidance and requires participants to discover attack paths through enumeration and analysis.

Key concepts covered include:

* SUID binary enumeration
* Dynamic binary analysis with ltrace
* Hardcoded credential discovery
* Authentication bypass techniques
* Symbolic link attacks
* Command construction flaws
* Binary and ASCII decoding
* Local brute-force attacks
* Linux privilege escalation methodology

The challenges closely resemble techniques encountered during Linux penetration testing and privilege escalation assessments.

---

## Why Krypton?

Krypton introduces classical cryptography and practical cryptanalysis.

Instead of exploiting systems directly, participants must understand how encryption schemes operate and how weaknesses in their design can be leveraged to recover hidden information.

Key concepts covered include:

* Base64 Encoding and Decoding
* Caesar Cipher
* ROT13
* Chosen Plaintext Attacks
* Encryption Oracles
* Monoalphabetic Substitution Ciphers
* Frequency Analysis
* Vigenère Cipher Cryptanalysis
* Key Length Determination
* Kasiski-style Analysis
* Stream Cipher Analysis
* Linear Feedback Shift Registers (LFSRs)
* Known Plaintext Attacks
* Weak Random Number Generation

These concepts frequently appear in malware analysis, digital forensics, threat intelligence investigations, reverse engineering, and cryptographic security research.

---

## Why Natas?

Natas focuses entirely on web application security.

Each level presents a live web application that must be analyzed through HTTP requests, cookies, sessions, source code review, application behavior, and exploit development.

Key concepts covered include:

* Information Disclosure
* Directory Traversal
* Command Injection
* SQL Injection
* Blind SQL Injection
* File Upload Vulnerabilities
* Session Hijacking
* Session Prediction
* Session Poisoning
* Authentication Bypass
* Authorization Bypass
* Cookie Manipulation
* XOR Cryptography Weaknesses
* ECB Cut-and-Paste Attacks
* PHP Type Juggling
* PHP Object Injection
* Local File Inclusion (LFI)
* Log Poisoning
* Argument Injection
* Perl Injection
* MD5 Collision Abuse
* PHP Phar Deserialization
* Remote Code Execution

The challenges closely mirror vulnerability classes encountered during web application penetration tests, bug bounty programs, VAPT engagements, and application security reviews.

---

## Progress Summary

### Bandit

* Status: Completed
* Levels Completed: 33/33
* Documentation: Complete

### Leviathan

* Status: Completed
* Levels Completed: 8/8
* Documentation: Complete

### Krypton

* Status: Completed
* Levels Completed: 7/7
* Documentation: Complete

### Natas

* Status: Completed
* Levels Completed: 34/34
* Documentation: Complete

**Topics Covered**

* Web Application Security
* HTTP Request Analysis
* Authentication Testing
* Authorization Testing
* Session Management
* Command Injection
* SQL Injection
* Blind SQL Injection
* File Upload Security
* Cryptographic Weaknesses
* Local File Inclusion
* Object Injection
* Deserialization Attacks
* Remote Code Execution

---

## Repository Structure

```text
overthewire/
├── README.md
├── bandit/
│   ├── README.md
│   └── level-writeups...
│
├── leviathan/
│   ├── README.md
│   └── level-writeups...
│
├── krypton/
│   ├── README.md
│   └── level-writeups...
│
└── natas/
    ├── README.md
    └── level-writeups...
```

---

## Completion Status

| Wargame   | Progress |
| --------- | -------- |
| Bandit    | 33 / 33  |
| Leviathan | 8 / 8    |
| Krypton   | 7 / 7    |
| Natas     | 34 / 34  |

---

## Current Repository Statistics

* Total Wargames Completed: 4
* Total Levels Completed: 82
* Documentation Status: Complete

---

## Key Takeaways

Across all completed OverTheWire wargames, the primary lessons were:

* Enumerate before exploiting
* Understand how applications process user input
* Never trust client-controlled data
* Authentication and authorization are separate problems
* Small implementation mistakes often create critical vulnerabilities
* Cryptography is frequently broken through misuse rather than mathematics
* Session management is a common attack surface
* File handling functionality requires strict validation
* Source code review dramatically accelerates vulnerability discovery
* Automation is essential for efficient exploitation

These concepts regularly appear in penetration testing engagements, red team operations, secure code reviews, malware analysis, incident response investigations, application security engineering, and offensive security research.
