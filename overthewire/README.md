# OverTheWire Writeups

This repository contains writeups for challenges from the OverTheWire wargames platform.

OverTheWire provides hands-on exercises focused on Linux fundamentals, networking, cryptography, file systems, permissions, authentication, privilege escalation, binary analysis, and security concepts. These challenges are designed to build practical problem-solving skills that transfer directly into real-world cybersecurity work.

## Wargames

| Wargame   | Status            |
| --------- | ----------------- |
| Bandit    | Completed (33/33) |
| Leviathan | Completed (8/8)   |
| Krypton   | Completed (7/7)   |
| Natas     | Planned           |

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

## Progress Summary

### Bandit

* Status: Completed
* Levels Completed: 33/33
* Documentation: Complete

**Topics Covered**

* Linux Fundamentals
* File Enumeration
* Permissions and Access Control
* Text Processing
* Data Encoding and Decoding
* Binary Analysis
* Compression Formats
* SSH Authentication
* SSL/TLS Communication
* Service Enumeration
* Local Network Services
* Cron Job Analysis
* Shell Scripting
* Brute Force Automation
* SetUID Privilege Escalation
* Restricted Shell Escapes
* Git Commit History Analysis
* Git Branch Enumeration
* Git Tag Enumeration

### Leviathan

* Status: Completed
* Levels Completed: 8/8
* Documentation: Complete

**Topics Covered**

* Hidden File and Directory Enumeration
* Runtime Binary Analysis
* ltrace-Based Investigation
* Hardcoded Credential Extraction
* String Comparison Analysis
* SUID Privilege Escalation
* Filename Manipulation Attacks
* Symbolic Link Attacks
* Binary-to-ASCII Decoding
* Local Authentication Brute Forcing
* Linux Privilege Escalation Methodology

### Krypton

* Status: Completed
* Levels Completed: 7/7
* Documentation: Complete

**Topics Covered**

* Base64 Decoding
* Caesar Cipher Analysis
* ROT13
* Chosen Plaintext Attacks
* Encryption Oracle Abuse
* Frequency Analysis
* Monoalphabetic Substitution Ciphers
* Vigenère Cipher Cryptanalysis
* Key Length Discovery
* Stream Cipher Weaknesses
* LFSR Analysis
* Known Plaintext Attacks
* Keystream Recovery

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
└── krypton/
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
| Natas     | Planned  |

Additional OverTheWire wargames will be documented as they are completed.
