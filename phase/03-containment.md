Phase 3: Containment
Goal: Limit the damage and prevent the incident from spreading, without destroying
evidence.
3.1 Containment Strategy Decision
Choose the right approach based on the situation:
Strategy
When to Use
Trade-off
Immediate
Ransomware spreading, active exfiltration,
SEV-1
May tip off attacker or
lose data
Delayed
Need to observe attacker TTPs, threat
hunting in progress
Risk of further damage
Partial
Critical system can’t go offline (production,
healthcare)
Attacker retains some
access
Default: Immediate containment for any SEV-1 or SEV-2 incident.
3.2 Short-Term Containment Actions
Take these steps first to stop the bleeding:
Isolate affected host(s) — network isolation via EDR or VLAN/firewall rule
Block known malicious IPs/domains at firewall and proxy level
Disable compromised accounts — do not delete, just disable
Revoke active sessions and tokens (SSO, OAuth, VPN)
Block malicious hashes in EDR/AV
Preserve system state — take snapshot before any changes if cloud/VM
Notify IT to halt any scheduled tasks or deployments that could interfere
3.3 Long-Term Containment Actions
Once immediate spread is stopped, take longer-term steps:
Patch or compensating control applied to the exploited vulnerability
Enhanced monitoring placed on all related assets
Privileged account audit completed (check for persistence mechanisms)
Threat hunting performed on similar assets for same IOCs/TTPs
Firewall rules hardened beyond the immediate incident
MFA enforced on any affected or related accounts
3.4 Network Isolation Methods
Method
Best For
Notes
EDR Host Isolation
Single endpoint
Fastest, preserves evidence
VLAN Segregation
Multiple hosts in same segment
Requires network team
Firewall ACL Block
Blocking C2 communication
Block outbound to known bad
IPs
DNS Sinkholing
Blocking malicious domain
lookups
Fast to implement, broad
coverage
Account Disable
Compromised credentials
Don’t delete — preserve
forensics
Cloud Security
Group
Cloud instances
Use AWS SG, Azure NSG, GCP
FW
3.5 Communication During Containment
Internal stakeholders to notify:
IR Lead / SOC Manager
CISO
Affected business unit owner
IT Operations (for system changes)
Legal (if PII or regulated data involved)
Do NOT:
Discuss the incident on unsecured channels
Send details via regular email if email may be compromised
Notify external parties without legal/executive approval
3.6 Containment Evidence Log
Document every action taken:
Timestamp
(UTC)
Action Taken
Performed
By
[datetime]
Host isolated via
CrowdStrike
System/Account
Affected
[Analyst]
[datetime]
Account disabled in AD
DESKTOP-ABC123
[IT Admin]
[datetime]
Firewall rule added blocking
1.2.3.4
jsmith@company.com
[NetEng]
Perimeter FW
 Next Phase: 
Eradication
