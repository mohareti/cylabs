# Threat Hunting

- [Indicators of Compromise](indicators-of-compromise.md)

---

Based on the provided notes, here is a reorganized and detailed threat hunting process:

## I. Threat Hunting Definition and Preparation

* **Definition**: Proactive and iterative search to validate all assets connected within an organization's network.
* **Starting Points (Hypotheses)**:
  * Suspected phishing emails.
  * Anomalous behaviors.
  * Unauthorized drive downloads.
  * Credential hijacking incidents.
  * Unusual external connections.

## II. Data Collection and Analysis

* **Data Collection**:
  * From endpoints, firewalls, applications, and network.
* **Analysis**:
  * Examine connections received at the time of incident.
  * Investigate remote logins via TeamViewer.
  * Analyze usage of SMB 1 protocol.
* **Hypothesis Validation**: Conclude if the initial hypotheses hold true.

## III. Network and Asset Understanding

* **Network Architecture**: Diagrams and documentation of network layout.
* **Asset Management**: Inventory of all assets, departments, DMZ servers, firewalls, routers, switches, WAFs, desktops, servers, printers, IOT/SCADA systems.
* **Security Controls**: Identification of preventive and detective security measures in place.

## IV. Centralized Log Collection

* **Purpose**: To streamline the analysis of system logs.
* **Logging Details**: Use Syslog port numbers and regex for efficient threat hunting in raw logs.

## V. Log Source Management

* **Sources**: Include firewall logs, IDS/IPS, VPN, proxies, endpoint/EDR systems, MFA, authentication, and authorization logs.
* **Past References**: Review previous penetration tests and audit reports for insights.

## VI. Indicators and Threat Intelligence

* **Indicators**: Understanding of Indicators of Compromise (IoCs) and Indicators of Attack (IoAs).
* **Threat Intelligence**: Focus on behavioral patterns instead of static indicators like IPs or DNS due to their dynamic nature.

## VII. Detection Systems and Organizational Security Posture

* **Systems**: Implementation of host and network intrusion detection systems like Suricata.
* **Security Posture**: Regular audits, internal penetration tests, and proactive vulnerability management.

## VIII. Proactive Measures and Research

* **Proactivity**: Shift from reactive measures like SOC alerts to proactive threat hunting.
* **Research**: Check for disabled logging or antivirus, and understand malware persistence mechanisms.

## IX. Threat Hunting Approaches

* **Active Hunting**: Engage in asset isolation and memory forensics.
* **Passive Hunting**: Review packets and SIEM logs for anomalies.

## X. Specialized Threat Hunting Techniques

* **Network Jitter**: Analyze and understand the variation in C2 communication timing.
* **Firewall Utilization**: Use firewalls strategically for threat hunting.

## XI. Avoiding False Positives

* **Validation**: Confirm the legitimacy of network connections and protocol communications.
* **Outbound Protocols**: Monitor standard and non-standard ports for unexpected application traffic.

## XII. Advanced Threat Hunting Methods

* **Tools**: Usage of Rita, Zeek, Tcpdump, Sysmon, and Wireshark.
* **Analysis**: Investigate network connections, session sizes, and persistence.
* **Intelligence**: Utilize platforms like AbuseIPDB and DNSlytics for additional data.

## XIII. Post-Incident Activity

* **Remediation**: Implement patches and manage updates.
* **Documentation**: Report findings and adjust strategies based on insights.

## XIV. Toolset for Threat Hunting

* \*\*

Utility Tools\*\*: Empire, Dnscat2, Rita, Zeek, Tcpdump, Sysmon, Wireshark, Ngrep, Grep.

* **Analysis Tools**: Passer for tracking cookies, Threat simulator for simulating threats, Imphash-Mandiant for malware analysis.

## XV. Custom Scripting and Frameworks

* **Scripting**: Utilize PowerShell and Kibana for custom search queries and monitoring.
* **Frameworks**: Explore tools like Powersploit and Deepwhite.

## XVI. Addressing Ransomware and Malware

* **Detection**: Employ Sysmon for WMIC detection and integrate with VirusTotal for a comprehensive overview.
* **Ransomware**: Study specific ransomware patterns like SAMSam and develop countermeasures.

## XVII. Posture Improvement

* **Audit Controls**: Adhere to required audit controls and manage responsibilities for patching vulnerabilities.
* **Network Anomalies**: Investigate unusual activities such as persistent connections to cloud storage and abnormal user-agent strings.

## XVIII. Incident Response

* **Response Plan**: Develop a clear incident response plan for identified threats.
* **Connection Analysis**: Examine outbound connections and validate whether they are legitimate business needs.

## XIX. Further Considerations

* **Beaconing and Botnet Detection**: Look for signs of beacon heartbeats and botnet activity.
* **Persistence Mechanisms**: Identify and address persistent threats and their communication patterns.

## XX. Documentation and Reporting

* **Record Keeping**: Maintain detailed logs and document all threat hunting activities.
* **Report Generation**: Create comprehensive reports for management and technical staff outlining threats, findings, and recommendations for improvements.

## XXI. Continuous Education and Improvement

* **Training**: Keep the security team updated with the latest threat hunting practices and tools.
* **Improvement Plans**: Continually refine threat hunting processes based on the latest trends and organizational changes.

## XXII. Legal and Compliance

* **Compliance**: Ensure all threat hunting activities are compliant with legal and regulatory requirements.
* **Privacy**: Respect privacy laws and regulations while conducting threat hunts.

By organizing the threat hunting process as outlined above, security teams can approach threat hunting in a structured, systematic, and effective manner.

Threat Hunting Resources:

Threat Hunting Maturity Models:

\- Effective Threat Hunting Models: <https://www.sans.org/reading-room/whitepapers/analyst/membership/36785>

\- Sqrrl team data-driven methodology: <https://www.cybersecurity-insiders.com/5-types-of-threat-hunting/>

\- Roberto (@Cyb3rWard0g) and José Luis (@Cyb3rPandaH) methodology: <https://www.youtube.com/watch?v=DuUF-zXUzPs>

Threat Hunting Playbooks and Platforms:

\- HELK (hunting platform): <https://github.com/Cyb3rWard0g/HELK>

\- ThreatHunter Playbook: <https://github.com/hunters-forge/ThreatHunter-Playbook>

\- Jupyter Book on Threat Hunter Playbook: <https://medium.com/threat-hunters-forge/writing-an-interactive-book-over-the-threat-hunter-playbook-with-the-help-of-the-jupyter-book-3ff37a3123c7>

Threat Hunting Methodologies and Guides:

\- Generating Hypotheses for Successful Threat Hunting: <https://www.sans.org/reading-room/whitepapers/threats/paper/37172>

\- Security data modeling with OSSEM: <https://github.com/OTRF/OSSEM>

\- Adversary Emulation Plans by MITRE: <https://attack.mitre.org/resources/adversary-emulation-plans/>

\- Computer Security Log Management Guide: <https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-92.pdf>

Event Logs and Windows Monitoring:

\- Microsoft Windows API documentation: <https://docs.microsoft.com/en-us/windows/win32/apiindex/api-index-portal>

\- PowerShell and Event Logs: <https://evotec.xyz/powershell-everything-you-wanted-to-know-about-event-logs/>

\- PowerShell command for Active Directory auditing: <https://evotec.xyz/the-only-powershell-command-you-will-ever-need-to-find-out-who-did-what-in-active-directory/>

\- Windows File System Auditing: <https://www.varonis.com/blog/windows-file-system-auditing/>

\- Viewing AD logs in Event Viewer: <https://community.spiceworks.com/how_to/166859-view-ad-logs-in-event-viewer>

MITRE ATT\&CK and CAR Framework:

\- MITRE ATT\&CK Matrices: <https://attack.mitre.org/matrices/enterprise/>

\- MITRE ATT\&CK Navigator: <https://mitre-attack.github.io/attack-navigator/>

\- CAR Framework: <https://car.mitre.org/>

\- C2 Matrix: <https://www.thec2matrix.com>

Tools and Frameworks:

\- yarGen: <https://github.com/Neo23x0/yarGen>

\- SilkETW: <https://github.com/mandiant/SilkETW>

\- Uber Metta: <https://github.com/uber-common/metta>

\- Endgame Red Team Automation: <https://github.com/endgameinc/RTA>

\- Invoke-Adversary: <https://github.com/CyberMonitor/Invoke-Adversary>

\- Infection Monkey: <https://github.com/guardicore/monkey>

\- OSSEM Power-up: <https://github.com/hxnoyd/ossem-power-up>

\- Sysmon Modular: <https://github.com/olafhartong/sysmon-modular>

\- DeTT\&CT: <https://github.com/rabobank-cdc/DeTTECT/>

Posters

<https://www.sans.org/posters/hunt-evil/>

## In this section

* 🚧 [Indicators of Compromise](indicators-of-compromise.md)
* ✅ [Threat Hunting Blogs](threat-hunting-blogs.md)
* ✅ [Ransomware: An Overview](ransomware-an-overview.md)
* ✅ [Threat Hunting and Incident Response Q&A](threat-hunting-and-incident-response-qanda.md)
* ✅ [Network Traffic Analysis: Wireshark](network-traffic-analysis-wireshark.md)
* ✅ [Threat Hunting Questionnaire](threat-hunting-questionnaire.md)
* ✅ [KQL](kql.md)
* ✅ [Email Header Analysis](email-header-analysis.md)
* ✅ [Threat Hunting Playbook](threat-hunting-playbook.md)
* 🚧 [Windows Process Exploration](windows-process-exploration.md)
