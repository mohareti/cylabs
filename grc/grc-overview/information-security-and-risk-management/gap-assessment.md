# Gap Assessment

* Designing Secure Information Systems
* Threat Modeling organization
* Secure design principles
* Architectural Vulnerabilities
* Cyber security models
* "We can't have a risk without a threat and threat actor, along with asset and vulnerability"
* Who attacks critical infrastructure
* Geopolitical situation
* What kind of disruption they can create
* Which threat groups
* Classifying threat actors and groups
* Insider risks what we have
* Threats
* Threat actor
* State sponsored actors
* Advanced persistent threats
  * Gain access
  * Elevate privileges
  * Maintain access
  * Exfiltrate data
  * Undetected /stealth
* Vulnerabilities
  * Physical threats
  * Software vulnerabilities
* System exploitation methods
  * Keyloggers
  * Malwares
  * Spyware
  * Viruses
  * Worms
  * Adware
  * Browser hijackers
  * Ransomware
  * Spyware
  * Keylogger
  * Logicbombs
  * Zerodays
  * phishing
* Elevated privileges
* Patches and patch management
* Exploits
* Exploit kits
* Root kits
* Boot kits
* Botnets
* Zombies
* DDOS\
  DOS
* P2P bonets
* Agencies
  * DOD
  * FBI
  * CISA
* IT Landscape
  * On prems
  * Cloud services - shared responsibility model
  * Thin client
  * Thick client
  * Web apps
    * owasp
  * Mobile apps
* Assessing and mitigating vulnerabilities
  * Penetration testing
* Single point of failure
* Detective controls
  * Siem
  * Security and Risk management current policies and requirements
    * What are our security policies
      * For example: bring your own device
  * Which compliance we follow
  * What/which operations are critical for us ?
  * What are our current cyber risk ?
  * Do we have cyber insurance ?
  * What is our Risk Management strategy ?
  * How we are conducting Risk assessment ? How we are measuring that ?
  * What is our current Risk score ?
  * How we are calculating Risks
  * Which applications we are using for Risk scores
    * Bitsight
    * Security scorecard
    * Immuniweb
  * What is our current security score card review ?
  * Requirement to get cyber insurance ?
  * Which encryption used at rest ?
  * How we are achieving separation of duties
  * How we achieving least privileges
    * PAM
  * Data classification policies on O365
  * Do we have list of software Assets information ?
  * Data loss prevention
  * What are our data retention policies
  * Data security policies
    * Data in transit
    * Which encryption used at Transit ?
      * Which TLS version is used in our org ?
      * Is still SSL is in use ?
    * Data at rest
    * Data in use
  * Do we have Asset inventory ? Asset classification ?
    * What are risks associated with them
    * Threats and vulnerabilities
    * Do we have cloud assets ? Whats our visibility
  * Do we have CMDB ?
  * What is our Vulnerability Management Program strategies ?
  * What is our Zero day vulnerability remediation policy ?
  * What is our vulnerability remediation policy ?
  * How we are testing vulnerabilities ?
  * How we communicate with patch management tool ?
  * Which patch management tool we are using
  * Which vulnerability tool used by us
    * Tenable
    * Qualys
    * MS ATP defender
    * Sentinel one
  * Is it on prem or cloud
  * Which vulnerabilities
    * 30 days old
    * 60 days old
    * 90 days old
    * Critical ? High ? Medium ?
  * What is our threat hunting methodology ?
  * How we handle security events and security incidents?
    * Do we have on call, emergency bridge ?
    * Whom we need to involve
  * Which privacy/security compliances we comes under
    * GDPR
    * NIST
    * CISA
    * PCI
    * ISO standards
    * Defense in depth
    * Zero Trust
    * CIS
    * OWASP Top 10
  * Service level agreements
  * Vendor security assessment questionnaire
  * DDOS protection
  * Ransomware protection
  * Incident response plans
  * Business continuity Management
* Preventive security controls
  * Security Policies
  * Physical security policies
  * Do we have security awareness training
    * On boarding training
    * Quarterly training
  * Data encryption
  * Writing weak passwords
* Deterrent Security controls
  * Firewalls
  * Encryption
* Technical/logical controls
  * Encyption
  * TPM on assets
* Detective security controls
  * Log management
    * SIEM/SOC/SOAR
  * Honey Pots/deception technology
* Corrective security controls
  * Antivirus/endpoint
  * IDS/IPS
  * Business continuity plans
* Recovery controls
  * Backup copies
  * Sever clustering
* Risk Frameworks
  * Security and risk management
  * Asset Security
  * Security Engineering
  * Communication and Network Security
  * Identity and Access Management
  * Security Assessment and Testing
  * Security Operations
  * Software Development Security
* Threat Modeling
  * STRIDE
  * DREAD
  * MART
  * Who attacking organization
  * Which threat actors are targeting us
  * Which state sponserd attackingus
  * Which attackers industry
  * Which APT's
  * STOP Ransomware
* Security Operations
  * SOC
  * Red Team
  * Blue Team
  * Penetration Testing
  * Purple Teaming
* Disaster Recovery and Business Continuity plan
* Asset Security
  * Classification of assets
* Data:
  * Data retention policies
    * Emails
    * Documents
    * SLA's
  * Which data to use
  * Data in rest : encryption methods
  * Data in motion : https
* NIST SP 800-53
* FIPS
* Network OSI model
* TCP/IP Model
* WAF
* Load Balancers
* Vulnerability Scanners
* Logging
* SIEM
* SOC
* ToDo:
* Know be 4 reporting
* MS ZAP phishing email analysis , email address for notification
* We need a sandbox form MS or Knowbe4
* Need knowbe4 review and setup a meeting
* Need to verify EXO-ATP with emails malware/phish explorer
* What is KB4 campaign\

* Reporting/metrics:
* How many phishing emails we are receiving to Knowbe4 Phish ER
* How many users reported
* Which users targeted most
* What kind of the payload/malwares are used for phish campaign
* Which geo location
  * ITS Cyber Security Team runs  and document the periodical cyber gap assessment findings.
    * Cyber Hygiene is highest Priority
    * Organization Assests, Data and User's Information is highest Priority
  * Impact Analysis Police/DPS
    * Fire/Training
    * Dispatch system
    * Radio systems
    * Terminals
    * Account department
    * IRMS
    * Critical Assests
  * Data classification
  * Data backup review
* Cyber Gap Assessment:
  * Email Security:
    * Email security Gateway configurations
    * SPF, DKIM, DMARC
    * Reviewing quarantined emails
  * User Access control  and activity
    * Enforce MFA
    * use least privileges or just-enough privilege
    * implementing Privileged Access Management (PAM) and Privileged Identity Management (PIM)
    * Delete unused Accounts
    * Delete unused email addresses
    * Strong Password policies
    * A\_ (Administrative account) review
    * Third  party company/service providers access review
    * Striping local admin privileges
    * Domain admin permissions review
    * Domain shares permission review
  * Backups
    * Visibility to security team
      * Do we getting the logs
      * How access management verified or audited
    * Backup recovery testing
  * Endpoint Security
    * Applications Whitelist
    * EDR/XDR coverage
      * Mobile Devices
      * Workstations
      * Laptops
      * Servers
      * Cloud
    * Restrict the use of scripting to approved users.
    * Disabling the Macro execution
  * Wireless
    * How Guest and corporate network segregated
      * Who is running the test and audit
  * Vulnerability Management
    * Patch and update all software, OSs (including network devices) to the latest supported versions.
  * Firewall/IDS/IPS/WAF
    * Configuration review
    * What is the scope
    * Block access to malicious sites
    * Rouge assets detection
    * SMB outbound
    * RDP connections
    * SSH connections
  * Network security
    * network segmentation audit
    * allow trusted devices on your network.
  * Domain Controllers Audit:
    * Domain Controllers (DCs) CIS benchmark
  * Cloud Assests
    * Cloud Posture Management
  * Security Awareness program
  * Vendor Risk Management (VRM) program
  * Incident Response Plan and strategy
    * Disaster Recovery plan
    * Incident Response Plan
    * What is asset and network quarantine strategy
  * Log Management
  * Recovery strategy
* Ransomware Prevention audit:
  * Bridged Networks using NIC's
  * Network scanning detection
  * BYOD
  * Open RDP
  * No endpoint
  * Unpatched assets
  * No backup strategy and policies
  * No 2fa
  * No network segmentation
* Perimeter devices that are accessible via the internet - including firewalls, virtualization solutions and virtual private network devices
* CVE-2022-22954
* CVE-2022-1388
* CVE-2021-44228
*  DDoS or a destructive ICS attack
* Financial gains/Ransomware
* Designing Secure Information Systems
* Threat Modeling organization
* Secure design principles
* Architectural Vulnerabilities
* Cyber security models
* "We can't have a risk without a threat and threat actor, along with asset and vulnerability"
* Who attacks critical infrastructure
* Geopolitical situation
* What kind of disruption they can create
* Which threat groups
* Classifying threat actors and groups
* Insider risks what we have
* Threats
* Threat actor
* State sponsored actors
* Advanced persistent threats
  * Gain access
  * Elevate privileges
  * Maintain access
  * Exfiltrate data
  * Undetected /stealth
* Vulnerabilities
  * Physical threats
  * Software vulnerabilities
* System exploitation methods
  * Keyloggers
  * Malwares
  * Spyware
  * Viruses
  * Worms
  * Adware
  * Browser hijackers
  * Ransomware
  * Spyware
  * Keylogger
  * Logicbombs
  * Zerodays
  * phishing
* Elevated privileges
* Patches and patch management
* Exploits
* Exploit kits
* Root kits
* Boot kits
* Botnets
* Zombies
* DDOS\
  DOS
* P2P bonets
* Agencies
  * DOD
  * FBI
  * CISA
* IT Landscape
  * On prems
  * Cloud services - shared responsibility model
  * Thin client
  * Thick client
  * Web apps
    * owasp
  * Mobile apps
* Assessing and mitigating vulnerabilities
  * Penetration testing
* Single point of failure
* Detective controls
  * siem
* References:
* 1. <https://www.ic3.gov/>
  2. <https://www.ic3.gov/Media/News/2021/210831.pdf>
  3. Cybersecurity and Infrastructure Security Agency (CISA): <https://www.cisa.gov/stopransomware>
  4. NIST: <https://csrc.nist.gov/projects/ransomware-protection-and-resp>
  5. <https://www.kroll.com/en/services/cyber-risk/assessments-testing/ransomware-preparedness-assessment>
  6. <https://redcanary.com/blog/how-one-hospital-thwarted-a-ryuk-ransomware-outbreak/>
  7. <https://www.hhs.gov/sites/default/files/maze-ransomware.pdf>
  8. <https://www.mandiant.com/sites/default/files/2022-10/Ransomware%20Defense%20Assessment.pdf>
  9. <https://intel471.com/glossary/threat-hunting>
  10. <https://www.tenable.com/solutions/ransomware>
  11. <https://www.crowdstrike.com/blog/ransomware-preparedness-a-call-to-action/>
  12. <https://cloud.google.com/blog/products/identity-security/5-pillars-of-protection-to-prevent-ransomware-attacks>
  13. <https://learn.microsoft.com/en-us/microsoft-365/security/defender/playbook-responding-ransomware-m365-defender?view=o365-worldwide>
  14. <https://www.cisa.gov/sites/default/files/2023-03/aa23-061a-stopransomware-royal-ransomware.pdf>
  15. <https://learn.microsoft.com/en-us/microsoft-365/security/defender/playbook-detecting-ransomware-m365-defender?view=o365-worldwide>
  16. <https://www.microsoft.com/en-us/security/blog/microsoft-detection-and-response-team-dart-blog-series/>
  17. <https://www.microsoft.com/en-us/security/blog/>
  18. <https://www.secretservice.gov/investigation/Preparing-for-a-Cyber-Incident>
* \
