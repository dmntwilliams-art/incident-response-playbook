Incident Ticket Template
Copy this template for every new incident. Fill in all sections as information becomes
available.
Incident Overview
Field Value
Incident ID INC-[YYYY-MM-DD]-[###]
Date/Time Opened [UTC datetime]
Date/Time Closed [UTC datetime]
Severity SEV-1 / SEV-2 / SEV-3 / SEV-4
Incident Type Malware / Phishing / Unauthorized Access / Data Breach / Other
Status Open / Contained / Eradicated / Closed
IR Lead [Name]
Assigned Analyst [Name]
Affected Systems
Hostname /
IP OS Owner /
Department Criticality Action Taken
[hostname] [OS] [Owner] High/Med/Low [Isolated / Rebuilt /
Monitored]
Affected Accounts
Username Account Type Domain / System Action Taken
[user] Admin / User [domain] Disabled / Reset PW
Incident Description
Provide a factual, chronological summary of what happened:
[Write 2–5 sentences describing how the incident was discovered, what systems/data
were involved, and the nature of the threat.]
Initial Indicators (IOCs)
Type Value Source
IP Address 192.168.x.x / 1.2.3.4 SIEM / EDR
Domain malicious-domain[.]com Proxy logs
File Hash abc123def456… (MD5/SHA256) EDR
Email Sender attacker@domain[.]com Email gateway
URL hxxps://malicious[.]com/path Web proxy
Use defanged notation for IOCs: replace . with [.] and http with hxxp
MITRE ATT&CK Mapping
Tactic Technique ID Technique Name
Initial Access T1566.001 Spearphishing Attachment
Execution T1059.001 PowerShell
Persistence T1053.005 Scheduled Task
Command & Control T1071.001 Web Protocols
Reference: https://attack.mitre.org/
Actions Taken
Timestamp
(UTC) Phase Action Performed
By
[datetime] Identification Alert triaged, confirmed TP [Analyst]
[datetime] Containment Host isolated via EDR [Analyst]
[datetime] Eradication Malware removed, creds reset [Analyst]
[datetime] Recovery System restored from clean
backup [IT Ops]
Evidence Collected
Evidence Item Location / Hash Collected
By
Date/Time
(UTC)
Memory dump - DESKTOP
ABC123
\evidence-share\INC
001 [Analyst] [datetime]
SIEM log export (72hr
window)
\evidence-share\INC
001 [Analyst] [datetime]
Email .eml file \evidence-share\INC
001 [Analyst] [datetime]
Root Cause
[Describe the root cause once determined. Example: “Attacker sent a spearphishing
email with a malicious macro-enabled Word document. The user opened the
attachment, which executed a PowerShell download cradle, establishing a C2
connection via HTTPS to 1.2.3.4.”]
Business Impact
Impact Category
Details
Systems Affected
X endpoints, X servers
Downtime
X hours of production downtime
Data Exposed
Yes / No — [describe if yes]
Financial Impact
Estimated $X
Regulatory Impact
Yes / No — [GDPR / HIPAA / PCI if yes]
Closure Summary
Brief statement confirming the incident has been fully remediated and the environment
is clean.
Incident Closed By: [Name]
Closure Date/Time (UTC): [datetime]
Approved By: [IR Lead / Manager Name]
