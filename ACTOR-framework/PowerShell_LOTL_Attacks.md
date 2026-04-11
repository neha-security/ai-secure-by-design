# PowerShell & Living-Off-The-Land Attacks

## What is Living-Off-The-Land?

Living-Off-The-Land (LOTL) means attackers use built-in operating system tools instead of malware.

Examples:
- PowerShell
- cmd
- WMIC
- rundll32
- mshta

This helps attackers avoid traditional antivirus detection.

---

## Why Attackers Use PowerShell

PowerShell is trusted, powerful, and already installed on Windows systems.

Attackers use it to:

- Run hidden commands
- Download scripts from internet
- Execute code in memory
- Create persistence
- Move laterally

---

## Common Suspicious PowerShell Switches

- `-nop` = NoProfile
- `-w hidden` = Hidden window
- `-enc` = Encoded command

These may indicate malicious activity.

---

## Detection Signals

- powershell.exe launched by Office apps
- Encoded command line usage
- Hidden PowerShell window
- Network connections after PowerShell start
- DNS requests to unusual domains
- PowerShell spawning child processes

---

## Important Logs

- Windows Event ID 4688 (Process Creation)
- Sysmon Event ID 1 (Process Creation)
- PowerShell Script Block Logging (4104)
- DNS logs
- Proxy / Firewall logs

---

## Example Detection Rule

If PowerShell starts with `-enc` OR `-w hidden`
AND network connection occurs within 1 minute

THEN raise alert for possible LOTL attack.
