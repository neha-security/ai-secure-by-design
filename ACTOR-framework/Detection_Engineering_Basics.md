# Detection Engineering Basics

## What is Detection Engineering?

Detection engineering is the process of designing, building, and improving security detections to identify attacker behavior in systems.

---

## Why It Matters

Traditional security relies on signatures.

Modern attacks use:
- Fileless malware
- Living-off-the-land techniques
- Identity abuse

Detection engineering focuses on behavior, not just indicators.

---

## Types of Detection

### 1. Signature-based
- Known malware hashes  
- Known malicious IPs or domains  

### 2. Behavior-based
- Abnormal PowerShell execution  
- Suspicious login patterns  
- Privilege escalation activity  

---

## Example Detection Rules

- If PowerShell runs with encoded command → Alert  
- If LSASS is accessed by non-system process → Alert  
- If user logs into multiple systems quickly → Alert  

---

## Key Data Sources

- Windows Event Logs  
- EDR telemetry  
- Identity logs (Azure AD / Okta)  
- Email security logs  

---

## Goal of Detection Engineering

To detect attackers early by identifying suspicious behavior before damage occurs.
