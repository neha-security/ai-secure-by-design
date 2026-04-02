Identity Attacks Basics
What are Identity Attacks?

Identity attacks occur when attackers compromise or misuse user credentials, tokens, or sessions to gain unauthorized access.

# Common Identity Attacks
1. Token Theft
Attacker steals authentication token
No password required
Used to access systems silently
2. Session Hijacking
Attacker reuses session cookies/tokens
Bypasses authentication
3. MFA Fatigue Attack
Multiple MFA prompts sent
User eventually approves
Attacker gains access

#Detection Signals
Multiple MFA failures followed by success
Login from different geographies
Token usage without authentication event
Multiple active sessions from different locations

# Response Actions
Revoke tokens
Force password reset
Block suspicious IP
Investigate accessed resources
