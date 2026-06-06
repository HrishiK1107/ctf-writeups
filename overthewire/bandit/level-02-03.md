## Bandit Level 2 → 3

**Concept:** Handling filenames containing spaces
**Difficulty:** Trivial

### What the level asks

Retrieve the password stored in a file whose name contains spaces.

### Solution

```bash
ls -la
# Identify the file with spaces in its name

cat "./--spaces in this filename--"
# Quote the filename so the shell treats it as a single argument

# Password obtained:
# [REDACTED]
```

### Real-world relevance

Files containing spaces are common on Linux and cloud-hosted systems. Correctly escaping or quoting filenames is important when reviewing logs, collecting evidence, or writing automation scripts that process filesystem data.
