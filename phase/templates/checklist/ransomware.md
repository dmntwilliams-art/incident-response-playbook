Ransomware Response Checklist
SEV-1 — Activate IR team immediately. Time is critical.
 First 15 Minutes
Confirm ransomware activity (encrypted files, ransom note, EDR alert)
Identify affected hosts — how many? Which segments?
Immediately isolate all affected hosts from the network (EDR isolation or pull
network cable)
Page IR Lead and SOC Manager NOW
Do NOT reboot affected systems — preserves memory artifacts
Do NOT pay the ransom without legal and executive approval
Begin documenting all actions with timestamps
 First Hour — Investigation & Containment
Identify the ransomware variant (check ransom note, file extension, VirusTotal hash)
Determine Patient Zero — which host was infected first?
Identify initial infection vector (phishing, RDP brute force, vulnerable software)
Determine blast radius — scan for encrypted files across network shares
Check for data exfiltration BEFORE encryption (many groups use double extortion)
Isolate network shares and backup systems to prevent encryption spread
Block ransomware C2 domains/IPs at firewall
Disable affected accounts — do not delete
Notify CISO and executive leadership
 Containment Actions
All affected endpoints isolated
Network shares taken offline or access restricted
Backup systems isolated (prevent backup encryption)
RDP disabled or restricted if used as attack vector
All privileged accounts audited and suspicious ones disabled
Domain controller checked for compromise
Cloud environments checked for lateral movement
 Investigation
Collect memory dumps from affected systems before any changes
Export SIEM logs for the 72-hour window prior to detection
Retrieve EDR telemetry and process tree from Patient Zero
Check email logs for phishing delivery
Check VPN and authentication logs for unauthorized access
Map attacker TTPs to MITRE ATT&CK
Identify all compromised accounts and systems
Determine if data was exfiltrated (check DLP, proxy, firewall egress logs)
 Eradication
All encrypted systems identified
Ransomware payload and all related artifacts removed
Persistence mechanisms removed (scheduled tasks, services, registry keys)
All compromised credentials rotated
Initial access vector closed (patched vulnerability, disabled exposed RDP, etc.)
Scan all remaining systems for indicators of compromise
 Recovery
Identify clean backup — confirm backup predates infection
Verify backup integrity before restoration
Restore in isolated environment and scan before reconnecting
Patch all systems before returning to network
Confirm normal operations with business owner
Enhanced monitoring active for 72 hours post-recovery
 Notifications
Who
When
By Whom
IR Lead / CISO
Immediately
Analyst
Executive Leadership
Within 1 hour
IR Lead
Legal
Within 1 hour (PII involved)
Cyber Insurance Carrier
Within 24 hours
IR Lead
Legal / CISO
Law Enforcement (FBI IC3)
Optional — discuss with Legal
Regulators (if required)
CISO
Per regulatory timeline
Affected Customers
Per legal guidance
Legal
Legal / Comms
 Do NOT Do
 Do not reboot infected systems before memory is captured
 Do not pay the ransom without legal and executive sign-off
 Do not delete the ransom note — it contains valuable forensic info
 Do not restore from backup before eradicating the threat
 Do not use regular email to communicate if email is compromised
 Do not make public statements without approval from Legal/PR
 Resources
No More Ransom Project — free decryptors
ID Ransomware — identify the variant
CISA Ransomware Guide
FBI Ransomware Reporting
