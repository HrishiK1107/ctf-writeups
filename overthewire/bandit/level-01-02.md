## Bandit Level 1 → 2

**Concept:** Accessing files with special characters in their names
**Difficulty:** Trivial

### What the level asks

Retrieve the password stored in a file named `-` located in the home directory.

### Solution

```bash
ls -la
# List files and identify the file named '-'

cat ./-
# Read the file using a relative path so '-' is treated as a filename

# Password obtained:
# [REDACTED]
```

### Real-world relevance

Security analysts frequently encounter unusual filenames during investigations, malware analysis, and filesystem triage. Understanding how the shell interprets special characters helps avoid mistakes when examining suspicious files on Linux systems.
