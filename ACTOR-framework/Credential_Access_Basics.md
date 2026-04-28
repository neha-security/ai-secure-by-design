# Credential Access Basics

## What is Credential Access?

Credential access is when attackers steal passwords, hashes, tickets, tokens, or session data to impersonate legitimate users.

---

## Why Credentials Matter

With valid credentials, attackers can log in normally and avoid many defenses.

---

## Common Techniques

### Endpoint

- LSASS dumping
- Browser password/cookie theft
- Keylogging
- SAM / NTDS theft

### Identity / Cloud

- Token theft
- Consent phishing
- Kerberoasting
- Pass-the-ticket

---

## Detection Signals

- LSASS accessed by unusual process
- Dump tools launched
- Spike in Kerberos ticket requests
- Browser credential files accessed
- New admin logins after suspicious activity
- Session reuse from new IP/device

---

## Important Logs

- 4624 / 4625 Logons
- 4672 Special privileges
- 4688 Process creation
- 4768 / 4769 Kerberos
- Sysmon 1 / 10 / 11
- Identity sign-in logs

---

## Response Actions

- Disable accounts
- Revoke sessions/tickets
- Reset passwords
- Isolate affected hosts
- Investigate lateral movement
