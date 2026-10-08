# Ransomware Prevention

Cyber Gap Analysis (Ransomware protection)

* Enforce MFA, use least privileges or just-enough privilege, and implement Privileged Access Management (PAM) and Privileged Identity Management (PIM).
* Patch and update all software, OSs (including network devices) to the latest supported versions.
* Ensure you are using the latest protection solutions including EDR or Extended Detection and Response (XDR).
* Implement next-generation network protection: firewalls, Intrusion and Detection Prevention (IDP), Intrusion Prevention Systems (IPSs), and so on.
* Implement network segmentation.
* Restrict the use of scripting to approved users.
* Secure your Domain Controllers (DCs).
* Block access to malicious sites.
* Only allow trusted devices on your network.
* Disable the use of macros.
* Only allow approved software to be used by your users.
* Remove local admin permissions.
* Enable advanced filtering for email.
* Use Sender Policy Framework (SPF), DomainKeys Identified Mail (DKIM), and Domain-based Message Authentication, Reporting, and Conformance (DMARC).
* Block Server Message Block (SMB) outbound protocol and remove outdated versions.
* Follow best practices to harden your end-user and infrastructure devices.
* Protect your cloud environment with best practices, especially public file shares.
* Review your remote strategy and ensure outside connections into your environment are secure. If Remote Desktop Protocol (RDP) is needed, ensure best practices are deployed.
* For backups, maintain an offline backup or air gap, encrypt all backups, and validate recovery by testing regularly.
* Implement and focus attention on a well-defined Vulnerability Management Program (VMP).
* Implement a good cybersecurity and awareness program. Train users not to click on links or open attachments unless they are confident they are legitimate.
* Build a mature Vendor Risk Management (VRM) program.
  * Understanding current organization security environment and posture
  * Understanding critical information security issues faced/facing by organization
  * Initiating cyber security best practices
  * Developing modern Cyber Security program with Defense in Depth and Zero Trust
  * Developing Cyber Security Strategies to mitigate threats
* Directing/Managing
  * Asset Management
    * High valued assets
    * Critical assets for operations
  * Cyber Physical Security Management
  * Hardware Security Management
  * IOT/OT/SCADA Security Management
  * Cyber Security Operations
    * SIEM
      * Audit log management
    * SOC
      * SOC Playbooks
    * SOAR
    * Incident Response
      * Identifying
      * Containing
      * Eradicating
      * recovering
    * Security breach management
      * Ransomware
      * Data loss
    * Shadow IT
  * Cloud Security Management
    * Cloud Security Architecture
    * Cloud Security tools
      * CASB, CWPP, CSPM
    * Security attacks
    * Cloud security frameworks
      * CSA, cloud adoption frameworks
      * Cloud computing policy
      * Cloud storage policy
    * Zero trust on cloud
  * SecDevOps/DevSecOps/Security Engineering
    * Shift left with security in DevOps Pipeline
    * Security Misconfigurations
    * Security automation
      * Infrastructure as code
    * Data Encryption
      * Symmetric
      * Asymmetric
      * Hashing
      * Encoding
      * Key exchange
      * Certificates
      * Digital signature
    * Data Privacy
  * Application Security
  * Secure Coding and software development
  * Security Awareness
    * Security First
    * Security Situational Awareness
  * Cryptography, Data Security and Protection
  * Vulnerability and Patch Management
    * Build
    * Audit
    * Review
  * Network Security/Perimeter security
    * Layered security controls
    * NGFW, NSM, IDS/IPS, Load Balancers, Proxies,
    * VPN, IPsec
  * Endpoint Security
    * End-user Security
    * EDR, XDR, HIDS,HIPS, EPP, FIM, Sandboxing, whitelist/blocklist
    * Malware defense
  * Cyber Security Governance, Risk,  Compliance Management
    * Risk Assessment and Management
    * Information security Management
    * Security policies
      * Business continuity
      * Disaster Recovery
    * Cyber Security Maturity Models
  * Cyber Security Architecture
    * Zero Trust Model
      * Zero trust network access
  * Cyber Security Frameworks and controls
    * NIST cyber security framework
    * CIS critical controls
    * CMMC
    * NIST SP 800-171
    * NIST SP 800-53
  * Cyber Defense architecture and frameworks
    * MITRE ATT\&CK
  * Cyber Security Standards
  * Cyber Security Reporting
  * Cyber Gap Analysis
  * Cyber Security Strategic Plan
  * Security workflow and relationships among multiple teams
  * Cyber Security Budget Management
  * Cyber Security Team performance, growth, learning
  * Penetration Testing/Red Team
  * Bring your own device policies
  * Remote work policies
  * Cyber Security product and services SLA's
  * Developing Non-Disclosure Agreements
  * Cyber Threat Landscape
    * Threat actors
    * Nation state attacks
    * TTP's
    * Critical business operations
    * Stakeholders
  * Organization business goals and vision
  * Security metrics
    * Weekly
    * Monthly
    * Quarterly

Preparation:

* Offline backups availability and integrity check
* Maintain and Audit golden images and build templates
* Use of Infrastructure as a code to deploy images
* Manage IaC in versions for audit purpose
* Storing application source code or executables as backup
* Removing and replacing outdated hardware
* Using multi cloud solutions and maintaining cloud backups, using immutable storage solutions
* Audit cloud environment
* Develop and audit incident response, communication and breach notification plan
* Develop Cyber incident response playbook
* Build and implement Zero  Trust Architecture

Prevention and Mitigating:

* Develop surface discovery plan and audit attack finding
  * Monitor deep web notification/credential monitoring services
* Periodical vulnerability Scans (review CISA Know vulnerability list)
  * External
  * Internal
  * VPN Infra
* Periodical patch management
* Assets security
  * BYOD
  * All devices on hybrid infrastructure
* Protocol, port and service usage metrics
  * RDP
* Have visibility to configuration and change management
* Implement MFA
* Disable weak protocols
  * SMB v 1 and v 2
  * Audit SMB traffic
  * Implement SMB signing and audit
* Blocking external access
  * SMB
    * TCP 445
    * UDP 137
    * UDP 138
    * TCP 139
  * Implement SMB encryption with Universal Naming Convention (UNC) hardening
  * Log and monitor SMB and RDP traffic

Initial Access:

* Implement
  * Phishing resistant MFA and password less MFA
  * IAM
  * PAM
* Change default creds
* Restrict use of root or system admin users s
* Password minimum length and policies
  * Password rotation
  * Password management tools
* Failed login attempts metrics and audit
* Disabling saving passwords to browser using Group Policy
* Local Administrator Password solution (LAPS)
* LSASS : implement attack surface reduction rule
* Windows credential guard
* Use Windows PowerShell Remoting, Remote Credential Guard, or RDP with restricted

Admin Mode

* Separation of admin and user accounts
* Conduct security awareness training
* Email attachments known bad
* Disable office macros
* Disable Windows Script Host (WSH)
* Review malware infections
  * Ex: s QakBot, Bumblebee, and Emotet
* Phishing email metrics and BEC scams
  * How many blocked
  * How many bypassed
* EDR implementation
  * Windows Defender Application Control (WDAC), AppLocker
  * Application allow listing
  * Implement of EDR on cloud
* Threat intel and feed into security stack
* Security awareness training
* Protective DNS
* Sandboxed browsers
* Monitor
  * Seo poisoning
  * Drive by download
  * Malvertising
* Restricting PowerShell usage and alerts

Keywords:

CISA

MSISAC

FBI IC3

NSA

ZTA

References:\

download: <https://ofac.treasury.gov/media/912981/download?inline>

Stop Ransomware | CISA: <https://www.cisa.gov/stopransomware>

Cross-Sector Cybersecurity Performance Goals | CISA: <https://www.cisa.gov/cross-sector-cybersecurity-performance-goals>

Public-Power-Cyber-Incident-Response-Playbook.pdf: <https://www.publicpower.org/system/files/documents/Public-Power-Cyber-Incident-Response-Playbook.pdf>

Zero Trust Maturity Model | CISA: <https://www.cisa.gov/zero-trust-maturity-model>

CSI-MITIGATING-CLOUD-VULNERABILITIES\_20200121.PDF: <https://media.defense.gov/2020/Jan/22/2002237484/-1/-1/0/CSI-MITIGATING-CLOUD-VULNERABILITIES_20200121.PDF>

KB5005413: Mitigating NTLM Relay Attacks on Active Directory Certificate Services (AD CS) - Microsoft Support: <https://support.microsoft.com/en-us/topic/kb5005413-mitigating-ntlm-relay-attacks-on-active-directory-certificate-services-ad-cs-3612b773-4043-4aa9-b23d-b87910cd3429>

Overview of Server Message Block signing - Windows Server | Microsoft Learn: <https://learn.microsoft.com/en-us/troubleshoot/windows-server/networking/overview-server-message-block-signing>

Manage Windows Defender Credential Guard (Windows) | Microsoft Learn: <https://learn.microsoft.com/en-us/windows/security/identity-protection/credential-guard/credential-guard-manage>

Exchange Online Protection feature details - Service Descriptions | Microsoft Learn: <https://learn.microsoft.com/en-us/office365/servicedescriptions/exchange-online-protection-service-description/exchange-online-protection-feature-details?tabs=Anti-spam-and-anti-malware-protection>

CISA Insights - Cyber: Enhance Email & Web Security: <https://www.cisa.gov/sites/default/files/publications/CISAInsights-Cyber-EnhanceEmailandWebSecurity_S508C-a.pdf>

How DMARC Advances Email Security: <https://www.cisecurity.org/insights/blog/how-dmarc-advances-email-security>

Malicious Domain Blocking and Reporting (MDBR): <https://www.cisecurity.org/ms-isac/services/%20mdbr>

Macros from the internet are blocked by default in Office - Deploy Office | Microsoft Learn: <https://learn.microsoft.com/en-us/deployoffice/security/internet-macros-blocked>

CSI\_Selecting a Protective DNS Service\_U00117652-21.PDF: <https://media.defense.gov/2021/Mar/03/2002593055/-1/-1/1/CSI_Selecting%20a%20Protective%20DNS%20Service_U00117652-21.PDF>

Microsoft Office 365 Security Recommendations | CISA: <https://www.cisa.gov/news-events/cybersecurity-advisories/aa20-120a>

csi\_keeping\_powershell\_security\_measures\_to\_use\_and\_embrace\_20220622.pdf: <https://media.defense.gov/2022/jun/22/2003021689/-1/-1/1/csi_keeping_powershell_security_measures_to_use_and_embrace_20220622.pdf>

Best Practices for Securing Active Directory | Microsoft Learn: <https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/plan/security-best-practices/best-practices-for-securing-active-directory>

BloodHound, Software S0521 | MITRE ATT\&CK®: <https://attack.mitre.org/versions/v13/software/S0521/>

Securing Active Directory Administrative Groups and Accounts | Microsoft Learn: <https://learn.microsoft.com/en-us/previous-versions/tn-archive/cc700835(v=technet.10)?redirectedfrom=MSDN>

Albert Network Monitoring and Management: <https://www.cisecurity.org/services/albert-network-monitoring>

KB5005413: Mitigating NTLM Relay Attacks on Active Directory Certificate Services (AD CS) - Microsoft Support: <https://support.microsoft.com/en-us/topic/kb5005413-mitigating-ntlm-relay-attacks-on-active-directory-certificate-services-ad-cs-3612b773-4043-4aa9-b23d-b87910cd3429>

download: <https://ofac.treasury.gov/media/912981/download?inline>

6 Incident Response Steps to Take After a Security Event: <https://www.exabeam.com/incident-response/steps/>

<https://www.malware.us-cert.gov>: <https://www.malware.us-cert.gov/>

Election Security Spotlight – Malware Analysis: <https://www.cisecurity.org/insights/spotlight/cybersecurity-spotlight-malware-analysis>
