# Krypton Level 0 → 1

**Concept:** Base64 Decoding
**Difficulty:** Trivial
**Tools Used:** base64

---

## What the level gives you

The level provides a Base64-encoded string:

```text
S1JZUFRPTklTR1JFQVQ=
```

The objective is to decode the string and use the resulting value as the password for the `krypton1` account.

## Cipher explanation

Base64 is an encoding scheme used to represent binary data using printable ASCII characters. It is commonly used when binary data needs to be transmitted through systems that only support text.

Base64 is not encryption because it does not require a key. Anyone who knows the encoding scheme can reverse it and recover the original data.

## Solution

```bash
# Decode the Base64 string
echo S1JZUFRPTklTR1JFQVQ= | base64 -d

# Output:
# KRYPTONISGREAT
```

## Screenshot

![Base64 Decode](assets/level-00-base64-decode.png)

## Real-world relevance

Base64 is frequently encountered during malware analysis, web application testing, JWT inspection, email analysis, and API debugging. Security analysts often decode Base64-encoded payloads to reveal hidden commands, configuration data, or embedded malware artifacts.