## Bandit Level 5 → 6

**Concept:** Finding files using size-based filters
**Difficulty:** Trivial

### What the level asks

Locate a file under the `inhere` directory that is human-readable, not executable, and exactly 1033 bytes in size.

### Solution

```bash
cd inhere
# Move into the directory tree containing the target file

find . -type f -size 1033c
# Search for regular files that are exactly 1033 bytes

cat ./maybehere07/.file2
# Read the matching file

# Password obtained:
# [REDACTED]
```

### Real-world relevance

Security analysts frequently search large filesystems for artifacts that match specific characteristics such as file size, extension, permissions, or timestamps. Efficient filtering reduces investigation time when triaging compromised systems or hunting for evidence.

```
```
