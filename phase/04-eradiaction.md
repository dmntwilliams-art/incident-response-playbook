Phase 4: Eradication
Goal: Remove the root cause of the incident and all attacker artifacts from the
environment.
4.1 Root Cause Analysis
Before eradicating, identify how the attacker got in:
Vector
Investigation Steps
Phishing
Review email headers, identify clicked link/attachment
Stolen Credentials
Check for credential exposure on HaveIBeenPwned, dark web
Unpatched Vulnerability
Identify CVE, check patch history
Misconfiguration
Review cloud configs, exposed services, open ports
Insider Threat
Review access logs, DLP alerts, user activity
Supply Chain
Identify affected software version and blast radius
Brute Force
Review auth logs for failed attempts before success
4.2 Eradication Checklist
All malware and attacker tools removed from affected systems
Persistence mechanisms removed (registry keys, scheduled tasks, cron jobs, startup
items)
Backdoors and web shells identified and removed
Compromised credentials rotated (all affected accounts)
SSH keys and API tokens revoked and reissued
Rogue accounts or services created by attacker removed
Malicious firewall rules or routing changes reverted
Cloud resources spun up by attacker terminated
Exploited vulnerability patched or mitigated
4.3 Persistence Mechanism Checklist
Attackers commonly establish persistence via these methods — check all:
Windows:
Registry Run keys ( HKCU\Software\Microsoft\Windows\CurrentVersion\Run )
Scheduled Tasks (check Task Scheduler and schtasks /query )
Services (check for new or modified services)
Startup folder items
WMI event subscriptions
DLL hijacking or side-loading
Browser extensions
Linux/macOS:
Cron jobs ( crontab -l , /etc/cron.* )
Systemd services ( /etc/systemd/system/ )
.bashrc, .bash_profile , .profile modifications
SSH authorized_keys modifications
SUID/SGID binaries
Cloud:
IAM users, roles, or access keys created by attacker
Lambda functions or cloud functions added
New VMs or containers spun up
Logging or alerting disabled
4.4 System Rebuild vs. Clean Decision
Scenario
Recommendation
Ransomware encrypted system
Rebuild from backup
Rootkit detected
Rebuild from backup
Single malware infection, no persistence
Clean in place
Attacker had prolonged access (> 48 hrs)
Rebuild from backup
Active directory / identity provider hit
Full AD review
Cloud instance compromised
Terminate and redeploy
Rule of thumb: When in doubt, rebuild. A compromised system can never be fully
trusted.
4.5 Validation After Eradication
Rescan system with updated AV/EDR signatures
No active C2 communication observed in network logs
No suspicious processes running
All known IOCs blocked and no longer seen in logs
Affected accounts show no further unauthorized activity
 Next Phase: 
Recovery
