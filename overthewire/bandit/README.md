# OverTheWire: Bandit

Bandit is a Linux-focused wargame from OverTheWire designed to teach the foundational skills required for cybersecurity, system administration, cloud engineering, and Linux operations.

The challenges gradually introduce Linux command-line usage, file discovery, permissions, text processing, networking, authentication, encoding, service enumeration, privilege escalation, shell scripting, and Git analysis.

This repository documents my solutions, methodology, and lessons learned while progressing through all Bandit levels. The goal was not only to solve each challenge but also to understand the underlying Linux and security concepts that frequently appear in real-world environments.

**Host:** bandit.labs.overthewire.org
**Port:** 2220

---

## Completed Levels

| Level   | Concept                                        | Writeup                   |
| ------- | ---------------------------------------------- | ------------------------- |
| 0 → 1   | Basic File Access                              | [writeup](level-00-01.md) |
| 1 → 2   | Special Character File Handling                | [writeup](level-01-02.md) |
| 2 → 3   | Escaping Spaces in Filenames                   | [writeup](level-02-03.md) |
| 3 → 4   | Hidden Files                                   | [writeup](level-03-04.md) |
| 4 → 5   | File Type Identification                       | [writeup](level-04-05.md) |
| 5 → 6   | Advanced File Enumeration                      | [writeup](level-05-06.md) |
| 6 → 7   | Permission-Based File Discovery                | [writeup](level-06-07.md) |
| 7 → 8   | Text Search with grep                          | [writeup](level-07-08.md) |
| 8 → 9   | Unique Line Identification                     | [writeup](level-08-09.md) |
| 9 → 10  | Extracting Human-Readable Strings              | [writeup](level-09-10.md) |
| 10 → 11 | Base64 Decoding                                | [writeup](level-10-11.md) |
| 11 → 12 | ROT13 Decoding                                 | [writeup](level-11-12.md) |
| 12 → 13 | Multi-Stage File Decompression                 | [writeup](level-12-13.md) |
| 13 → 14 | SSH Private Key Authentication                 | [writeup](level-13-14.md) |
| 14 → 15 | Connecting to a Local TCP Service              | [writeup](level-14-15.md) |
| 15 → 16 | SSL/TLS Encrypted Communication                | [writeup](level-15-16.md) |
| 16 → 17 | Service Enumeration and SSH Authentication     | [writeup](level-16-17.md) |
| 17 → 18 | File Comparison Using diff                     | [writeup](level-17-18.md) |
| 18 → 19 | Restricted Login Environment Bypass            | [writeup](level-18-19.md) |
| 19 → 20 | SetUID Privilege Escalation                    | [writeup](level-19-20.md) |
| 20 → 21 | Local Network Services and IPC                 | [writeup](level-20-21.md) |
| 21 → 22 | Scheduled Task Enumeration                     | [writeup](level-21-22.md) |
| 22 → 23 | Cron Job Analysis                              | [writeup](level-22-23.md) |
| 23 → 24 | Scheduled Task Abuse via Shell Scripting       | [writeup](level-23-24.md) |
| 24 → 25 | Network Service Brute Forcing                  | [writeup](level-24-25.md) |
| 25 → 26 | SSH Private Key Authentication                 | [writeup](level-25-26.md) |
| 26 → 27 | Restricted Shell Escape                        | [writeup](level-26-27.md) |
| 27 → 28 | Git Repository Cloning                         | [writeup](level-27-28.md) |
| 28 → 29 | Git Commit History Analysis                    | [writeup](level-28-29.md) |
| 29 → 30 | Git Branch Enumeration                         | [writeup](level-29-30.md) |
| 30 → 31 | Git Tag Enumeration                            | [writeup](level-30-31.md) |
| 31 → 32 | Git Repository Modification and Submission     | [writeup](level-31-32.md) |
| 32 → 33 | Restricted Shell Escape via Variable Expansion | [writeup](level-32-33.md) |

---

## Concepts Covered

### Linux Fundamentals

* Linux command-line usage
* File navigation
* File creation and manipulation
* Hidden files and directories
* Linux file systems

### Enumeration

* File discovery
* Permission-based searching
* Service enumeration
* Network enumeration
* Scheduled task enumeration

### Text Processing

* grep
* sort
* uniq
* strings
* diff

### Encoding and Decoding

* Base64
* ROT13
* Binary data inspection
* Multi-stage file extraction

### Networking

* TCP services
* Netcat
* OpenSSL
* SSL/TLS communication
* Local network services

### Authentication

* SSH passwords
* SSH private keys
* Public-key authentication

### Privilege Escalation

* SetUID binaries
* Restricted shell bypasses
* Environment abuse
* Privileged program execution

### Git Analysis

* Repository cloning
* Commit history inspection
* Branch enumeration
* Tag enumeration
* Repository modification and submission

### Automation

* Shell scripting
* Brute-force automation
* Scheduled task abuse

---

## Tools Used

Throughout the Bandit wargame, the following tools and techniques were used:

```bash
cat
less
file
find
grep
sort
uniq
strings
diff
xxd
base64
gzip
bzip2
tar
ssh
nc
openssl
nmap
cron
git
vim
bash
```

---

## Why Bandit?

Bandit serves as a practical introduction to Linux and cybersecurity concepts.

Rather than teaching security through theory, Bandit requires participants to interact directly with Linux systems and solve progressively more complex problems.

The skills developed throughout Bandit are directly applicable to:

* Security Operations Center (SOC) workflows
* Linux system administration
* Cloud engineering
* Penetration testing
* Security engineering
* Capture The Flag (CTF) competitions
* Incident response investigations

Many of the concepts introduced in Bandit reappear in more advanced wargames, real-world security assessments, and production Linux environments.

---

## Repository Structure

```text
bandit/
├── README.md
├── level-00-01.md
├── level-01-02.md
├── ...
├── level-32-33.md
│
└── assets/
```

---

## Completion Status

Bandit currently concludes at Level 33. The official OverTheWire platform notes that Level 34 does not exist at this time.

* Status: Completed
* Levels Completed: 33/33
* Final Level Reached: Bandit33


---

## Key Takeaways

The most important lessons learned throughout Bandit were:

* Enumerate before making assumptions
* Understand Linux permissions thoroughly
* Learn how common command-line tools work together
* Inspect data before attempting to decode it
* Automate repetitive tasks when possible
* Understand network services before interacting with them
* Treat Git repositories as valuable sources of information
* Privilege escalation often begins with careful enumeration

Bandit provides an excellent foundation for more advanced OverTheWire wargames such as Leviathan, Natas, Krypton, and beyond.
