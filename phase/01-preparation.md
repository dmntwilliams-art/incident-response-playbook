Phase 1: Preparation
Goal: Ensure the organization is ready to respond to incidents before they occur.
1.1 IR Team Roles & Responsibilities
Role Responsibility
IR Lead Coordinates response, owns communication, makes decisions
Security Analyst Performs triage, investigation, and containment actions
Threat Intel Analyst Provides context on TTPs, threat actors, IOCs
IT/Sysadmin Executes technical containment (isolation, patching)
Legal/Compliance Advises on regulatory obligations, evidence handling
Communications/PR Manages external messaging if breach becomes public
Executive Sponsor Authorizes major decisions (e.g., take down production)
1.2 Contact Directory (Template)
 Replace placeholders with actual contacts before deployment.
Name Role Phone Email Availability
[Name] IR Lead [Phone] [Email] 24/7
[Name] SOC Manager [Phone] [Email] Business hours
[Name] Legal Counsel [Phone] [Email] On-call
[Name] CISO [Phone] [Email] 24/7
1.3 Required Tools & Access
Verify the following are operational and accessible before an incident:
SIEM access confirmed (Splunk / Sentinel / QRadar)
EDR console access confirmed (CrowdStrike / SentinelOne)
Network tap or PCAP capability available
Forensic workstation ready with licensed tools
Isolated response network segment available
Incident ticketing system accessible (Jira / ServiceNow)
Secure communication channel established (Signal / encrypted Slack)
Evidence storage location defined and accessible
Backup and recovery systems verified operational
1.4 Pre-Incident Documentation
Ensure the following are documented and current:
Network topology and asset inventory
Critical asset register (crown jewels)
Data flow diagrams
Cloud environment architecture
Third-party and vendor access list
Regulatory and compliance requirements (PCI, HIPAA, SOC2)
1.5 Training & Exercises
Activity
Frequency
Last Completed
Tabletop Exercise
Quarterly
Owner
[Date]
Red Team / Purple Team
Annually
IR Lead
[Date]
Security
Phishing Simulation
IR Playbook Review
Monthly
Semi-annually
[Date]
Security
[Date]
IR Lead
1.6 Legal & Regulatory Prep
Understand breach notification timelines: GDPR (72 hrs), HIPAA (60 days), PCI DSS
Establish relationship with outside legal counsel specializing in cyber incidents
Know your cyber insurance policy: what’s covered, who to call first
Understand chain of custody requirements for digital evidence
 Next Phase: 
Identification
