# Threat Intelligence Tools and Techniques

Microsoft advanced threat analytics

Structured threat information sharing format STIX

TAXII

defense in depth NSA

Companies to follow on linked/Twitter/blog reading

* Proofpoint
* Microsoft security
* knowBe4

Organization to follow

* CISA
* NIST
* FBI
* MITRE ATTACK
* SANS
* UK NCS
* Australian Cyber division

<https://www.cia.gov/library/intelligence-literature>

STIX and Taxii

<https://oasis-open.github.io/cti-documentation/>

Cyber Threat Intelligence is combination of multiple operations

* Security Operation Center
  * Review the alerts
* Incident Response
  * Review the current plan
* System Engineering and IT
  * OS CIS benchmark scans
  * Application best practices
  * Password reuse policies
  * SSL certificate usage
* Business Operations
  * Aviation
  * Party/Service Providers
* Vulnerability Management
  * Tenable

Incident Response Questionnaires:

*Threat Intelligence Collections*

Internal Resources

* Endpoints
  * MS ATP
  * Sentinel One
  * Windows defender

* Email gateway
  * O365
* DNS
  * Infoblox
* Firewall
  * Palo Alto
  * F5 WAF
* Load Balancer
  * F5
* Router
  * Cisco

External Resources

IOC's

malicious files, URLs, domains, IPs, paths, filenames, Registry keys, and malware files themselves.

Droppers

* Single staged
* Multi staged

Command and Control

* cloud-based services
* Emails
* blog comments
* GitHub repositories
* DNS queries

Understanding different Malware families capabilities

Threat Intelligence Frameworks

* The cyber kill chain
* Diamond model
* Mitre attack framework

Active Countermeasures

* Modern attack operandi
* Already victim information collected
* Sunbrust/solarwinds/supply chain attacks
* Attacks are targeted
* Centralized logs collections
  * Syslog is not for security
  * How we are finding failover of log collection
* Adversaries stop log forwarding
* Threat hunting feed cant stop
* Empire and dnscat2
* Suricata signatures
* Proactive validation of all connected systems
* Include Desktops, laptops, cellphones, tablets, servers, network, printers, IoT, IIOT

 STIX and TAXII

* As of now we have subscription with ASIAC
  * Only TAXII 1  is working  : <https://a-isac.cyware.com/ctixapi/taxii/>
*  \[To Do]
  * Need to automatically integrate the threat intel with
    * LogRhythm
    * MS ATP

* References:
* <https://logrhythm.com/blog/logrhythm-threat-intelligence-services-stix-via-taxii/>
* <http://stixproject.github.io/supporters/>
* <https://www.anomali.com/resources/what-are-stix-taxii>

Threat Intel Resources\
<https://attack.mitre.org/>

<https://cve.mitre.org/>

<https://attack.mitre.org/groups/>

<https://attack.mitre.org/techniques/enterprise/>.

Product/service Follow

<https://redcanary.com/threat-detection-report/threats/socgholish/>

<https://secureworks.com>

<https://fireeye.com>

Mandiant

Google zero day finding

Microsoft

Kill chain

<https://www.lockheedmartin.com/en-us/capabilities/cyber/cyber-kill-chain.html>

Diamond model

mitre

Opencti.io

Stixx

Taxii

MISP

Here are some popular open-source threat intelligence tools:

* **AlienVault Open Threat Exchange (OTX):** A free community-driven threat intelligence platform that provides access to a vast collection of indicators of compromise (IOCs), malware samples, and threat actor data.
* **MISP (Malware Information Sharing Platform):** An open-source platform for sharing, storing, and collaborating on threat intelligence. MISP allows users to create and share threat indicators, reports, and other relevant information with other organizations and communities.
* **TheHive:** An open-source platform for incident response and collaboration. TheHive allows security teams to track incidents, share information, and collaborate on investigations. It also integrates with MISP and other threat intelligence tools.
* **Cuckoo Sandbox:** An open-source automated malware analysis sandbox that enables users to analyze suspicious files in a safe and isolated environment. Cuckoo Sandbox can help security analysts understand the behavior of malware and identify potential threats.
* **OpenCTI (Open Cyber Threat Intelligence):** An open-source platform for managing and analyzing cyber threat intelligence data. OpenCTI allows users to collect, store, and analyze threat intelligence from various sources and share it with others.
* **YARA:** An open-source framework for identifying and classifying malware. YARA uses text patterns to identify malicious code and can be used to create custom rules to detect specific threats.
* **Maltego:** A free community-driven link analysis tool that can be used to investigate relationships between different entities, such as IP addresses, domains, and malware samples. Maltego can be helpful for identifying connections between different parts of a cyberattack.
* Urlscan.io <https://urlscan.io/>
* abuse.ch <https://abuse.ch/>
* Phishing Tool <https://app.phishtool.com/sign-up/community>
* Cisco Talos Intelligence <https://talosintelligence.com/>

## In this section

* ✅ [Yara](yara.md)
