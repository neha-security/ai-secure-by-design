# Lateral Movement Basics

## What is Lateral Movement?

Lateral movement is when an attacker uses one compromised account or device to access additional systems inside an environment.

---

## Why Attackers Move Laterally

- Reach sensitive systems
- Gain higher privileges
- Dump more credentials
- Access crown-jewel data
- Build persistence

---

## Common Methods

### Windows / Enterprise

- RDP using stolen credentials
- PsExec / SMB remote execution
- WMI remote execution
- Pass-the-Hash
- WinRM / Remote PowerShell

### Identity / Cloud

- Shared token reuse
- Privileged access across connected systems

---

## Detection Signals

- Same user logging into many hosts quickly
- RDP to unusual servers
- New remote services installed
- Admin shares accessed
- Domain controller contacted unexpectedly
- Burst of Kerberos ticket requests

---

## Important Logs

- 4624 (Logon)
- 7045 (Service creation)
- 4768 / 4769 (Kerberos)
- 4776 (NTLM)
- 4672 (Special privileges)
- 4688 (Process creation)

---

## Response Actions

- Disable affected account
- Revoke tickets/sessions
- Isolate impacted systems
- Block malicious IPs
- Review spread scope
- Preserve logs for forensics
