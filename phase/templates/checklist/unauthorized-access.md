Unauthorized Access Response Checklist
Covers: brute force, credential stuffing, stolen credentials, insider threat, and
privilege escalation.
 First 15 Minutes
Identify the affected account(s) and system(s)
Confirm unauthorized access is genuine (not a legitimate user from a new location)
Determine if access is ongoing or historical
Disable the compromised account — do NOT delete it
Revoke all active sessions for the affected account
Notify IR Lead
Begin documenting actions and timestamps
 Investigation
Account Activity Review:
Pull full authentication logs for affected account (last 7–30 days)
Identify source IPs — are they internal, VPN, or external?
Check for off-hours or unusual geographic access
Review actions taken while attacker had access:
Files accessed, downloaded, or modified
Emails sent or forwarded
New accounts or rules created
Privilege escalation attempts
Cloud resource access
Attack Vector Analysis:
Was this a brute force attack? (review failed login attempts)
Was this credential stuffing? (check HaveIBeenPwned for account exposure)
Was this via phishing? (check if preceded by phishing incident)
Was this an insider threat? (check user behavior analytics if available)
Was MFA bypassed? (check for MFA fatigue / SIM swap / legacy auth protocol)
Was this from a compromised third party or vendor account?
Scope Analysis:
Did the attacker access only one account or multiple?
Did lateral movement occur to other systems or accounts?
Were any privileged or admin accounts accessed?
Were any cloud resources (AWS, Azure, GCP) accessed or modified?
Was any data downloaded or exfiltrated?
 Containment
Affected account(s) disabled
All active sessions and tokens revoked
VPN access revoked for affected credentials
Source IP(s) blocked at firewall (if external attack)
MFA enforced or re-enrolled on affected account
Any new accounts created by attacker disabled immediately
Email forwarding rules reviewed and removed if unauthorized
Cloud IAM access reviewed — revoke any suspicious permissions
 Eradication
Root access vector closed (patched, rule applied, account policy updated)
All attacker-created accounts removed
Unauthorized firewall rules or access policies reverted
All affected credentials reset
Legacy authentication protocols disabled if exploited (NTLM, Basic Auth)
OAuth app permissions reviewed and unauthorized apps removed
 Recovery
Legitimate user re-enrolled with MFA
Account re-enabled with new credentials
User briefed on what occurred and what to watch for
Enhanced alerting applied to account for 30 days
If insider threat: coordinate with HR and Legal before restoring access
 Notifications
Scenario
Notify
PII or sensitive data accessed
Legal, CISO, Compliance
Executive or admin account hit
CISO, Executive Leadership
Insider threat suspected
HR, Legal, Management
Regulatory data accessed
Legal (GDPR/HIPAA/PCI)
Customer data exposed
Legal, Customer Comms
 Post-Incident Improvements
Enforce MFA across all accounts if not already done
Implement Conditional Access Policies (geo-restriction, device compliance)
Review password policy — enforce complexity and breach password checking
Enable User and Entity Behavior Analytics (UEBA) if not active
Audit all service accounts and shared credentials
Review privileged access — apply least privilege principle
 Resources
HaveIBeenPwned — check for credential exposure
MITRE ATT&CK — Credential Access
CISA — Protecting Against Credential Theft
