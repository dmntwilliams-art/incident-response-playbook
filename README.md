# incident-response-playbook

A structured, practitioner-built Incident Response (IR) Playbook aligned with NIST SP
800-61 and real-world SOC operations. Designed for security analysts, IR teams, and
SOC leads.
 Repository Structure
ir-playbook/
├── README.md                   
├── phases/
│   
├── 01-preparation.md       
│   
│   
│   
│   
│   
├── 02-identification.md    
├── 03-containment.md       
├── 04-eradication.md       
├── 05-recovery.md          
← You are here
← Team readiness, tools, contacts
← Detection, triage, classification
← Short & long-term containment
← Root cause removal
← Restoration and validation
└── 06-lessons-learned.md  ← Post-incident review
├── templates/
│   
│   
├── incident-ticket.md      
└── executive-summary.md   
└── checklists/
├── ransomware.md           
├── phishing.md             
← Incident documentation template
← Leadership communication template
← Ransomware response checklist
← Phishing response checklist
└── unauthorized-access.md ← Unauthorized access checklist
 IR Lifecycle (NIST SP 800-61)
[Preparation] → [Identification] → [Containment] → [Eradication] → [Recovery] → [Lessons Learned]
↑_______________________________________________________________|
 Purpose
This playbook provides:
Step-by-step response procedures for common incident types
Documentation templates for consistent record-keeping
Escalation paths and communication frameworks
Post-incident review processes to improve defenses
 Severity Classification
Severity Label Description Response
SLA
SEV-1 Critical Active breach, data exfiltration, ransomware Immediate
SEV-2 High Confirmed compromise, lateral movement
detected < 1 hour
SEV-3 Medium Suspicious activity, policy violation < 4 hours
SEV-4 Low Anomaly flagged, investigation needed < 24 hours
 Core Tools Referenced
Category Tools
SIEM Splunk, Microsoft Sentinel, QRadar
EDR CrowdStrike, SentinelOne, Defender
Threat Intel VirusTotal, MISP, OpenCTI
Network Analysis Wireshark, Zeek, Suricata
Forensics Velociraptor, FTK, Autopsy
 References
NIST SP 800-61 Rev 2
MITRE ATT&CK Framework
SANS Incident Handler’s Handbook
