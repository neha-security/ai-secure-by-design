# Persistence Techniques Basics

## What is Persistence?

Persistence is the ability for an attacker to regain or maintain access after reboot, logout, or password reset.

---

## Common Windows Persistence Methods

### Scheduled Tasks
- Automatic execution at specific times or startup
- Event ID 4698 may indicate creation

### Registry Run Keys
- HKCU/HKLM Run paths launch programs at login

### Startup Folder
- Scripts or shortcuts placed in Startup path

### New Local Admin User
- Hidden privileged account for future access

---

## Identity Persistence Methods

### OAuth Consent Abuse
- Malicious app keeps access via granted tokens

### Added MFA Method
- Attacker adds own device or method

### Mailbox Rules
- Auto-forwarding sensitive emails

---

## Detection Signals

- New scheduled task creation
- Unexpected registry autorun changes
- New privileged account created
- OAuth consent to unknown app
- MFA methods changed unexpectedly

---

## Response Actions

- Revoke tokens
- Reset password
- Remove malicious apps
- Review MFA methods
- Delete persistence artifacts
- Investigate impacted systems
