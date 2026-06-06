## Bandit Level 7 → 8

**Concept:** Searching text using pattern matching

**Difficulty:** Trivial

### What the level asks

Retrieve the password stored in `data.txt` next to the word `millionth`.

### Solution

```bash
cat data.txt | grep "millionth"
# Search the file for the line containing the keyword 'millionth'

# Password obtained:
# [REDACTED]
```

### Real-world relevance

Pattern matching is a fundamental skill in security operations. Analysts frequently use tools such as `grep` to locate indicators of compromise, suspicious commands, usernames, IP addresses, or specific log entries within large datasets.

```
```
