# Cyber Defense & SOC

## What is Defensive Security?

Defensive security, also known as cybersecurity, focuses on protecting an organization's assets and preventing unauthorized access, use, disclosure, disruption, modification, or destruction of their information systems and data.

## Key Strategies in Defensive Security

* **Defense in Depth:** A multi-layered defense approach that uses various security tools and mechanisms. This ensures that even if one control fails, others are in place to mitigate the risk.
* **Least Privilege:** This principle ensures users have only the access they absolutely need to perform their job functions. This reduces the attack surface attackers can exploit.
* **Network Segmentation:** Separating a network into smaller segments using firewalls and other mechanisms, minimizing the spread of an attack if one segment is compromised.
* **Security Awareness Training:** Educates employees about security risks such as phishing, malware, social engineering tactics, and password best practices.
* **Perimeter Defenses:** Measures to control traffic entering and leaving an organization's network. This typically includes:
  * **Firewalls:** Filter network traffic based on defined rules.
  * **Intrusion Detection & Prevention Systems (IDS/IPS):** Detect and potentially block malicious activity
* **Endpoint Security:** Security solutions installed directly on devices like laptops, and servers. This may include:
  * **Antivirus/Antimalware:** Detects and blocks known malicious software
  * **Endpoint Detection & Response (EDR):** Provides advanced detection and response capabilities on endpoints.
* **Data Protection:** A range of strategies to protect sensitive data
  * **Encryption:** Transforms data into unreadable code, preventing access without decrypting it.
  * **Data Loss Prevention (DLP):** Solutions that monitor and prevent unauthorized movement of sensitive data.
  * **Backup & Recovery:** Process of making regular copies of data and well-defined procedures for restoring it in case of loss or corruption.
* **Vulnerability Management:** The ongoing process of:
  * **Identifying Vulnerabilities:** Using automated tools and processes to scan for potential weaknesses.
  * **Prioritizing Risks:** Categorizing vulnerabilities by the level of the risk they pose.
  * **Patching and Remediation:** Applying relevant software updates, configuration changes, and workarounds to fix identified vulnerabilities.

## The Importance of Defensive Security

A strong defensive security posture is crucial for organizations of all sizes. Cyberattacks are becoming increasingly frequent and sophisticated, and the consequences of data breaches can be devastating, including:

* **Financial Loss:** From direct theft, remediation costs, and ransoms
* **Reputational Damage:** May result in loss of customer trust.
* **Operational Disruption:** Attacks can disrupt business operations.
* **Legal & Regulatory Penalties:** Noncompliance with regulations can result in fines.

## Remember

* **No System Is Impenetrable:** Even with strong defenses, there's always a risk. Continuous effort is essential.
* **Balance with Usability:** Security shouldn't overly hinder functionality.
* **Defense Is Layered:** Defensive security isn't about a single solution but rather a strategic, multi-layered approach.

## Enhancing Security Posture Using CISA Security Catalog and Best Practices

## A. Understanding and Prioritizing Potential Attack Vectors

* **Internet-Facing Systems:**
  * Ensure network and security appliances are up-to-date and monitored.
  * Keep web servers secured against known exploits and regularly update security patches.
  * Implement rigorous security measures for web applications, including code reviews and vulnerability scanning.
  * Maintain the host operating system with the latest security updates and monitoring tools.
  * Consider the feasibility and benefits of employing endpoint detection and response (EDR) on network appliances.

## B. Securing Client Interfaces and Applications

* **Client Software Security:**
  * Regularly update and patch critical software such as MS Office and Adobe PDF readers to mitigate exploit risks.
  * Secure browsers through configuration settings that minimize vulnerabilities and restrict unauthorized plugins.
  * Maintain mobile apps with up-to-date security practices to prevent data breaches on mobile devices.
  * Ensure Host OS and Mobile Devices are equipped with the latest security patches and protective software.

## C. Internal Infrastructure Protection

* **Server and Software Security:**
  * Protect database servers by implementing strong access controls and regular audits.
  * Secure applications through continuous integration/continuous deployment (CI/CD) practices that include security testing.
  * Manage file servers with strict access permissions and monitoring to detect unauthorized access or anomalies.
  * Enhance the security of IoT devices with regular firmware updates and monitoring for suspicious activities.
  * Ensure printers and other peripheral devices are not overlooked in the security framework, especially those connected to the network.

## D. Proactive Security Maintenance

* **Update Management:**
  * Configure systems for automatic updates where feasible to ensure continuous protection against vulnerabilities.
  * Establish protocols for manual patching, including the tools required for effective vulnerability management.
  * Utilize CISA's catalog of known exploited vulnerabilities to guide scanning and remediation efforts.

## E. Log Management and Network Traffic Control

* **Monitoring and Filtering:**
  * Implement comprehensive logging from critical resources and establish procedures for regular review.
  * Control and monitor outbound traffic through firewall rules that block unnecessary IP ranges and ensure egress rules are reviewed periodically for relevance and effectiveness.
  * Deploy web content filtering strategies using web proxies and firewalls to block uncategorized domains and specific content types that pose security risks.
  * Apply DNS content filtering to prevent connections to malicious sites and domains.

## F. Attack Mitigation and System Integrity

* **Malware and Attack Prevention:**
  * Deploy network monitoring tools to gain visibility into network traffic and potential threats.
  * Establish limits on malware execution through restrictive policies and anti-malware tools.
  * Prevent Living off the Land (LOLBin) attacks by monitoring and controlling the use of legitimate system tools for malicious purposes.
  * Use the Srum-dump tool for forensic analysis and gaining insights into system usage patterns.

## G. Application Inventory and Management

* **Operational Security:**
  * Conduct a thorough inventory to determine which applications are running across the organization's infrastructure, focusing on both sanctioned and unsanctioned software.

By systematically addressing each area, organizations can effectively leverage the guidance provided by CISA, maintain a strong security posture, and minimize the risk of successful cyber attacks.

## In this section

* ✅ [Security Operations Center (SOC)](security-operations-center-soc/README.md) · 2/2 pages written
* 🚧 [Different Classes of Threat Actor](different-classes-of-threat-actor.md)
