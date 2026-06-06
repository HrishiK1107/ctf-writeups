## Bandit Level 6 → 7

**Concept:** Finding files using ownership and metadata filters
**Difficulty:** Trivial

### What the level asks

Locate a file anywhere on the system that is owned by user `bandit7`, owned by group `bandit6`, and has a size of exactly 33 bytes.

### Solution

```bash
find / -user bandit7 -group bandit6 -type f -size 33c 2>/dev/null
# Search the filesystem for files matching the required owner, group, and size
# Suppress permission-denied errors to keep the output readable

cat /var/lib/dpkg/info/bandit7.password
# Read the matching file

# Password obtained:
# [REDACTED]
```

### Real-world relevance

Ownership and metadata filtering are frequently used during incident response and system auditing. Investigators often search for files belonging to specific users, services, or applications to identify misconfigurations, sensitive data exposure, or attacker-created artifacts.

```
```
