# Privilege Escalation Basics

## What is Privilege Escalation?

Privilege escalation is when an attacker gains higher access than originally granted, such as moving from standard user to administrator.

---

## Why Attackers Do It

Higher privileges allow attackers to:

- Access sensitive systems
- Disable security tools
- Dump credentials
- Move laterally
- Create persistence
- Exfiltrate data at scale

---

## Common Methods

### Endpoint / Windows

- Misconfigured services
- Local privilege escalation vulnerabilities
- Credential reuse
- Token impersonation

### Identity / Cloud

- Admin role assignment abuse
- OAuth app with elevated permissions
- Misused privileged access workflows

---

## Detection Signals

- New admin group membership changes
- Unexpected privileged role assignments
- Antivirus / EDR disabled after elevation
- Access to sensitive servers after new privilege
- Special privilege logon events
- Sudden burst of admin actions

---

## Important Logs

- 4728 / 4732 / 4756 Group membership changes
- 4624 / 4625 Logons
- 4672 Special privileges assigned
- 4688 Process creation
- 4663 Object access
- Cloud admin audit logs

---

## Response Actions

- Disable affected account
- Revoke sessions / tokens
- Reset credentials
- Remove unauthorized privileges
- Isolate impacted devices
- Review scope of actions taken
