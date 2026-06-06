## Bandit Level 0 → 1

**Concept:** Basic Linux file discovery and file reading
**Difficulty:** Trivial

### What the level asks

Connect to the Bandit server and retrieve the password stored in a file within the user's home directory.

### Solution

```bash
ssh bandit.labs.overthewire.org -l bandit0 -p 2220
# Connect to the Bandit game server using the provided credentials

ls
# List files in the current directory to identify available content

cat readme
# Read the file containing the password for the next level

# Password obtained:
# [REDACTED]
```

### Real-world relevance

Reading files directly from the command line is a fundamental skill during Linux administration, security assessments, and incident response. Security analysts frequently inspect configuration files, logs, scripts, and credential stores to understand system behavior and investigate suspicious activity.
