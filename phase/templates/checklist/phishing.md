Phishing Response Checklist
Phishing is the #1 initial access vector. Speed matters — act before credentials are
used.
 First 15 Minutes
Obtain the suspicious email (as .eml or .msg file — do NOT click any links)
Identify who received the email — is it targeted or a broad campaign?
Determine if any recipients clicked the link or opened the attachment
Pull email headers (check sending IP, reply-to, SPF/DKIM/DMARC results)
Analyze the email safely (use a sandbox — ANY.RUN, Hybrid Analysis, or VirusTotal)
Quarantine/delete the email from all inboxes immediately
 Investigation
Email Analysis:
Sender address and domain (is it spoofed or lookalike?)
Reply-to address (does it differ from sender?)
Links in the email — where do they redirect? (defang before sharing)
Attachments — hash the file and submit to VirusTotal/sandbox
Email headers — check originating IP, authentication results
Check if domain/IP is in threat intel feeds
Recipient Analysis:
Pull list of all recipients from email gateway
Identify who clicked the link (proxy/web filter logs)
Identify who opened the attachment (EDR telemetry)
Identify who submitted credentials (if credential harvest site)
Impact Analysis:
Were credentials entered on a phishing page?
Was a malicious attachment opened? Any process execution?
Any post-click activity: malware download, macro execution, C2 callback?
Is this a Business Email Compromise (BEC) attempt?
 Containment
If credentials were entered:
Reset password immediately for all affected accounts
Revoke all active sessions (SSO, O365, VPN, etc.)
Enable MFA immediately if not already active
Check account for forwarding rules, delegates, or sent items (BEC indicator)
Review account activity for the past 24–72 hours
If attachment was opened / malware executed:
Isolate the endpoint via EDR
Escalate to malware response process
Pull process tree from EDR for the suspicious process
Check for lateral movement from affected host
For all phishing incidents:
Block sender domain and IP at email gateway
Block phishing URL at web proxy and DNS filter
Submit URL/domain to Google Safe Browsing and Microsoft SmartScreen
Block malicious file hash in EDR
 Eradication
All malicious emails removed from all inboxes
Malware removed (if attachment was executed)
Compromised accounts secured
All IOCs blocked
Email gateway rules updated to block similar campaigns
 Communication
Notify affected users — let them know what to look for
Send organization-wide alert if it was a broad campaign
Notify management if sensitive accounts were targeted
File report with email security vendor if applicable
Notify legal if PII credentials were compromised
 Post-Incident Improvements
Update email gateway rules/signatures
Consider additional DNS filtering for newly registered domains
Add phishing campaign to security awareness training
Review and tune DMARC/DKIM/SPF policies
Consider deploying anti-phishing tool (e.g., Proofpoint, Abnormal Security)
 Analysis Resources
VirusTotal — file and URL analysis
ANY.RUN — interactive malware sandbox
MXToolbox — email header analysis
URLScan.io — safe URL scanning
PhishTank — community phishing database
