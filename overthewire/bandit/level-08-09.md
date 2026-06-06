## Bandit Level 8 → 9

**Concept:** Identifying unique entries in a dataset

**Difficulty:** Trivial

### What the level asks

Find the only line in `data.txt` that appears exactly once.

### Solution

```bash
sort data.txt | uniq -u
# Sort the file so duplicate lines become adjacent
# Display only lines that occur exactly once

# Password obtained:
# [REDACTED]
```

### Real-world relevance

Deduplication is a common task in log analysis, threat hunting, and data processing. Security analysts often remove repeated events to highlight unusual activity, unique indicators, or anomalies that may require further investigation.

```
```
