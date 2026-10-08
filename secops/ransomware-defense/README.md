# Ransomware Defense

Go based Ransomware/Malware

* BlackCat
* RobbinHood
* Nefilim
* EKANS
* Zebrocy - Russian state-sponsored group APT28 created a Go-based version of their Zebrocy malware last year.
* WellMess - Russian state-sponsored group APT29 deployed new upgraded versions of their Go-based WellMess malware last year.
* Godlike12 - A Chinese state-sponsored group deployed Go-based backdoors for attacks on the Tibetan community last year.
* Go Loader - The China-linked Mustang Panda APT deployed a new Go-based loader last year for their attacks.
* GOSH - The infamous Carbanak group deployed a new RAT named GOSH written in Go last August.
* Glupteba - New versions of the Glupteba loader were seen in 2020, more advanced than ever.

Nim based Ransomware/Malware

Rust based Ransomware/Malware

* Buer

Dlang based Ransomware/Malware

C

C++

.NET

C#

Java

Objective-c

Python

Perl

Javascript

Powershell

WebAssembly

Delphi

RAT (Remote Access Trojans)

* Cobalstrike
* Remcos
* Nanocore

Crypto Miners

Data exfiltration

* Rclone
* 7zip

Malicious behavior

* deleting backups and logs
* Changing firewall
* Azure Credentials

Which programming languages are hard to reverse engineer

Analyzing ELF files and PE

Win32 API's

References:

<https://unit42.paloaltonetworks.com/blackcat-ransomware/>

<https://www.trendmicro.com/vinfo/us/security/definition/Ransomware>

<https://github.com/redcode-labs/Neurax>

<https://github.com/redcode-labs/Coldfire>

<https://github.com/ponty/pyscreenshot>

Wazuh

\- HIDS

\- OSSEC

MISP

\- Threat Intellegence

Zeek/Suricata/Snort

\- IDS/IPS

PFSense

\- Firewall

Perimeter security logs collected from PFsense and Zeek (span port )

using file beat to forward data to Elkstack(log stash)

AD/DC

\- Winlog Beat

\- Metric Beat

Linux server

\- Audit Beat

\- Metric Beat

\- File Beat

SOAR

\- The Hive

Siemplify

SoC Architectures

Log Collection

Log Parsing

Events

Threat Intel (ingest)

Threat detection

Alerts

Threat investigation

Incident Response

Forensics

Netflow

Switch spanport -> zeek  ids - different logs

Switch spanport -> suricata -> json (Event.log)

Switch spanport -> Moloch/arkime -> pcap

NSM distribution

* Security onion
* SELKS
* CAPESStack
* HELK
* ROCK NSM

Host Data collections

Event Generation

* OSSEC
* Sysdig for container security
* Windows sysinternals
  * sysmon
* Osquery
* Wazuh

Data Shippers/aggregators

* Beats
  * Filebeat
  * Winlogbeat
  * Audit beat
  * Packetbeat
  * Journalbeat
  * Functionbeat
  * Heartbeat
  * DIY beats

* LogStash
* Nxlog
* Fluentd
* Nifi

SIEM

Graylog

Apache metron

Alien vault

Sigma

Jupyter

Sguil

Evebox

Incident management

TheHive

Sigma

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

## In this section

* ✅ [APT Groups](apt-groups.md)
