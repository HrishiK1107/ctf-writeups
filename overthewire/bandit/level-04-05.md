## Bandit Level 4 → 5

**Concept:** Identifying file types in Linux
**Difficulty:** Trivial

### What the level asks

Find the only human-readable file in the `inhere` directory and retrieve the password stored inside it.

### Solution

```bash
cd inhere
# Move into the directory containing the candidate files

find . -type f | xargs file
# Determine the type of every file and identify the one marked as ASCII text

cat ./-file07
# Read the human-readable file

# Password obtained:
# [REDACTED]
```

### Real-world relevance

File type identification is a common task during malware analysis, forensic investigations, and security assessments. Analysts often encounter large collections of files and use tools such as `file` to quickly distinguish text, binaries, archives, scripts, and other content types.

```
```
