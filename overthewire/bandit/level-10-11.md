## Bandit Level 10 → 11

**Concept:** Decoding Base64-encoded data

**Difficulty:** Trivial

### What the level asks

Retrieve the password stored in a file containing Base64-encoded data.

### Solution

```bash
cat data.txt
# Inspect the file contents and identify the Base64-encoded string

base64 -d data.txt
# Decode the Base64 data and reveal the original plaintext

# Password obtained:
# [REDACTED]
```

### Real-world relevance

Base64 encoding is commonly encountered in web applications, email protocols, API communications, cloud configurations, and security logs. Security analysts regularly decode Base64 content when investigating encoded payloads, authentication tokens, phishing artifacts, and malware communications.
