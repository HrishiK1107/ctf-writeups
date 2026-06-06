## Bandit Level 16 → Level 17

**Concept:** Service Enumeration, SSL/TLS Communication, and SSH Key Authentication

**Difficulty:** Non-trivial

## What the level asks

The credentials for the next level can be retrieved by submitting the current Bandit16 password to the correct service listening on localhost between ports `31000` and `32000`. The challenge requires identifying which ports are open, determining which services use SSL/TLS, and finding the one service that returns credentials instead of simply echoing input.

## Approach

The first step was identifying which services were running within the specified port range. Rather than testing every port manually, I performed an Nmap scan with service detection enabled. The scan revealed several open ports, including multiple SSL-enabled services.

Since the challenge specifically mentioned SSL/TLS, I focused on the ports identified as SSL services. I then used OpenSSL's client utility to interact with these services and submit the current Bandit16 password.

One of the services responded with an RSA private key instead of echoing the supplied input. This indicated that the correct service had been found and that the returned private key would be required for authentication to the next level.

I copied the private key to my Kali Linux system, saved it as a file, and applied the correct permissions. Using the SSH client's `-i` option, I authenticated successfully as Bandit17 and retrieved the next password.

## Solution

```bash
nmap -sV -T4 -p 31000-32000 localhost
# Enumerate open ports and identify services running in the target range
```

Relevant results:

```text
31046/tcp open  echo
31518/tcp open  ssl/echo
31691/tcp open  echo
31790/tcp open  ssl/unknown
31960/tcp open  echo
```

Submit the current password to the SSL-enabled service:

```bash
echo "<bandit16_password>" | openssl s_client -connect localhost:31790 -quiet
# Connect to the SSL service and submit the current password
```

The service responds with:

```text
Correct!
-----BEGIN RSA PRIVATE KEY-----
...
-----END RSA PRIVATE KEY-----
```

Save the private key locally:

```bash
mkdir bandit17
cd bandit17

nano private.key
# Paste the RSA private key into the file

chmod 600 private.key
# Restrict permissions so SSH accepts the key
```

Authenticate as Bandit17:

```bash
ssh -i private.key bandit17@bandit.labs.overthewire.org -p 2220
# Login using the retrieved RSA private key

whoami
# Verify the authenticated user

cat /etc/bandit_pass/bandit17
# Retrieve the next password

# Password obtained:
# [REDACTED]
```

### Screenshot

![Nmap Port Discovery](assets/nmap-port-discovery.png)

**Caption:** Enumerating services running on localhost between ports 31000 and 32000.

**Explanation:** Nmap identified several open services, including SSL-enabled ports. These results narrowed the investigation to the services most likely to return credentials.

### Screenshot

![RSA Private Key Retrieved](assets/private-key-retrieved.png)

**Caption:** Retrieving an RSA private key from the SSL service.

**Explanation:** After the correct password was submitted through an encrypted connection, the service returned an RSA private key rather than echoing the input, indicating that the correct service had been identified.

### Screenshot

![SSH Login Using Private Key](assets/private-login.png)

**Caption:** Authenticating to Bandit17 using the retrieved private key.

**Explanation:** The RSA private key was saved locally, secured with appropriate permissions, and supplied to the SSH client. Successful authentication confirmed that the retrieved key granted access to the Bandit17 account.

## Real-World Relevance

This level combines several skills commonly used during security assessments and incident response. Service enumeration is a fundamental reconnaissance technique used to identify exposed applications and protocols. SSL/TLS inspection is frequently required when analyzing encrypted services, while SSH key-based authentication is widely used in Linux administration, cloud infrastructure, and DevOps environments. Understanding how to enumerate services, interact with encrypted applications, and securely handle private keys is essential for both offensive and defensive security work.
