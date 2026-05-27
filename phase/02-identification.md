Phase 2: Identification
Goal: Detect, triage, and classify the incident accurately and quickly.
2.1 Detection Sources
Incidents may be identified through:
Source
Examples
SIEM Alerts
Correlation rules, threshold alerts, anomaly detections
EDR Telemetry
Malicious process execution, memory injection, C2 beaconing
User Reports
Phishing emails, locked files, unusual system behavior
Threat Intelligence
External IOC matches, vendor alerts, dark web mentions
Third-Party Notification
MSSP alerts, law enforcement, partner organizations
Automated Scanners
Vulnerability scanners, IDS/IPS triggers
2.2 Initial Triage Questions
When an alert or report comes in, answer these immediately:
1. What system(s) are affected? (hostname, IP, owner, criticality)
2. What is the nature of the activity? (malware, unauthorized access, data exfil,
DDoS)
3. When did this start? (first seen timestamp, log correlation)
4. Is this activity ongoing or historical?
5. What data or systems are at risk? (PII, financial, IP, infrastructure)
6. Is there any indication of lateral movement?
7. What is the blast radius? (single host vs. network-wide)
2.3 Severity Classification
Severity Criteria Action
SEV-1 Active ransomware, confirmed data exfiltration, critical
system down
Immediate all
hands
SEV-2 Confirmed compromise, C2 communication, lateral
movement
Page IR Lead
now
SEV-3 Suspicious behavior, policy violation, unconfirmed
compromise
Analyst
investigation
SEV-4 Anomaly, low-fidelity alert, needs review Queue for
review
2.4 Incident Classification
Type Description
Malware Virus, ransomware, trojan, spyware, worm
Phishing Credential theft, BEC, spear phishing
Unauthorized Access Brute force, credential stuffing, insider threat
Data Breach Confirmed exfiltration of sensitive data
Denial of Service DDoS, resource exhaustion
Insider Threat Malicious or negligent employee activity
Supply Chain Compromise via third-party software or vendor
Cloud Misconfiguration Exposed S3 bucket, open storage, misconfigured IAM
2.5 Evidence Collection Checklist
Collect and preserve the following before making any changes to affected systems:
Full memory dump (if active compromise)
System logs (Windows Event Logs, Syslog, auth.log)
SIEM query exports for the relevant timeframe
EDR process tree and telemetry
Network flow data (NetFlow, PCAP if available)
Relevant email headers (for phishing)
Browser history and artifacts (if relevant)
Cloud audit logs (CloudTrail, Azure Activity Logs, GCP Audit)
Screenshot of alerts and dashboards (timestamped)
 Document the chain of custody for all evidence collected. Note: who collected it,
when, from where, and how it was stored.
2.6 Escalation Decision Tree
Alert received
│
▼
Is it a true positive?
├── No  → Document as false positive, tune rule, close ticket
└── Yes ▼
Is a system actively compromised?
├── No  → Assign SEV-3/4, begin investigation
└── Yes ▼
Is sensitive data at risk or lateral movement detected?
├── No  → Assign SEV-2, notify IR Lead
└── Yes → Assign SEV-1, activate full IR team NOW
 Next Phase: 
Containment
