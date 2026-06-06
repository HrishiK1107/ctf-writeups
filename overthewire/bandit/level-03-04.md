## Bandit Level 3 → 4

**Concept:** Discovering hidden files in Linux
**Difficulty:** Trivial

### What the level asks

Locate a hidden file inside the `inhere` directory and retrieve the password stored within it.

### Solution

```bash
cd inhere
# Move into the directory containing the hidden file

ls -all
# Display hidden files and directories

cat ...Hiding-From-You
# Read the contents of the hidden file

# Password obtained:
# [REDACTED]
```

### Real-world relevance

Hidden files are commonly used to store configuration data, shell history, application settings, and occasionally attacker artifacts. During incident response and security assessments, enumerating hidden files is a routine step when examining Linux systems.

```
```
