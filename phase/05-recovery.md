Phase 5: Recovery
Goal: Safely restore systems to normal operations and validate the environment is
clean.
5.1 Recovery Prerequisites
Do NOT begin recovery until all of the following are true:
Root cause has been identified and documented
All attacker artifacts and persistence mechanisms removed
Exploited vulnerability has been patched or mitigated
Affected credentials have been rotated
Enhanced monitoring is in place for affected systems
Legal and compliance teams have been notified (if required)
Business owner has approved return to service
5.2 System Restoration Steps
Step
Action
1
Identify clean backup (prior to compromise date)
2
Restore from backup in isolated environment first
3
Validate backup integrity and scan for malware before deployment
4
Apply all security patches before reconnecting to network
5
Reconnect to network with enhanced monitoring active
6
Monitor closely for 24–72 hours post-restoration
7
Confirm normal business operations with system owner
5.3 Credential & Access Recovery
All compromised passwords reset (enforce new password policy)
MFA re-enrolled for all affected accounts
API keys and service account credentials rotated
OAuth tokens and SSO sessions revoked and reissued
Privileged access reviewed — remove any accounts that shouldn’t have it
PAM (Privileged Access Management) audit completed
5.4 Monitoring During Recovery
Place enhanced monitoring on recovered systems for a minimum of 72 hours:
What to Monitor
Tool
Alert On
Process execution
EDR
Any anomalous or new processes
Network connections
SIEM / NDR
C2 IOCs, new external
connections
Authentication events
SIEM
Failed logins, off-hours access
File system changes
EDR / FIM
Changes to system directories
Cloud resource
changes
CloudTrail / Activity
Logs
New IAM, compute, storage
events
5.5 Communication & Stakeholder Update
Internal:
Notify executive team that systems are restored
Brief affected business units on what occurred and steps taken
Update IR ticket with closure details
External (if applicable):
Notify affected customers per regulatory requirements
File required regulatory reports (GDPR 72hr, SEC 8-K, etc.)
Engage cyber insurance carrier with incident documentation
Notify law enforcement if criminal activity involved (FBI IC3, CISA)
5.6 Recovery Validation Checklist
All systems restored and operational
Business functions operating normally
No further malicious activity detected
All IOCs remain blocked
Enhanced monitoring in place and active
Stakeholders notified and satisfied
Incident ticket updated and ready for closure
 Next Phase: 
Lessons Learned
